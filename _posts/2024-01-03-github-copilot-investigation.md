---
title: "Crash landing or a soaring success? Investigating GitHub’s AI pair programming tool, Copilot."
date: 2024-01-03
author: "Frankie Clipsham"
---

## Introduction
In my last blog, I spoke about not knowing the capability of GitHub Copilot. I decided to change this by signing up for the 30-day free trial and I began my investigation. I set out to determine the effectiveness, accuracy and security of GitHub Copilot as a tool for programmers. The end goal is a consideration of whether the monthly subscription costs involved are justified and the security measures are satisfactory.

For context, GitHub Copilot is an AI-powered assistant specifically trained to assist with programming. It can be installed as an extension in your programming environment (IDE) of choice to give code completions, explanations or 
suggest fixes. This investigation primarily used the Visual Studio Code IDE for reasons explained later.

## First Impressions
Inline chat was the most useful way I found to interact with Copilot. It's triggered by hitting `Ctrl` + `I` with a file open or with a segment of code selected.

Copilot has a `/explain` feature that will use the context of the highlighted code and the user's prompt to succinctly detail a section of code. This could be particularly beneficial for junior programmers or anyone attempting to get to grips with a new code base to understand the code. Furthermore, programmers working with code not written in their primary language could make use of this feature to improve their confidence and help with the syntactical nuances. 

The `/fix` command can be used on errors to help debug issues in the code. Copilot provided me multiple valid suggestions for fixes in YAML pipelines when I references the line causing the build failures. 

There is also a `/doc` feature that can be used to document or add comments to old/unsupported code. This could be particularly useful for those who forget to write or dislike writing documentation.

These features would also benefit senior programmers as there would be more support for juniors. This would result in less time spent on calls explaining code, debugging a missing semi-colon or resolving other syntax errors. The code quality should remain relatively high as Copilot is aware of the code-base as context so it makes attempts to follow coding standards set when making suggestions.

## Examples
The three features particularly useful from GitHub Copilot during my investigation were code completions, suggestions and explanations. Below I have provide some examples, which I believe, detail the necessity for Copilot as a tool for programmers.

### Code Completion

#### 1. Code completion for an Azure Pipelines `docker login` task

This completion was appreciated as my next step would have been to include the login step. The completion saved me time and managed to include the valid service connection variable name from the context of the current file.

![Pipeline code completion 1](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/code%20completion%20pipelines%201.png)

#### 2. Python code completion
The completion below was accurate and welcome as it was the next code I was about to write. Copilot managed to pick up on the fact that I was attempting to update the message content if the message `role` property was `system` and if the `system_message_content` variable was set.

![Python code completion](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/python%20code%20completion.png)

#### 3. App settings definition assisted with code completion
 In this example, I was manually defining my app's settings in a pipeline and it managed to perfectly suggest the next three settings which I was about to type. It used the context from the first variable `DOCKER_REGISTRY_SERVER_PASSWORD` to determine the next settings required and then matched my variable format. This is a great example of the time-saving benefit of GitHub Copilot as the manual process is very mundane and time-consuming.

![App settings code completion 1](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/app%20settings%202.png)
### Code Suggestions

#### 1. App settings code suggestion from prompt
This example is very similar to the one above, however, I prompted Copilot with the list of known app settings names. It then added them to the existing list of app settings and matched the correct format e.g. `APP_SETTING_1` = `-APP_SETTING_1 $(APP_SETTING_1)`. This saved me a great deal of time typing out each specific app setting.
![App settings code completion 2](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/app%20settings%201.png)

#### 2. Accurate code suggestion from a very simple prompt
Here I was trying to define an Azure Pipelines stage with multiple dependencies. The previous build failed stating an error in this line. I simply prompted Copilot with `depends on multiple` as it it was a syntax issue and it quickly suggested a re-format, which resulted in a successful pipeline run.

![Pipeline code suggestion depends on](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/depends%20on%20multiple.png)

