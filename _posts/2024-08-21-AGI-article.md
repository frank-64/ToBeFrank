---
title: "Is AI smarter than you?"
date: 2024-08-21
author: "Frankie Clipsham"
---

## Introduction
On today's episode of are you smarter than a Large Language Model (LLM) we have **you** versus OpenAI's cutting edge GPT 4! Do you think you have what it takes to beat the 200+ billion parameter LLM that has a training data set the size of the internet?

![AI smarter](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/ai-smarter.jpg)

I'm going to tell you why you have a much better chance than you may think and while these models have vast amounts of data and knowledge at their disposal they lack characteristics uniquely human that no algorithm can mimic.

During my last blog post I concluded that AI is not a threat to the jobs of Software Engineers (SWE). As a SWE this may seem biased, so I have decided to delve more deeply into this topic to discuss where AI is now and why (_I believe_) AI won't take your job anytime soon. During this article I will touch on the concept of Artificial General Intelligence (AGI), what this means, how close we are to it and its relevance to the future of Software Development. I'll also talking about the hype around AI and why, all too often, we're seeing these inflated capabilities and pipe dreams rather than candour and reality.

## What is Artificial General Intelligence (AGI)?

The field of Artificial Intelligence (AI) has been around since the 60s [[Rockwell, A. 2017]](https://sitn.hms.harvard.edu/flash/2017/history-artificial-intelligence/) so the concept of measuring the intelligence of AI is nothing new. One of the first tests to measure computer intelligence was from Alan Turing who proposed the 'Turing Test'. An AI would pass if it's responses to questions were indistinct from that of a human, regardless of their correctness. It feels like we are here with the most advanced Large Language Models (LLM) such as GPT-4o, but this isn't the point. Many consider the Turing test to be insufficient in measuring intelligence as it doesn't account for any concept of a "mind" or "consciousness". This test only measures one aspect of intelligence that a narrow AI\*\* designed for natural language conversation, such as GPT-4o, is inherently good at.

A huge milestone, that many speculate on, is Artificial General Intelligence (AGI). AGI is the crown-jewel of AI research, but a hot topic for many in this community due to it's ethical concerns. **AGI is the concept of an AI that matches or even exceeds human intelligence and possesses 'human' features** such as:

- Adapting to problems it was not prepared for.
- Succeeding in a variety of different contexts and environments.
- Generalising knowledge gained to transfer between problems or contexts.

These are just a small subset of the capabilities we, as humans, possess that enabled our species to succeed. The most advanced Artificial Intelligence models do not thrive in problems they were not specifically trained on.

\*\*Narrow AI: A system that carries out specific "intelligent" behaviours in specific contexts [[Kurzweil, R. 2005]]()

## Will we see AGI?

As mentioned, AGI is a hot topic rife with hype and speculation. 
Elon Musk claims that we will see AGI next year and some form of Artificial Super Intelligence (ASI) by 2029.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">AI will probably be smarter than any single human next year. By 2029, AI is probably smarter than all humans combined. <a href="https://t.co/RO3g2OCk9x">https://t.co/RO3g2OCk9x</a></p>&mdash; Elon Musk (@elonmusk) <a href="https://twitter.com/elonmusk/status/1767738797276451090?ref_src=twsrc%5Etfw">March 13, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I think these are wildly optimistic claims given the current state of artificial intelligence research and development;
despite significant progress, many technical and ethical hurdles remain, and the substitution of Software Developers by AI will only become possible come AGI, which I think we're very far away from.

Even if AGI was possible in theory there is still the practical reality that an AGI could be too expensive to train and deploy. The current latest models have over 100 billion parameters and take months to train on the latest GPUs. An AGI would have significantly higher compute requirements to that of the latest narrow AIs which would require huge advancements in hardware and model efficiency before becoming feasible for wide-spread use.

## The Hype

'AI' has been the talk of the tech since it's potential was widely realised with the release of GPT 3.5 and ChatGPT in November 2022. During this initial hype we saw many companies scramble to implement their own AI offerings. This led to some companies demonstrating their implementation of AI with best case examples in favourable environments and even faking capabilities. This practice has been coined 'AI Washing' where companies are overhyping their AI further than their capabilities to attract investment and, ultimately, mislead consumers. We've seen this from demos such as [Devin AI](https://youtu.be/tNmgmwEtoWE) and [Google's Gemini](https://www.theregister.com/2023/12/11/ai_in_brief/).

There are huge market incentives in AI and it's a buzzword that gets lots attention from investors and consumers alike. This has lead to explosions in profit and stock prices for microchip companies such as NVidia and Supermicro, due to huge compute requirements to train and deploy/run all these models, that are only getting bigger. I think we're definitely in the AI bubble at the moment and it's not popping anytime soon. These companies are only going to keep growing as others race to develop, train and deploy the latest and greatest models.

On the other hand, are the research academics and lawmakers exploring the possibilities and implications to ensure the safeguarding of humans.

## Devs Are Expensive, So Are Mistakes...

I believe companies see AI as a way to slim down their work force and increase profits as with most companies payroll is the highest expense. If an AGI was widely available, adoption in Software would most likely start with junior developers being let go and seniors guiding the AI. To me this raises issues down the line as without a pipeline of junior developers gaining experience the pool of senior developers would shrink, leading to a skills gap and lack of innovation. This could end in disastrous spiral if their was an over-dependence on AI while problem-solving and critical thinking skills atrophy among human developers.

Bugs in software can be very costly, especially in low-level or mission critical systems. Take the recent CrowdStrike Falcon update that caused huge global impact when over 8 million Windows machines experienced the blue screen of death. 
Although this was a result of a logic error introduced by the update, the main problem, for me, lies with process, not the developer. There needs to be much more robust QA, staged rollouts and disaster recovery plans for a change that gets deployed directly to millions of Windows machines and runs as low-level as the kernel device drivers. The processes should be defined at the organisational or departmental level with experienced guidance to ensure reliability and safety for the user. These are human decisions that should not be decided by AI as there is huge reputational impact at risk. 

There are some ethical concerns that arise when the output of AI is given so much importance. Who is responsible if the AI makes mistakes? The person prompting the AI? The company who developed the AI? The company that adopted AI into their development process? It's very risky putting your companies reputation in the hands of an AI that has the potential to [hallucinate](https://www.ibm.com/topics/ai-hallucinations) or confidently produce erroneous responses.

In a case from earlier this year a ChatBot on Air Canada's website offered a ticket discount to a customer due to a bereavement. This was not actually in their policy. The customer sued Air Canada and the court ruled that Air Canada were responsible of "ensuring it's ChatBot was accurate". This case sets a precedent that the company deploying an implementation of AI is liable for any hallucinations it outputs.

We're only going to see more cases like this as AI adoption increases. Hence, there should always be serious consideration of the potential impact incorrect responses would result in, especially if the implementation is publicly facing.

## Back To Reality

Honestly, I think AI is great, it's going to be the most influential piece of technology since the internet and there is huge potential. The hype is going nowhere, with each release of a new model or implementation using 

- Race to AGI
- Lots of claims of AGI before we reach it
- Can't forget the impact on humans and ethical issues
## Sources
