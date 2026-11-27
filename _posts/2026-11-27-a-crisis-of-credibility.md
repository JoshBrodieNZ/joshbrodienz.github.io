---
layout: post
title: A Crisis of Credibility
description: An expanded version of my CHCon 2026 rant on AI, credibility, and the security industry's opt-out.
---

At CHCon 2026, I was invited on stage to give a brief rant about whatever was on my mind. I hadn't prepared anything, but I can't turn down an offer to be the centre of attention, so I took to the stage to share my reckons about everyone's favourite topic: AI. Based on the reception, it seems like I struck a chord. Or maybe a nerve? Either way, folk wanted a more fleshed-out version of these reckons to be made available, so that's what this is.
{: .preface}

This is not a piece of AI evangelism. The hype cycle has burned everybody's goodwill and trust and I'm not asking for it back. Having said that, I'm certain that our industry's failure to credibly adopt this technology, or even understand it, has conceded an advantage to attackers that is already causing harm we could have avoided. I'm a little bit cross about it.

Look, I get it. We're a suspicious and deeply cynical bunch. There are plenty of valid criticisms we can use to build a tempting off-ramp for non-participation.

We can easily dismiss the tech as fundamentally broken: a non-deterministic black box that hallucinates with absolute confidence. And if the technical flaws don't justify our distance, the moral ones will. It's often pointed out that the space is ethically compromised: built on a foundation of stolen data, an accelerant of environmental ruin, a mass-producer of high-fidelity disinformation and a weapon of corporate austerity designed to launder mass layoffs as "innovation".

I'm not going to argue against any of that. It's all close enough to the truth that nitpicking the nuance is a loser's game. We'll leave "well actually, per-inference energy cost is blah blah blah" to AI engagement farmers. Like every disruptive technology before it, society will inevitably pick this up and wield it to harm the exact same groups of people we always do. I just don't accept that this gets us out of doing the work. If anything, it makes the work more essential.

I'm not asking you to love AI. But if you aren't actively mastering it, you are forfeiting your credibility as a practitioner. Have we forgotten what hackers are for? We claimed ownership of understanding how systems really work under the hood. Builders and users can take advantage of the comfort of higher-level abstractions, but we know that the delta between a system's assumed behaviour and its true behaviour is exactly where the harms hide. We committed to living in that gap, exposing those failures, and mitigating them. We've actually been pretty well compensated for it.

The models don't always tell the truth. So what? The entire history of this discipline is one of building reliable systems out of profoundly unreliable parts. Our infrastructure has been failing constantly since the 1940s and we've been engineering around it ever since. Packets drop, so we retransmit. Bits flip, so we error-correct. Flight computers fail, so we run three variants and take the vote. The same techniques work on models: run several, make them critique each other, and take the consensus over any single answer. For the errors that persist, we do what we've always done with untrusted components: make sure that being wrong can't do intolerable damage. It's absurd to throw our hands up in the air and treat LLMs as a uniquely unsolvable problem instead of the next layer of chaos we need to constrain.

Nobody in this field has clean hands by the standard applied to AI. The computer runs on conflict minerals, the platforms people spend their days on are paid for by surveillance advertising and many of our most essential customers have their own skeletons in their closets. We secured all of it anyway, because people depended on it.

Why the sudden crisis of conscience? What property of agentic systems has made their adoption a bridge too far? Our job is to take powerful machines that society depends on, but which we must remain deeply suspicious of at all times, and ensure those machines operate close enough to the expectations of their users. We use those machines to achieve that aim, because there aren't any other tools at our disposal that let us deliver on our commitments.

AI is one more of those machines. It's being deployed into platforms real people rely on whether we take part or not, so refusing doesn't make our hands any cleaner. It just leaves those platforms without us. Our obligations outweigh our objections and, as ever, if we don't get on board we're going to be routed around. We simply have to get over it and get to work.

While we're sitting on the sidelines being smug about whether an LLM can count the 'r's in 'strawberry', the gap between the work we deliver and the work that's needed from us has grown.

Much of how we decide what matters rests on an estimate of how likely something is to be attacked, and most of those estimates have priced in how expensive an attacker's time was and how rare certain tiers of capability were. Both assumptions are failing. Agentic offensive frameworks are already putting runs on the board. These tools haven't yet removed the need for skill against a well-defended target, but most of your customers aren't well-defended. The mantra of Grok shills on LinkedIn is unfortunately not wrong: this is the least capable these frameworks are ever going to be.

Then there's the sheer volume. You've seen the graphs. Crime stonks are going up. Sure, confirmed exploitation is climbing much more slowly than disclosure, but it is climbing, and nobody can tell you in advance which few of this week's wave of CVEs will be used. 

