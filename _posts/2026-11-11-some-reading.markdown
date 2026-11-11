---
layout: post
title:  Reading up on a lot of history of formalisation and starting to read metaprogramming for Lean
date:   2026-11-11
categories: General weekly review
---

So the past weeks I have been reading some more about metaprogramming but also the history of formalisation software. This somehow is a lot more relevant this thesis around compared to the previous thesis. So let's just get down to the spark notes version of what Lawrence Paulson has written in the following four articles: [The one with most history](https://lawrencecpaulson.github.io/2025/12/05/History_of_Proof_Assistants.html), [Hardware verification](//lawrencecpaulson.github.io/2023/01/04/Hardware_Verification.html), [His omission of Mizar in the history](https://lawrencecpaulson.github.io/2026/05/07/Mizar.html) and [Sledgehammer in Isabelle](https://lawrencecpaulson.github.io/2022/04/13/Sledgehammer.html). So let's just start blabbering on.

Before any formal verification language using the calculus of inductive constructions. There was one language in 1967 called Automath: This was the first formal verification language in the world[^1](Citation needed) and it was written here in the Netherlands by de Bruijn (always love a little bit of chauvinism). 

Over time a few others started appearing over time and some stuff started to be formalised like the definition of the natural numbers, but apart from that it was. Anyway apart from it starting the idea of formal verifiction languages not much seemed to happen yet.

Later on somewhere past 1985 we finally see the use of the calculus of inductive constructions appear which is already a big improvement as induction is now supported natively. However it still took some time until we started seeing actual applications.

At the same time on the other side of the iron curtain we see that in Poland the language Mizar was invented. Although I wish to say more about the language's development it seems to be a lot harder to research more about. I feel like it is worth noting though that Mizar also had a library that one could say is kinda a predecessor of Mathlib: The Mizar Mathematics Library. So it seems interesting that for some reason Lean one out.

Now between 1995 and 2005 we start getting into the first "useful" application of formal verification languages: Formally verified hardware. This was apparently a lot easier than formally verified code, which is interesting as generally the real-world is only messier. The idea of formally verified hardware is to do three things:
1. Rewrite the circuit specifications into mathematics;
2. Formalise the assembly instruction set into the formal language;
3. Proof that the assembly instructions indeed give the mathematical output.

Notably for defining the circuit specifications apparently inputs and outputs of the circuit were completely removed just like tensor networks do. Which is rather interesting if you ask me.

In the same period there were 2 other notable mathematical statements/proofs being formalised: Some of mathematics and the four colour theorem. Especially the four colour theorem is rather interesting. Before in order to ensure that one trusted the output of the code of the four colour theorem one needed to check all the 800 odd cases now one only needed to check the formalisation of the definition. It sadly didn't change that the proof is still rather gross, but hey at least checking correctness is less time consuming.

Then between 2005 and 2015 we finally see this niche hobby actually properly being taken up by some niche industry: We got a formally verified OS kernel, Compiler verification (which still is not completely secure, but a lot better) and also some actually interesting mathematics.

This basically brings us to present day with the breakthrough with Lean. It specifically all started with Mathlib; an ambitious project mostly lead by Kevin Buzzard, which started trying to formalise at least all of pure undergraduate mathematics. This kinda grew out of proportions and AI only made this worse. All culminating in Fermat's Last theorem finally being formalised in Lean this October.

_Just to see how crazy the growth is I made the following image during my Bachelor thesis:_

![Image showing the quick growth from Lean being barely no player at all to the frontrunner.]({{site.url}}/images/FreekWiedijk100problems.png)

There is only one small application I want to talk about that is kinda insane to me: The fact that a lot of the security of the Nitro Isolation Engine was formally verified for Amazon Web Services. This seems all to important with all the cybersecurity troubles that are occuring now thanks to AI.

Lastly I wanted to say that I started joining the metaprogramming cafe and also started reading some of it. But I definitely still have a lot to learn there.


