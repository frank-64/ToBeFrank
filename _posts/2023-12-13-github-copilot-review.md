## GitHub CoPilot Investigation - Crash Landing or Smooth Soaring?
### Introduction
In my last blog I spoke about not knowing the capability of GitHub Co-Pilot. I decided to change by signing up for the 30 day free trial and began my invesitgation. I set out to determine the effectiveness, accuracy and security of GitHub Co-Pilot as an assistant/tool for programming. The end goal being a justification 

For context, GitHub Co-Pilot is an AI powerered assistant specifically trained to assist with programming. It can be installed as an extension in your programming environment (IDE) of choice to give code completions, code explainations or 
offer code fixes. This invesitgation primarly used the Visual Studio Code IDE for reasons explained later.

### Prior Understanding
### First Impressions
/fix is good
highlight to select specific context
Inline makes it so much easier
Ctrl+I
/fix 
/explain good for getting to grips with new codebases


### Good Examples
Screenshots
Really good for pipeline creation, bicep, IaC etc
### Bad Examples
Screenshots
### Security Concerns
Research and reference privacy policies 
### Conclusions

As mentioned earlier, the investigation was conducted in Visual Studio Code, primarly. However, I did conduct some testing on the same code in Visual Studio Professional 2022 in order to perform some comparisons. Here's my discoveries:

1. I encountered fewer code completions and they were less accurate than Visual Studio Code and in some cases the standard Visual Studio code completions.
2. The suggestions are not *inline* as they are shown in a separate GitHub Co-Pilot tab instead of overlaying on the class/file window that is being worked on. As seen in the examples above, you can open GitHub Co-Pilot directly inline when using Visual Studio Code or highlight the lines to use, narrowing the context.
3. Visual Studio Code has a dedicated Chat window to discuss more generic questions which is really useful at the inception of a project to help get started.

These were a few of the drawbacks I discovered while using Visual Studio as opposed to Visual Studio code. It appears the community agrees, judging by the disparity in reviews and downloads for VS and VS Code.

#### Visual Studio GitHub Copilot Extension
![Visual Studio Bad Reviews](/assets/images/vs-bad-reviews.png)

#### Visual Studio Code GitHub Copilot Extension
![Visual Studio Code Good Reviews](/assets/images/vs-code-good-reviews.png)

Pitch to my company why we should/shouldn't use it

In my eyes I do not see AI as a threat to the jobs of Software Engineers. It's purely a tool, when used correctly, can increase the efficiency of certain day-to-day tasks. There are many stages of the Software Development lifecycle which simply cannot be completed by an AI (at the moment) and the main ones are centered determining what the client/product owner want and subsequently prioritising and breaking down these requirements. You could say that AI is a headless chicken that regains it's head upon direction and context from the prompter.

Good for juniors to get to grips with a code base
Good for seniors to reduce the amount of support required to a junior

Inline makes it so much easier
Ctrl+I
/fix 
/explain good for getting to grips with new codebases