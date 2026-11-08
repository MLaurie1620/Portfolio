# FundTrace — AI Audit Triage

**Workplace · Applied AI · Sole creator and project owner**

An AI-assisted workflow that shortlists vendor-funding email conversations and
quotes supporting evidence for auditor review.

I created and own the end-to-end workflow: archive processing, AI scoring,
evidence output, and evaluation.

## Workflow

The pipeline removes exact duplicates, groups replies into conversations, and
uses AI to score each exchange. Shortlisted items include a summary and evidence
quotations. Auditors make the final decision, and corrections are retained.

## Evaluation and results

Development and testing covered seven vendor archives. Separate scorer,
reviewer, and optimizer model calls examined mistakes and proposed instruction
changes. Experiments used vendor-level separation and compared changes against
the deployed baseline.

The detailed October 2026 evaluation reports this single-vendor benchmark:

| Measure | Result |
|---|---|
| Conversations evaluated | 1,498 |
| Shortlisted for review | 506 (34%) |
| Relevant conversations found | 162 of 198 (82% recall) |
| Relevant conversations missed | 36 |

Providing full email text increased recall to 95% while flagging 49% of
conversations. Larger instruction sets mainly shifted the recall/workload
balance, without a clear overall improvement.

These figures describe one vendor benchmark, later reused for development.
Fresh vendor testing is needed to assess broader performance, and review-time
savings remain illustrative.

## Engineering lessons

- Measure the version people actually receive, with a baseline in every experiment.
- Track missed evidence alongside the review workload created.
- Record reviewer failures explicitly and preserve zero scores correctly.
- Separate ambiguous labels, missing context, and model error before optimizing.

The project demonstrates workflow automation, AI orchestration, evidence
traceability, evaluation design, failure observability, and communication of
operational tradeoffs.

[View the case study →](https://mlaurie1620.github.io/Portfolio/fundtrace.html)
