---
layout: post
title:  Finally have some time to work
date:   2026-10-28
categories: General weekly review
---

# Update: 
I only just at the end reread the zulipthread of organising the community and thus only then read that apperently Alex Meiburg is planning on creating the overarching library: *QuantumLib*. Luckily they are planning on including the algolean library so it should be more than fine that I still spent time reading the library. I specifically missed [this](https://leanprover.zulipchat.com/#narrow/channel/508986-Quantum-information/topic/Quantum.20Computing.3A.20Organizing.20the.20community/near/624713301) message.

# The rest of the post:


It's the end of the first period and the start of the next period. Importantly I will always have a free Wednesday this period, and thus can finally start working on my thesis :). I have finally managed to work through algolean, which has pretty good documentation in the code. Generally it does seem to include almost everything we would already want for what my Master's thesis is going to be about. So it could very well be the case that I instead were to add some more support for working with the library for proving quantum algorithm specific statements.

To give an example on how unreasonable clean the implementation seems to be for implementing code see the following code snippet ripped straight from Shreyas Srinivas's poster about Algolean:

```lean
noncomputable def deutschJozsa (n : ℕ) :
    Prog (QuantumQuery n)
    (MState (Fin n → Fin 2)) := do
    let ρ ← applyHadamards (zeroRegisterState n)
    let ρ ← applyGate .oracle ρ
    applyHadamards ρ
```
Here the Deutsch Josza algorithm is pretty nicely implemented, thus easy to check for reviewers to check whether the implemented algorithm is the same as described in the corresponding paper.

Furthermore there are a bunch of advantages to just straight up using Algolean which I definitely won't be able to implement on my own, at least not for now:
- It supports complexity theory natively. Thus there would also be no reason for me to implement that as well.
- It allows for model reductions, thus also proving (in)equivalence for some different models (specifically allowing for QRAM model as an implementation as well, but then lifting a lot of the complexity theory from it by reductions). Normally any implementation I would make would by definition be of basically only one model, unless I were to be tempted to implement yet another model completely from scratch.

This also lead me into the direction of going ahead more and looking into metaprogramming in Lean as described in [The lean metaprogramming book](https://leanprover-community.github.io/lean4-metaprogramming-book/main/01_intro.html). So this might possible be a pivot, again, into what the main thesis is going to be about. This is very much fine for me as we are still very much in the setup phase instead of the proper working phase of the thesis.

Some more links I want to read more for myself are here below:
- [A (meta) explanation for the simp tactic](https://leanprover-community.github.io/blog/posts/simp-made-simple/)
- [A guide for writing effective simp procs](https://leanprover-community.github.io/blog/posts/simprocs-tutorial/)
- [A more formal setup of QM by general probabilistic theories](https://arxiv.org/abs/2103.07469)