And it isn't only attackers who have sped up. The businesses we work for are shipping faster with these same tools, which means more designs, more code and more change landing on the same number of security people. Processes and postures built for the tempo of yesteryear aren't going to scale by people working harder.

I'm going to pick on pentesting, because that's where my background is, and I'm downrange of any shot I take at it. 

A common objection in this domain is that the market isn't asking for agentic testing yet. We seem to have conveniently forgotten that the market never asked for pentesting, either. We invented it, convinced everyone they needed it, and got it written into the standards they answer to. And then, as a cheeky little prank amongst ourselves, we declined to meaningfully improve it for the next twenty-odd years apart from a handful of new vulnerability classes added to the OWASP Top Ten just to keep folk on their toes. Who was going to notice if we collected our stacks of cash while the relevance of the service drifted?

Reality is coming knocking now, and it's going to give the lie to the confidence we inspired. Cheaper attacks, rising CVE volumes and a faster attacker tempo are forcing organisations to confront whether the security services they've been buying were ever aimed at the threats they now face. When market demand emerges in response to this world of hurt, it won't give notice. Ask yourself now how much lead time you'll need to build the offering that answers it.

As a defender, does a report that tells me what a human being can find in a week actually give me any information that I can use to prioritise where I spend my attention?
{: .ask}

I think an honest case can still be made for what a week of a person's time is worth, and for where that value runs out. However, I'm sceptical that many of the people selling it could faithfully make that case to me.

The tools that would increase the value of tester time already exist, and plenty of providers still aren't using them. Either they're leaving findings on the table while I pay for the privilege, or they've taken their finger off the pulse of the field they're paid to understand.

Sometimes it's the client tying the tester's hands behind their back, with a contract that bans sending their data to a third-party model. That's a legitimate constraint. Open-weight models on your own hardware get some of the capability back, and what's left isn't a new kind of problem. It has always been on the testing firm to spell out how a client's restrictions limit what the test can tell them, the same as a narrow scope or a shortened testing window. If the client's restrictions stop them getting an effective test, that's a finding in its own right. Feel free to link them to this rant if they need a second opinion on how much that decision undermines their defences.

A cynical observer might note that much of this work is sold by the day, and tools that threaten to turn a week of findings into an afternoon are awkward news for an invoice built on the week. There's still plenty of human work that can be billed for. It's just different work, and you only find out what it is by picking up the tools.

Buyers who've noticed and gone looking elsewhere find a market full of AI testing tools built by people who discovered pentesting the same week they discovered AI, and plenty of them are rubbish. That's what happens when the people who know what good looks like refuse to build it.

It's not just pentesting. Defence has always been an economic argument. We spend what the risk justifies. But the collapse in what an attack costs changes the argument. If a shift on that scale has snuck up on you, at what point does the advice you're giving amount to malpractice? It's a question we'd be forced to answer if there were any meaningful professional standards we had to hold ourselves to.

We don't have the luxury of time to grapple with this. Our customers and our employers are already defending against a reality we haven't equipped them for.

When the attacker's capability compounds, there are only two ways to get ahead of it: start earlier, or improve faster. Starting earlier is off the table, so we have to improve faster. Most of the gains arrive after a stretch of unglamorous investment. A team that cautiously trials a chatbot for a quarter gets the frustrating part and stops before the payoff. A team that puts these tools into its daily work, and changes how that work gets done, reaches the payoff.

The galling thing is that when AI boosters first started their spiel, I set out to prove them wrong. I made a good-faith effort to actually put this technology to work, expecting to collect enough information to more credibly shut down vendors. I absolutely love to shut down vendors.

Imagine my chagrin when it performed so well that I had to rebuild basically every part of my day-to-day work around it. How fucking embarrassing. Triaging incidents, reviewing architecture, investigating potential attacks, auditing code: the robot had the audacity to excel at all of it while I was still looking for a reason to hate it. As a further indignity, it gave me back hours in my week to use on projects I had written off as impossible to get to.

I maintain that the ability of the technology to deliver is independent of the promises made by many of its proponents. It turns out they can be right and still be lying. However, letting their grift poison our read on reality is a hell of an own goal.

I'm not the only one this has happened to. There are people in this industry who've accepted the scale of the disruption but can't bring themselves to say so out loud, for fear of being associated with the wrong crowd. When we stay quiet, we hand the conversation to the grifters and the holdouts, and we leave anyone trying to use this stuff conscientiously thinking they're the only one.

Well, I'm **resentfully** on the hype train.
{: .kicker}

The obvious next question: what actually worked, and what does it take to get AI working for you? For that, you'll need my upcoming book, *Resentful Velocity: Ten Agentic Habits of Highly Cynical Hackers*. Nah, not really. I'll cover it properly in a second post, because it doesn't belong in the rant.
{: .coda}
