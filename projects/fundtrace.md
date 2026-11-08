# FundTrace — AI Audit Triage

**Workplace · Applied AI · Sole creator and project owner**

I created and own a workflow that shortlists vendor-funding email conversations
and quotes supporting evidence for reviewer decisions.

## Workflow and evaluation

The pipeline removes duplicates, groups conversations, and uses AI to score the
material. Shortlisted items include a summary and evidence quotations. Reviewers
make the final decision, and corrections are retained.

Development used multiple vendor archives. Evaluation compares changes with the
deployed baseline and tracks both missed evidence and review workload.

## Reported benchmark

| Measure | Rounded result |
|---|---|
| Share of conversations shortlisted | **34%** |
| Share of relevant conversations captured | **82%** |
| Share of relevant conversations missed | **18%** |

These percentages describe a limited, single-vendor benchmark later reused for
development. They do not establish performance on new archives.

Providing more context improved recall while increasing the review workload.
Longer instructions mainly shifted that balance without a clear overall gain.

## Engineering lessons

- Compare changes with the version users receive.
- Measure missed evidence alongside the workload created.
- Make processing failures explicit and preserve valid scores correctly.
- Separate ambiguous labels, missing context, and model error before optimizing.

The project demonstrates workflow automation, AI orchestration, evidence
traceability, evaluation design, and communication of operational tradeoffs.

[View the case study →](https://mlaurie1620.github.io/Portfolio/fundtrace.html)
