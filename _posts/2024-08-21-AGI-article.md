---
title: "Are you smarter than AI?"
date: 2024-08-21
author: "Frankie Clipsham"
---

## Introduction

_On today's episode of Are You Smarter Than a Large Language Model (LLM) we have **you** versus OpenAI's cutting edge GPT 4! Do you think you have what it takes to beat the 200+ billion parameter LLM that has been trained on the internet?_

![AI smarter](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/images/ai-smarter.jpg)

I'm going to tell you why you have a much better chance than you may think, and while these models may have vast amounts of data and knowledge at their disposal, they lack characteristics uniquely human that no algorithm can mimic.

In my last post I concluded that AI is not a threat to the jobs of Software Engineers (SWE). Coming from a SWE this may seem biased, so it would only be right to delve more deeply into this topic to discuss where AI is now and why (_I believe_) AI won't take your job anytime soon. Stay tuned as I'll be touching on the concept of Artificial General Intelligence (AGI), what this means, how close we are to it and its relevance to the future of Software Development. I'll also be addressing the hype around AI and why, all too often, we're seeing these inflated capabilities and pipe dreams rather than candour and reality.

## What is Artificial General Intelligence (AGI)?

The field of Artificial Intelligence (AI) has been around since the 50s so the concept of measuring the intelligence of AI is nothing new [[1]](#sources). One of the first tests to measure computer intelligence was from Alan Turing who proposed the 'Turing Test'. An AI would pass if it's responses to questions were indistinct from that of a human, regardless of their correctness. It feels like we are here with the most advanced Large Language Models (LLM) such as GPT-4o, but this isn't the point. Many consider the Turing test to be insufficient in measuring intelligence as it doesn't account for any concept of a "mind" or "consciousness". This test only measures one aspect of intelligence that a narrow AI\*\* designed for natural language conversation, such as GPT-4o, is inherently good at.

A huge milestone, that many speculate on, is Artificial General Intelligence (AGI). AGI is the crown-jewel of AI research, but a hot topic for many in this community due to it's ethical concerns. **AGI is the concept of an AI that matches or even exceeds human intelligence and possesses 'human' features** such as:

- Adapting to problems it was not prepared for.
- Succeeding in a variety of different contexts and environments.
- Generalising knowledge gained to transfer between problems or contexts.

These are just a small subset of the capabilities we, as humans, possess that enabled our species to succeed. The most advanced Artificial Intelligence models do not thrive in problems they were not specifically trained on.

\*\*Narrow AI: A system that carries out specific "intelligent" behaviours in specific contexts [[2]](#sources)

## Will we see AGI?

As mentioned, AGI is a hot topic rife with hype and speculation. 
Elon Musk claims that we will see AGI next year and some form of Artificial Super Intelligence (ASI) by 2029.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">AI will probably be smarter than any single human next year. By 2029, AI is probably smarter than all humans combined. <a href="https://t.co/RO3g2OCk9x">https://t.co/RO3g2OCk9x</a></p>&mdash; Elon Musk (@elonmusk) <a href="https://twitter.com/elonmusk/status/1767738797276451090?ref_src=twsrc%5Etfw">March 13, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I think these are wildly optimistic claims given the current state of artificial intelligence research and development;
despite significant progress, many technical and ethical hurdles remain, and the substitution of Software Developers by AI will only become possible come AGI, which I think we're very far away from.

Even if AGI was possible, in theory, there is still the practical reality that an AGI could be too expensive to train and deploy. The current latest models have over 100 billion parameters and take months to train on the latest GPUs. An AGI would have significantly higher compute requirements to that of the latest narrow AIs which would require huge advancements in hardware and model efficiency before becoming feasible for wide-spread use.

Some theorise that AGI will not even be possible on the current trend of Large Language Models that just predict the next word in a sentence. After all the world is not simply made up of words, there are fundamental mathematical and physical concepts that should be at the core of this generally intelligent model [[4]](#sources).

## The Hype

'AI' has been the talk of the tech since its potential was widely realised with the release of GPT 3.5 and ChatGPT in November 2022. During this initial hype we saw many companies scramble to implement their own AI offerings. This led to some companies demonstrating their implementation of AI with best case examples in favourable environments and even faking capabilities. This practice has been coined 'AI Washing' where companies are overhyping their AI further than their capabilities to attract investment and, ultimately, mislead consumers. We've seen this from demos such as Devin AI and Google's Gemini [[5]](#sources)[[6]](#sources).

There are huge market incentives in AI and it's a buzzword that gets lots attention from investors and consumers alike. This has lead to explosions in profit and stock prices for microchip companies such as NVidia and Supermicro, due to huge compute requirements to train and deploy all these models, that are only getting bigger. I think we're in the AI bubble at the moment and it's not popping anytime soon. These companies are only going to keep growing as others race to develop, train and deploy the latest and greatest models.

On the other hand, are the research academics and lawmakers. They are playing catch up with the AI companies to explore the possible implications of the AI boom to ensure proper safeguarding and regulations are in place to protect against copyright, scams, disinformation and abuse.

## Devs Are Expensive, So Are Mistakes...

I believe companies see AI as a way to slim down their work force and increase profits as with most companies' payroll is the highest expense. If an AGI was widely available, adoption in Software would most likely start with junior developers being let go and seniors guiding the AI. To me this raises issues down the line as without a pipeline of junior developers gaining experience the pool of senior developers would shrink, leading to a skills gap and lack of innovation. This could end in disastrous spiral if there was an over-dependence on AI while problem-solving and critical thinking skills atrophy among human developers.

Software bugs can be costly, especially in mission-critical or low-level systems. A recent example is the CrowdStrike Falcon update, which caused the blue screen of death on over 8 million Windows machines due to a logic error. However, the bigger issue is the process, not the developer. Robust QA, staged rollouts, and disaster recovery plans are essential for updates affecting millions of machines, especially at the kernel level. These processes should be guided by experienced teams, as the reputational risks are too great to have AI involved with. 

There are some ethical concerns that arise when the output of AI is given so much importance. Who is responsible if the AI makes mistakes? The person prompting the AI? The company who developed the AI? The company that adopted AI into their development process? It's very risky putting your companies' reputation in the hands of an AI that has the potential to hallucinate [[7]](#sources) or confidently produce erroneous responses.

In a case from earlier this year a ChatBot on Air Canada's website offered a ticket discount to a customer due to a bereavement. This was not actually in their policy. The customer sued Air Canada and the court ruled that Air Canada were responsible of "ensuring it's ChatBot was accurate". This case sets a precedent that the company deploying an implementation of AI is liable for any hallucinations it outputs [[8]](#sources).

We're only going to see more cases like this as AI adoption increases. Hence, there should always be serious consideration of the potential impact incorrect responses would result in, especially if the implementation is publicly facing.

There's other research to suggest developers using AI are producing worse code that without as shown in the number of comments on pull requests for the same quantity of changes. This might be a topic for another blog, but it's worth considering: if AI struggles to succeed in the core areas where it can make an impact (coding), then Artificially Intelligent Software Engineers aren't coming anytime soon since coding is only one aspect of a Software Engineer's role.

## Conclusion

Honestly, I think AI is great, it's going to be the most influential piece of technology since the internet and there is huge potential, but it's not taking Software jobs anytime soon, it's creating them, if any. Personally, I've found real benefits from using AI to improve my day-to-day efficiency at work as shown in my last blog on GitHub Copilot. It's disrupting many industries, and the competition among AI companies is fuelling innovation, enabling cutting-edge technology right at our fingertips. It's an exciting time to be in the tech industry, but hype is going nowhere, with each release of a new model or implementation only fuelling further excitement. So, all I'll suggest is taking a pinch (_bucket_) of salt with each new demo from the latest AI startup as the product may be much less capable than they insist.

![Never celebrate too early](https://raw.githubusercontent.com/frank-64/ToBeFrank/master/assets/gif/winner_05.gif)

The race toward AGI has also begun, but the starting gun has barely sounded, and it's more of a marathon than a sprint. There are still some huge technical and ethical hurdles to overcome before are close to the finish line, but I think we'll see many, especially those with a financial incentive like Elon, celebrating too early and claiming it's a reality.

## Sources
1. _[The History of Artificial Intelligence](https://sitn.hms.harvard.edu/flash/2017/history-artificial-intelligence/) - Rockwell, A. 2017_
2. _[The singularity is near: When humans transcend biology](https://en.wikipedia.org/wiki/The_Singularity_Is_Near) - Kurzweil, R. 2005_
1. _[Artificial General Intelligence:
Concept, State of the Art, and Future Prospects](https://intapi.sciendo.com/pdf/10.2478/jagi-2014-0001) - Goertzel, B. 2014_ - A paper on AGI that assisted with the [What is AGI?](#what-is-artificial-general-intelligence-agi) section. A huge topic as you can see by the size of the paper. The opening pages were really useful for definitions and sources, but the later sections go into immense depth about measuring intelligence, attempting to characterise AGI, comparing AGI to the human mind and the psychological point of view. A good amount going over my head.
2. _[Why LLMs Will Never Be AGI](https://chrisfrewin.medium.com/why-llms-will-never-be-agi-70335d452bd7#:~:text=Intelligence%20Alone%20Cannot%20Lead%20To%20AGI%20or%20ASI&text=An%20LLM%20trained%20even%20on,hasn't%20been%20done%20yet!) - Frewin, C. 2024_ - Really interesting article that does a great job at discussing the gaps between current LLMs and AGI that I only touch on.
4. _[Debunking Devin: "First AI Software Engineer" Upwork lie exposed](https://www.youtube.com/watch?v=tNmgmwEtoWE) - Internet of Bugs_ - I really like this guy's channel, he's a been a software professional for 35 years and does some great deep dives into the AI hype and how AI might affect software development. He's an experienced guy with some good takes that are well backed up by sources, some helping to form my own opinions in this article. I'd highly recommend a watch.
4. _[Don't be fooled: Google faked its Gemini AI voice demo](https://www.theregister.com/2023/12/11/ai_in_brief/) - The Register (Quach, K. 2023)_
5. _[What are AI hallucinations?](https://www.ibm.com/topics/ai-hallucinations) - IBM_
3. _[Airline held liable for its chatbot giving passenger bad advice - what this means for travellers](https://www.bbc.com/travel/article/20240222-air-canada-chatbot-misinformation-what-travellers-should-know) - BBC Travel_


