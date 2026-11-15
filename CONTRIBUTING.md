# Contributing

Thank you for helping keep this catalogue complete and accurate. This list is only useful if every entry can be trusted, so the bar is verification, not volume.

## Inclusion criteria

An entry belongs in the **independent variants** sections if it has:

1. Its own questions, corpus, modality or task format (not a subset or re-annotation of an existing entry), **and**
2. A primary source: a paper, an official repository, or an official dataset page.

An entry belongs in **Derivatives & evaluation settings** if it reuses an existing variant's questions — subsets, answer revisions, corpus projections, shared-task projections, or a new evaluation context over the same questions.

**Lineage is functional, not nominal.** A benchmark that drops the "BrowseComp" name can still be family if it is built on the same task idea — persistent browsing toward verifiable answers, or exhaustive set retrieval positioned directly against BrowseComp-style single-answer search. If you propose such an entry, say in the PR why it belongs to the lineage.

Out of scope: training-data pipelines, agent frameworks evaluated *on* BrowseComp, leaderboard subsets, mirrors/forks, and long-report writing benchmarks scored by rubric rather than verifiable answers.

## Entry format

Follow the existing entries:

```markdown
### Name
- **Release:** YYYY-MM · Organisation
- **Size / format:** N questions · language · modality · **open web** or **fixed corpus**
- **Construction:** One or two sentences on how the data was built.
- **Best reported:** Model/system, score, and the split or setting it applies to.
- **Links:** [Paper](…) · [Code](…) · [Data](…) · [Project page](…)
```

Rules:

- **Verify against the primary source.** Link the paper, official repo or dataset page — not a blog post, news article or third-party summary.
- **Conflicting figures are shown side by side, never silently merged.** If the paper says 1,000+ and the released splits sum to 1,089, the entry shows both, with a line in *A note on conflicting figures*.
- **"Best reported" is the entry's own reported result**, with its split/setting named. Do not import scores from other papers' comparison tables without saying so.
- **Say what is missing.** If there is no paper, no code release, or data is request-only, state it plainly in the entry (see SnapshotBrowseComp, LoHoSearch, Ko-WideSearch for the pattern).
- **Preview / unreleased benchmarks must be flagged** ⚠️ in the entry and the comparison table (see ATLAS).
- Update `benchmarks.json` in the same PR, and adjust the counts in the README header, the lineage map and the comparison table if the entry changes them.

## Corrections

If a number here is wrong, a PR with a link to the primary source showing the correct figure is the fastest fix. If two primary sources disagree, we list both — open an issue describing the conflict rather than replacing one figure with the other.

## Style

- British or American English spelling are both fine; be consistent within an entry.
- Keep entries factual and compact. No marketing language, no superlatives about your own benchmark.
- One benchmark per PR where possible, so each can be verified independently.
