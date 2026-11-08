# Failure-first case study

A case study for a hiring manager or a deployment review. It earns trust by showing what went
wrong and what you changed, not by listing what went right. One page; numbers over adjectives.

```yaml
id: LOG-NN
title: one sentence, the question the work answers
summary: two sentences, what you built and what it measures
status: live | production | shipped | building   # "building" has no metrics
year: 2026
context: where it ran (anonymised: "tier-1 Italian enterprise", "open-source lab")
role: what you did yourself
shows: what it proves to someone hiring for this job
metrics:            # at most 3, each with its denominator and its caveat in the label
  - value: ""
    label: ""
stack: []
links: []           # code, results, a 2-minute video, the related case study
```

## Problem

Who loses what when this goes wrong? Name the failure that costs money (a wrong account looked
up, an emergency kept waiting), not the feature. Say what is already known: the benchmark or
paper closest to this, and how your work differs.

## Constraints

What you could not do, and how it bends the result: synthetic data, sample size, one model,
one run, no production traffic, legal limits. A reader should be able to guess the error bars
from this section alone.

## Architecture

One diagram in a code block, then a bullet per component. Pin versions (model, recogniser,
settings) and say what is cached so someone else can reproduce the numbers.

## What I did

Three to five bullets, each a finding a deployment team would act on, with its number. Lead with
the result, then the caveat. If an extractor or prompt was tuned on the data it is scored on,
say it here or in the next section.

## What broke

Your own mistakes: in the system, in the measurement, in the test data. Each one with how you
found it and what it changed in the numbers. This is the section people remember.

## What I would do differently

The one change you would make on day one, then the next steps in order of what they would teach.

---

Checklist before publishing:

- [ ] No employer, client or vendor names you are not allowed to use; ranges, not internal figures
- [ ] Every number traceable to a file or a run someone else can repeat
- [ ] Each metric has its denominator and its biggest caveat
- [ ] Known prior work cited accurately (scope, languages, date)
- [ ] Someone who did not build it has read it
