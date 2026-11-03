# When the expert review and the usability test disagree

A bunch of you asked some version of this in your reflections (last week AND this week!):

> If an expert review flags a serious problem, but a small usability test shows nobody struggling with it, how should a team decide whether to fix it or gather more evidence?

This is a great question, and HCI folks have been arguing about it since at least the early 90s. So I did a bit of digging. Here's some notes on that (+ my own thinking on it) that might help.

## "Nobody struggled" with 5 people isn't the same as "no problem"

The rule of thumb that 5 users is enough comes from a specific calculation: 5 users will catch about 85% of the problems that affect roughly a third of your users ([MeasuringU](https://measuringu.com/five-users/)). That's great for finding the big, common problems. It's not so great for rarer ones.

Here's some quick math to get an intuition: if a problem trips up 10% of your users, the chance that at least one of your 5 participants runs into it is 1 − 0.9⁵, which is about 41%. So more often than not, you'd see nobody struggle, even though the problem is real! (You'd need something like 18 users to have an 85% chance of seeing it.)

So when the test comes back clean, the more accurate thing to say is "this probably doesn't affect most of our users", not "this isn't a problem".

This is a bit related to the idea of "statistical power" and sample size. The smaller the effect you're looking for, the bigger the sample you'll need to have a good shot at not making a "Type II" (there really was something going on, but I missed it) error. If you want to play with this, try this [interactive visualization of power and significance testing](https://rpsychologist.com/d3/NHST/): drag the sample size and effect size sliders and watch the Type II error area shrink and grow!

## But expert reviews DO raise false alarms

Heuristics are pretty good at generating candidate problems, and not so good at ruling out the ones that won't actually bother anyone. In one big study, Cockton and Woolrych had 99 people do heuristic evaluations of the same interface, then checked their predictions against user test data, and a lot of the predictions (they report about 65%!) never showed up ([Cockton & Woolrych 2001](https://researchportal.northumbria.ac.uk/en/publications/understanding-inspection-methods-lessons-from-an-assessment-of-he/)). And back in 1991, Jeffries and colleagues found that heuristic evaluation caught the most serious problems for the least effort, but also turned up a ton of low-priority stuff ([Jeffries et al. 1991](https://course.khoury.northeastern.edu/is4300sp13/ssl/articles/p119-jeffries.pdf)).

Jeff Sauro makes the counterpoint nicely: a problem the test didn't catch isn't automatically a false alarm. It might just be a less common, "long-tail" issue ([MeasuringU](https://measuringu.com/effective-he/)). And when people compare the two methods head to head, they tend to find fairly different sets of problems. So I think of the two methods as complementary, rather than one being the "check" on the other.

NOTE: this is basically why I've been nudging you to treat your expert review findings as hypotheses! And a small usability test is a pretty weak test of a hypothesis about a rare problem.

## So how do you decide?

There's no formula, but here are the questions I'd ask (this is my own synthesis of the stuff above, not one author's checklist):

1. Did the test actually give the problem a chance to show up? If none of your tasks went through that part of the interface, the test basically tells you nothing about it. (Go check your task list!)
2. How bad is it when it does happen? Nielsen's severity ratings combine how often a problem happens, how hard it is to get past, and whether it keeps coming back ([summary here](https://www.cs.princeton.edu/courses/archive/spring13/cos436/handouts/Heuristics_explained.pdf)). A rare problem that's catastrophic when it hits (e.g., someone loses their work, or gets locked out) can still be worth fixing.
3. Who wasn't in the room? Small samples miss whole groups of people. This is especially true for accessibility: if none of your 5 people use a screen reader, your test can't tell you anything about how it works with a screen reader ([MeasuringU](https://measuringu.com/severe-frequent/)). We'll dig into this a LOT in Weeks 10 and 11.
4. What does the fix cost, compared to what more evidence would cost? If the fix is cheap and low-risk, I'd often just fix it. That's the logic behind RITE (Rapid Iterative Testing and Evaluation), where teams change the design as soon as a problem and a fix are clear ([MeasuringU on RITE](https://measuringu.com/rite-method/)). If the fix is expensive or risky, that's when it's worth gathering more evidence first: more users, the RIGHT users, or a task designed specifically to poke at that part of the interface.

One more wrinkle: severity ratings themselves are noisy! Individual experts disagree quite a bit, so averaging a few people's ratings helps ([Herr et al. 2016](https://cml.hci.uni-bamberg.de/~gross/publ/chi16_herr_et_al_severity_rating_scales__proceedings.pdf)).

## If you want to go deeper

- MeasuringU's [How Effective are Heuristic Evaluations?](https://measuringu.com/effective-he/) is a short, readable take on the whole debate.
- [Why you only need to test with five users (explained)](https://measuringu.com/five-users/) walks through the math above.
- Cockton and Woolrych's [follow-up on "falsification testing"](https://core.ac.uk/download/41074723.pdf) is the classic version of the argument about whether these really are false alarms, if you want the deep cut :)
