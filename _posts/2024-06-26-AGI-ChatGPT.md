---
title: "Is AI Smarter Than You?"
date: 2024-06-26
author: "Frankie Clipsham"
---

<!--
Things to mention:


 -->

## Introduction

In my last blog post I concluded that AI is not a threat to the jobs of Software Engineers (SWE). As a SWE this may seem biased, so I have decided to delve more deeply into this topic to discuss where AI is at the moment and why (_I believe_) AI won't take your job anytime soon . During this article I will touch on the concept of Artificial General Intelligence (AGI), what this means, how close we are to it and it's relevance to the future of Software Development. I'll also talking about the hype around AI and why, all too often, we're seeing these inflated capabilites and pipe dreams rather than candor and reality.

## What is Artificial General Intelligence (AGI)?

The field of Artificial Intelligence (AI) has been around since the 60s [[Rockwell, A. 2017]](https://sitn.hms.harvard.edu/flash/2017/history-artificial-intelligence/) so the concept of measuring the intelligence of AI is nothing new. One of the first tests to measure computer intelligence was from Alan Turing who proposed the 'Turing Test'. An AI would pass if it's responses to questions were indistinct from that of a human, regardless of their correctness. It feels like we are here with the most advanced Large Language Models (LLM) such as GPT-4o, but this isn't the point. Many consider the Turing test to be insufficient in measuring intelligence as it doesn't account for any concept of a "mind" or "conciousness". This test only measures one aspect of intelligence that a narrow AI\*\* designed for natural language conversation, such as GPT-4o, is inherently good at.

A huge milestone, that many speculate on, is Artificial General Intelligence (AGI). AGI is the crown-jewel of AI research, but a hot topic for many in this community due to it's ethical concerns. **AGI is the concept of an AI that matches or even exceeds human intelligence and possesses 'human' features** such as:

- Adapting to problems it was not prepared for.
- Succeeding in a variety of different contexts and environments.
- Generalising knowledge gained to transfer between problems or contexts.

These are just a small subset of the capabilities we, as humans, possess that enabled our species to succeed. The most advanced Artificial Intelligence models do not thrive in problems they were not specifically trained on.

\*\*Narrow AI: A system that carries out specific "intelligent" behaviours in specific contexts [[Kurzweil, R. 2005]]()

## Will we see AGI?

<!--
- Elon Musk's claims
- Academics claims (find X rant)
- If we see AGI then we may see a move towards AI replacing devs
- Very contested topic, so I won't draw too many conclusions. Many academic papers have defined what is required to consider this.
- There are challenges that AI cannot complete
- Surely the if AI can only complete a subset of challenges a human can complete than it cannot be considered generally intelligent
- The ability to adapt and infer with limited information and in different environments is what makes humans excel and where AI has shortfalls
- Compute and energy
 -->

As mentioned, AGI is a hot topic rife with hype and speculation. 
Elon Musk claims that we will see AGI next year and some form of Artificial Super Intelligence (ASI) by 2029.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">AI will probably be smarter than any single human next year. By 2029, AI is probably smarter than all humans combined. <a href="https://t.co/RO3g2OCk9x">https://t.co/RO3g2OCk9x</a></p>&mdash; Elon Musk (@elonmusk) <a href="https://twitter.com/elonmusk/status/1767738797276451090?ref_src=twsrc%5Etfw">March 13, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I think these are wildly optimistic claims given the current state of artificial intelligence research and development;
despite significant progress, many technical and ethical hurdles remain, and the substitution of Software Developers by AI will only become feasible come AGI, which I think we're very far away from.

Even if AGI was possible in theory there is still the practical reality that an AGI could be too expensive to train and deploy. The current latest models have over 100 billion parameters and take months to train on the latest GPUs. An AGI would have significantly higher compute requirements to that of the latest narrow AIs which would require huge advancements in hardware and model efficiency before becoming feasible for wide-spread use.

## The Hype

<!--
  - The market incentives to make AI profitiable and desire to hype as much as possible. Sometimes further than it's capabilities.
  - Faked demos with best case examples, AI in the best environments with the most favorable examples/test data
  - Devin AI
  - Gemini fakes
  - Rabbit R1
  - NVidia most valuable company in world
  - Overhype until people realise capabilities
  - Investors love the AI buzzword
  - Hire less workers
   -->
'AI' has been the talk of the tech since it's potential was widely realised with the release of GPT 3.5 and ChatGPT in November 2022. During this initial hype we saw many companies scramble to implement their own AI offerings. This lead to some companies demonstrating their implementation of AI with best case examples in favorable environments and even faking capabilities. This practice has been coined 'AI Washing' where companies are overhyping their AI further than their capabilities to attract investment and mislead consumers. We've seen this from demos such as [Devin AI](https://youtu.be/tNmgmwEtoWE) and [Google's Gemini](https://www.theregister.com/2023/12/11/ai_in_brief/).

There are huge market incentives in AI and it's a buzzword that gets lots attention from investors and consumers alike. This has lead to explosions in profit and stock prices for microchip companies such as NVidia and Supermicro, due to huge compute requirements to train and deploy/run all these models, that are only getting bigger. On the other hand are the research academics and lawmakers exploring the possibilities and implications to ensure the safeguarding of humans.

## Devs Are Expensive, So Are Mistakes...

<!--
- Candid about how good AI actually is
- Emotional aspect
- Middle management held accountable if they're the ones instructing AI
- Ethical issues with AGI
  -->
I believe companies see AI as a way to slim down their work force and increase profits as with most companies payroll is the highest expense. If an AGI was widely available, adoption in Software would most likely start with junior developers being let go and seniors guiding the AI. To me this raises issues down the line as without a pipeline of junior developers gaining experience the pool of senior developers would shrink, leading to a skills gap and lack of innovation. This could end in disasterous spiral if their was an over-dependence on AI while problem-solving and critical thinking skills atrophy amoung human developers.

Bugs in software can be very costly, especially in mission critical systems. Take the recent CrowdStrike Falcon update that caused huge global impact when over 8 million Windows machines experienced the blue screen of death. 
Although this was a result of a logic error introduced by the update, the main problem, for me, lies with process, not the developer. There needs to be much more robust QA, canary testing/phased rollout and better overall update management for a change that gets deployed directly to millions of Windows machines and runs as low-level as the device kernel drivers. AI cannot resolve these issues, they need to be defined by 

There are some ethical concerns that arise when the output of AI is given so much importance. Who is responsible if the AI makes mistakes? The person prompting the AI? The company who developed the AI? The company that adopted AI into their development process? It's very risky putting your companies repuation in the hands of an AI that has the potential to [hallucinate](https://www.ibm.com/topics/ai-hallucinations) or confidently produce erroneous responses.

In a case from earlier this year a ChatBot on Air Canada's website offered a ticket discount to a customer due to a bereavement. This was not actually in their policy. The customer sued Air Canada and the court ruled that Air Canada were responsible of "ensuring it's ChatBot was accurate". This case sets a precedent that the company deploying an implementation of AI is liable for any hallucinations it outputs.

We're only going to see more cases like this as AI adoption increases. Hence, there should always be serious consideration of the potential impact incorrect responses would result in, especially if the implementation is publically facing.

## Back To Reality

<!--
- I honestly think AI is great, I think it will be the biggest disruptor since the internet and has huge potential
- Save t
- Race to AGI
- Can't forget the impact on humans and ethical issues
- The hype is going nowhere
 -->

Honestly, I think AI is great, it's going to be the most influencial piece of technology since the internet and there is huge potential. The hype is going nowhere, with each release of a new model or implementation using 
## Sources