### Code Explanation
#### 1. Explanation of code in an unfamiliar code base and language
This example shows an inline chat to determine if a message could still be added to an array if it was a constant or `const` definition. The code-base was not written by me and this was the first time viewing it. The idea of a constant being updated confused me. Thankfully, Copilot provided a clear explanation as to why the code works fine. 
![Constant explain](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/constant%20explain.png)

#### 2. Explanation of unfamiliar line in a YAML pipeline file
During an update to some pipelines, I was curious why the documentation stated a `.` at the end of the build command. I highlighted line `58` and started a chat with Copilot to determine why this was needed. Copilot used the context of the code and its understanding of Docker to provide a clear and concise explanation as to why the `.` was needed at the end.
![Pipelines explain](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/pipelines%20explain.png)

### Chat GPT vs GitHub Copilot
I decided to compare ChatGPT and GitHub Copilot by asking the same question: How do I set the admin user property on an Azure Container Registry in a Bicep template? ChatGPT was provided with the existing resource definition for context. In the images below ChatGPT was completely off from the documented approach by [Microsoft](https://learn.microsoft.com/en-us/azure/templates/microsoft.containerregistry/registries?pivots=deployment-language-bicep#:~:text=properties%3A%20%7B%0A%20%20%20%20adminUserEnabled%3A%20bool). It was attempting to use Role-based access control assignments, but Copilot suggested the correct addition and saved some time researching.

#### ChatGPT
![GPT Code suggestions](https://raw.githubusercontent.com/frank-64/ToBeFrank/aec2ec3606ee8a792e441795b38f41acda986559/assets/images/admin%20user%20chatgpt.png)

#### GitHub Copilot
![Copilot Code suggestions](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/admin%20user%20copilot.png)

## Security Concerns

There's the obvious elephant in the room when we talk about AI and that is our data. When working with sensitive information or intellectual property it's a very valid concern to have considering Copilot uses the source code to generate completions and suggestions. 

GitHub Copilot is being used in dev teams by huge enterprise companies from sectors such as banking, distribution, e-commerce and aviation. These companies have done their due diligence when it comes to security concerns and are satisfied with the level of security implemented for Copilot. For most companies, weak security and privacy is a deal breaker, so it seems this has been prioritised by GitHub during Copilot's development.

Here are just some measures GitHub are taking to ensure privacy and security **(Enterprise or Business plans only)**:

1. Azure infrastructure is used throughout to ensure encryption in transit and at rest.
2. Prompts are not stored as they are discarded once a suggestion is returned.
4. Code used as context is destroyed in memory once a suggestion is returned.
3. Prompts, code and other contexts are not used for training models.
4. Prompt content is not logged or exposed via an API.

You can read more on this here: [GitHub docs](https://resources.github.com/copilot-trust-center/)

There are also concerns about secrets being leaked and displayed in some Copilot suggestions. The reason some suggestions contained secrets is because Copilot is trained from **public** GitHub repositories. If these secrets are contained in these public repositories then anyone can see them regardless. This should only be a concern if you are using hard-coded secrets, which is far from best practice, anyway. You should be using environmental variables or ideally managed secrets in something like Azure Key Vault.

### Copilot for Business
It is **crucial** that I mention the security measures above are exclusive to the Copilot Business plan and Enterprise plan (coming Feb 2024). As far as I'm aware this means that the free trial or Copilot Individual plan *may* train its model using your code-base and store prompts. GitHub claims that code stored in public GitHub repositories is currently used to train the model as mentioned [here](https://docs.github.com/en/copilot/overview-of-github-copilot/about-github-copilot-individual#:~:text=GitHub%20Copilot%20is%20powered,data%20for%20that%20language.). So, for work on client projects the business plan at $19 per user/per month would be satisfactory to ensure code security.

![GitHub Copilot Pricing](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/github-copilot-pricing.png)

## Visual Studio versus VS Code

As mentioned earlier, the investigation was conducted in Visual Studio Code, primarily. However, I did conduct some testing on the same code in Visual Studio Professional 2022 to perform some comparisons. 

Here are my discoveries:

1. I encountered fewer code completions and they were less accurate than Visual Studio Code and in some cases the standard Visual Studio IntelliCode completions.
2. The suggestions are not *inline* as they are shown in a separate GitHub Copilot tab instead of overlaying on the class/file window that is being worked on. As seen in the examples above, you can open GitHub Copilot directly inline when using Visual Studio Code or highlight the lines to use, narrowing the context.
3. Visual Studio Code has a dedicated Chat window to discuss more generic questions or reference the entire codebase which is useful at the inception of a project to help get started on a feature/bug fix.

These were a few of the drawbacks I discovered while using Visual Studio as opposed to Visual Studio code. It appears the community agrees, judging by the disparity in rating and downloads for VS and VS Code.

#### Visual Studio GitHub Copilot Extension
![Visual Studio Bad Reviews](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/vs-bad-reviews.png)

#### Visual Studio Code GitHub Copilot Extension
![Visual Studio Code Good Reviews](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/vs-code-good-reviews.png)

## Conclusions

I found Copilot's suggestions and completions particularly useful when writing YAML for pipelines and Infrastructure-as-Code (IaC). Although, I only scratched the surface of Copilot's strengths and weaknesses during my 30 day free-trial. Good developers are inquisitive by nature so I'm certain many better applications are being discovered and documented.

In my eyes, AI is not a threat to the jobs of Software Engineers. It's purely a tool that, when used correctly, can increase the efficiency of certain day-to-day tasks. There are many stages of the Software Development lifecycle which simply cannot be completed by AI (at the moment) and I think the main one is around client interaction. When AI can understand what the client/product owner wants, break this down into requirements and prioritise it will be a different story. 

AI *today* resembles a headless chicken, moving quickly and sporadically without a clear direction. It comes into it's own when provided with precise context, good examples and well-thought-out prompts, gaining direction and purpose, similar to the chicken finding it's head. It will not be long until this bridge is gapped, however.

On the whole, I believe that GitHub Copilot is something every developer could find benefits from using and its cost are justifiable. All developer teams should consider GitHub Copilot and unless you are working on a system to handle state secrets the Business plan has you covered. GitHub claims a 55% improvement in coding speeds when using Copilot, even if the reality was 10-15% this is a considerable improvement in efficiency for busy developers, resulting in higher overall team productivity. Ultimately, it depends on businesses' risk tolerance versus appetite for innovation as to its adoption, but with the right measures and risk-mitigations, it's a tool not to be ignored.

## Further Reading and Demonstration

During this investigation, most of the features were tested, however, while writing this article GitHub made a release for Copilot.

I highly recommend watching this GitHub demonstration [video](https://youtu.be/a2DDYMEPwbE?si=B-UY9uMTji0My3wd) as it shows Copilot in action and introduces the new changes such as the use of multi-models, codebase referencing and inline chat improvements.

Here are some other articles I read during my research, which you may also find interesting:

1. [5 Ways to Reduce GitHub Copilot Security and Legal Risks](https://fossa.com/blog/5-ways-to-reduce-github-copilot-security-and-legal-risks/)

2. [GitHub Copilot security concerns](https://vlad-rad.medium.com/github-copilot-security-conserns-d4209f0d5c28)

3. [Yes, GitHub's Copilot can Leak (Real) Secrets](https://blog.gitguardian.com/yes-github-copilot-can-leak-secrets/#:~:text=The%20study%20analyzed%20435%20code,of%20the%20programming%20language%20used.)

4. [About Copilot Individual Plan](https://docs.github.com/en/copilot/overview-of-github-copilot/about-github-copilot-individual)

5. [GitHub Copilot Chat now generally available for organizations and individuals](https://github.blog/2023-12-29-github-copilot-chat-now-generally-available-for-organizations-and-individuals/)