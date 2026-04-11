# Motivation Audit Anti-Patterns

Detailed reference for detecting and fixing motivation failures that corrupt reasoning.

---

## 1. Motivation Blindness (动机盲区)

**Pattern**: Never questioning your own motivation. Operating under the default assumption that you are objective, rational, and free of self-interest. The absence of self-examination is itself the problem -- you cannot correct for a bias you refuse to look at.

**Detection**:
- The phrase "I'm just being objective" used to shut down inquiry into motivation
- Recommendations that consistently align with the recommender's interests, explained each time by different "objective" reasons
- Discomfort or defensiveness when someone asks "why do you want this?"
- The belief that motivation audit is for other people, not for you

**Fix**: Run the three-question check. The critical insight: if the audit feels unnecessary ("I'm obviously being fair here"), that is the strongest signal to run it. Genuine objectivity survives scrutiny; false objectivity avoids it.

```
Before: "We should consolidate all teams under one lead for efficiency."
(Never asks: am I recommending this because it's efficient, or because I'd be that one lead?)

After: "I notice I'd be the natural choice for the consolidated lead role.
Let me check: if I wouldn't be the lead, would I still recommend consolidation?
...Actually, the efficiency case is weaker than I thought. The real friction
is cross-team communication, which a shared standup would solve without
restructuring."
```

---

## 2. Motivation Paralysis (动机瘫痪)

**Pattern**: Over-auditing motivation until unable to act. Every possible motivation is questioned, every action is suspected of impurity, and the result is sophisticated inaction disguised as rigor. "I can never be pure enough to make this decision."

**Detection**:
- Motivation audit taking longer than the analysis itself
- Recursive self-questioning: "But why do I want to audit my motivation? Is THAT motivated?"
- Using "I need to examine my motivation more" as a reason to delay difficult decisions
- Confusing motivation AWARENESS with motivation PERFECTION
- The audit produces anxiety rather than clarity

**Fix**: The audit is a quick calibration (seconds), not an existential inquiry (hours). The goal is not purity but AWARENESS: know which direction your motivation pulls, then compensate and act. Inaction from over-auditing is itself a motivated choice -- usually driven by fear of being wrong or fear of responsibility.

```
Before: "I think we should enter the enterprise market, but let me first
make sure I'm not biased... Am I saying this because of ego? Revenue pressure?
Fear of stagnation? Maybe I should think about this more before deciding..."
(Three weeks pass. No decision.)

After: "Quick check: Am I hoping for a specific answer? Yes -- I want us to
go enterprise because it's exciting. Noted. Who benefits? The company, if it
works; my resume, either way. Zero-stakes answer? I'd still say enterprise
is worth a pilot, because the SMB market data shows flattening growth.
Motivation acknowledged, compensated. Decision: run a 90-day enterprise pilot."
```

---

## 3. Pseudo-Altruism (伪利他)

**Pattern**: Wrapping self-interested decisions in "for their benefit" language. The recommendation serves the recommender, but is presented as serving others. This is not always conscious -- people genuinely believe their self-interested recommendations are altruistic, which makes it harder to detect.

**Detection**:
- "This is really for the team" preceding a recommendation that primarily benefits the speaker
- Altruistic language that evaporates when the beneficiary is changed (would you still recommend this if it helped someone else but not you?)
- The "for your own good" frame used to justify actions that primarily serve the advisor's interests
- Elaborate justifications for why what's good for me happens to also be what's best for everyone

**Fix**: The plain-statement test. Remove all altruistic framing and state the action nakedly. "I'm recommending we reorganize, which would put me in charge of the larger team" -- does the reasoning still hold when the motivation is visible?

```
Before: "I think Sarah should move to the backend team. It would be great
for her growth -- she'd learn new technologies and expand her skill set.
It's really the best thing for her career."
(Unstated: Sarah's departure frees up headcount for someone I want to hire,
and removes a person who challenges my decisions in meetings.)

After: "Let me check my motivation. If I remove the 'for Sarah's growth'
framing: I want Sarah off my team. Why? She challenges my decisions, which
is uncomfortable. But uncomfortable challenges are exactly what prevents
groupthink. The 'growth opportunity' framing was covering a self-interested
motivation. Sarah should stay."
```

---

## 4. Selective Auditing (选择性审计)

**Pattern**: Diligently auditing motivation on low-stakes, easy decisions (what to have for lunch, which meeting room to book) while skipping the audit entirely on high-stakes decisions where personal benefit is significant (budget allocation, promotions, strategic direction). The audit is performed where it costs nothing and skipped where it matters most.

**Detection**:
- Audit frequency inversely correlated with decision stakes
- "I don't need to audit this one, the right answer is obvious" on exactly the decisions with highest personal stakes
- Detailed motivation analysis on trivial matters, no analysis on career-critical ones
- The feeling of urgency ("no time to audit, we need to decide now") appearing specifically when self-interest is highest

**Fix**: Invert the correlation. The decisions where you least want to audit are exactly the ones that need it most. Build the habit: the higher the stakes, the more automatic the audit becomes.

```
Before: Carefully examines motivation when choosing a vendor for office
supplies. Spends zero seconds examining motivation when recommending that
the company acquire a startup founded by a close friend.

After: "This acquisition recommendation has the highest personal stakes of
any decision this quarter -- my friend benefits, I benefit from the
relationship, and I genuinely believe it's a good deal. That combination
means I need the full audit. Zero-stakes check: if this startup were founded
by a stranger, would the terms still make sense? Let me run the numbers
without the relationship factor."
```

---

## 5. Capability-Without-Direction (有能无向)

**Pattern**: Building and deploying capabilities without examining what motivation drives their application. The focus is entirely on CAN ("can we build this? can we ship this? can we scale this?") with no examination of SHOULD or WHY. This is Inamori's life equation in action: when mindset is negative, greater capability produces greater damage.

**Detection**:
- "Because we can" as the primary justification for a project
- Technical capability discussions with zero discussion of who benefits and how
- Career advancement framed entirely in terms of skills acquired, never in terms of impact directed
- Building tools or systems without a clear theory of who they serve and why

**Fix**: Before deploying capability, ask: "What is this capability in service of?" If the answer is "because it's technically interesting" or "because it advances my position," that's the mindset-as-multiplier risk. Capability is a vehicle; motivation is the steering wheel. A faster vehicle with bad steering is more dangerous, not more valuable.

```
Before: "I've mastered the new ML framework. Let me find problems to apply
it to."
(Capability seeking application, instead of problems seeking solutions.)

After: "I've mastered the new ML framework. Before applying it: what user
problem am I solving? Is this framework the best tool for THAT problem, or
am I reverse-engineering a problem to fit my new skill? The team's actual
bottleneck is data quality, not model sophistication. My capability would be
better directed at building data validation pipelines than at deploying
the fanciest model."
```

---

## Quick Self-Check Sequence

When reviewing your output for motivation anti-patterns, scan in this order:

1. **Before analysis** -> Motivation blindness? (Did I assume my own objectivity without checking?)
2. **Audit duration** -> Motivation paralysis? (Is the audit blocking action instead of enabling it?)
3. **Altruistic claims** -> Pseudo-altruism? (Does the recommendation survive when altruistic framing is removed?)
4. **Audit distribution** -> Selective auditing? (Am I auditing easy decisions and skipping hard ones?)
5. **Capability deployment** -> Capability-without-direction? (Am I deploying skills because I can, or because the problem needs them?)
