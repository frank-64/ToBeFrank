# An investigation into the effectiveness of the AI pair programming tool GitHub Copilot
## Introduction
In my last blog, I spoke about not knowing the capability of GitHub Copilot. I decided to change by signing up for the 30-day free trial and I began my investigation. I set out to determine the effectiveness, accuracy and security of GitHub Copilot as a tool for programmers. The end goal being a consideration of whether the costs involved are justified.

For context, GitHub Copilot is an AI powered assistant specifically trained to assist with programming. It can be installed as an extension in your programming environment (IDE) of choice to give code completions, code explanations or 
offer code fixes. This investigations primarily used the Visual Studio Code IDE for reasons explained later.

## First Impressions
/fix is good
highlight to select specific context
Inline makes it so much easier
Ctrl+I
/explain good for getting to grips with new codebases

## Examples
The three features I found most useful from GitHub Copilot during my investigation were code completions, suggestions and explanations. Below I will provide some examples, which I believe, detail the necessicity for Copilot as a tool for programmers.

### Code Completion

#### 1. Code completion for an Azure Pipelines `docker login` task

This completion was appreciated as my next step would have been including the login step. The completion saved me time and managed to include the valid connection variable name from the context of the current file.

![Pipeline code completion 1](/assets/images/code%20completion%20pipelines%201.png)

#### 2. App settings definition assisted with code completion
 In this example I was manually defining my app's settings in a pipeline and it managed to perfectly suggest the next three settings which I was about to type. It used the context from the first variable `DOCKER_REGISTRY_SERVER_PASSWORD` to determine the next settings required and then matched my variable format. This is a great example of the time saving benefit of GitHub Copilot as the manual process is very specific and time consuming.

![App settings code completion 1](/assets/images/app%20settings%202.png)
### Code Suggestions

#### 1. App settings code suggestion from prompt
This example is very similar to the one above, however, I prompted Copilot with the list of known app settings names. It then added them to the existing list of app settings and matched the correct format e.g. `APP_SETTING_1` = `-APP_SETTING_1 $(APP_SETTING_1)`. This saved me a great deal of time typing out each specific app setting.
![App settings code completion 2](/assets/images/app%20settings%201.png)

#### 2. Accurate code suggestion from a very simple prompt
Here I was trying to define an Azure Pipielines stage with multiple dependencies. The previous build failed stating an error in this line. I simply prompted Copilot with `depends on multiple` and it quickly suggested a re-format which resulted in a successful pipeline run.

![Pipeline code suggestion depends on](/assets/images/depends%20on%20multiple.png)

### Code Explanation
#### 1. Explanation of an code in an unfamiliar code base and language
This example shows an inline chat I started to determine if a message could still be added to an array if it was a constant or `const` definition. The code-base was not written by me and this was the first time viewing it. I am not a TypeScript pro so the idea of a constant being updated surprised me. Thankfully, Copilot provided me a clear explanation in to why the code works fine. 
![Constant explain](/assets//images/constant%20explain.png)

#### 2. 
![Pipelines explain](/assets/images/pipelines%20explain.png)

### Chat GPT vs GitHub Copilot
I decided to compare ChatGPT and GitHub Copilot by asking the same question: How do I set the admin user property on an Azure Container Registry in a Bicep template? I provided ChatGPT the existing resource definition for context. As you can see below, ChatGPT was completely off as it was attempting to use Role-based access control assignments, but Copilot suggested the correct addition and saved me some time researching.

![GPT Code suggestions](/assets/images/admin%20user%20chatgpt.png)

![Copilot Code suggestions](/assets/images/admin%20user%20copilot.png)

## Security Concerns
Research and reference privacy policies 
## Conclusions

As mentioned earlier, the investigation was conducted in Visual Studio Code, primarily. However, I did conduct some testing on the same code in Visual Studio Professional 2022 in order to perform some comparisons. Here are my discoveries:

1. I encountered fewer code completions and they were less accurate than Visual Studio Code and in some cases the standard Visual Studio code completions.
2. The suggestions are not *inline* as they are shown in a separate GitHub Copilot tab instead of overlaying on the class/file window that is being worked on. As seen in the examples above, you can open GitHub Copilot directly inline when using Visual Studio Code or highlight the lines to use, narrowing the context.
3. Visual Studio Code has a dedicated Chat window to discuss more generic questions which is useful at the inception of a project to help get started.

These were a few of the drawbacks I discovered while using Visual Studio as opposed to Visual Studio code. It appears the community agrees, judging by the disparity in reviews and downloads for VS and VS Code.

### Visual Studio GitHub Copilot Extension
![Visual Studio Bad Reviews](/assets/images/vs-bad-reviews.png)

### Visual Studio Code GitHub Copilot Extension
![Visual Studio Code Good Reviews](/assets/images/vs-code-good-reviews.png)

Pitch to my company why we should/shouldn't use it

In my eyes, I do not see AI as a threat to the jobs of Software Engineers. It's purely a tool that, when used correctly, can increase the efficiency of certain day-to-day tasks. There are many stages of the Software Development lifecycle which simply cannot be completed by an AI (at the moment) and the main ones are centred on determining what the client/product owner wants then subsequently prioritising and breaking down these requirements. You could say that AI is a headless chicken that regenerates its head upon proper direction and relevant context from the prompter.

Copilot has a `/explain` feature that will use the context of the highlighted code and the user's prompt to succinctly detail a section of code. This could be particularly beneficial for junior programmers or anyone attempting to get to grips with a new code base in order to actually understand the code. Furthermore, programmers working with code not written in their primary language could make use of this feature to improve their confidence and help with the syntactical nuances. 

There is also a `/doc` feature that can be used to to document or add comments to old/unsupported code.

These features would benefit senior programmers as there would be more support for juniors. This would result in less time spent on calls explaining code, debugging a missing semi-colon or resolving other syntactic errors. The code quality should still remain relatively high as Copilot is aware of the code-base as context so it makes attempts to follow coding standards set when making suggestions.

Inline makes it so much easier and convinient with context
Ctrl+I
/fix 
Really good for pipeline creation, bicep, IaC etc