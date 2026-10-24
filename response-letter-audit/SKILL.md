---
name: response-letter-audit
description: Audit an existing academic response letter for reviewer coverage, numerical and cross-response consistency, opening-overview accuracy, and Word formatting. Produce a visually verified Word audit with actionable corrections. Use for checking revision responses, not for drafting an initial letter or writing a referee report.
---

# Response Letter Audit

Audit the existing response letter and produce an evidence-based report. Determine whether the authors answer the review team's concerns, whether their statements agree with each other, and what needs correction or verification. Do not predict acceptance or treat polite wording as evidence that a concern has been resolved.

## Inputs and scope

Required: the response letter, including reviewer comments and authors' responses. Optional: editor decision letter, original reviewer reports, revised manuscript and appendices, prior manuscript, estimation exports or code, previous audit, and supplied journal formatting requirements.

Use explicitly designated files. When the user designates an audit Input folder, use only its contents unless they authorize other sources. Record the exact input filenames and versions in a short scope paragraph at the beginning of the report. Do not silently select a different version by modification time. If versions are ambiguous and affect the findings, ask a focused question while continuing independent checks.

A response-letter-only audit is valid. Complete the internal checks and mark unavailable verification explicitly:

- Without original reviews, coverage is assessed only against comments reproduced in the letter; completeness of that reproduction is unverified.
- Without a revised manuscript, claimed manuscript changes are unverified, not automatically absent.
- Without previous manuscript versions, a change can be located but cannot necessarily be confirmed as newly added.
- Without estimation output, numerical agreement does not verify estimation correctness.
- Prior audits are leads to recheck, not proof that an issue persists.

Read the full document, including table notes, equations, captions, footnotes and relevant appendices. Inspect embedded table images visually when their numbers cannot be extracted reliably. For tracked changes, assess the intended revised text by including insertions and excluding deletions, and report material ambiguity about the intended version. Also note visible tracked changes as a formatting item when relevant. Never silently flatten or modify the source.

## Audit workflow

### 1 Map reviewer concerns and assess coverage

Include editor, senior editor, associate editor and reviewer requests. Preserve existing identifiers. Split multi-part comments into separately assessable concerns, for example R2.3a and R2.3b, without altering the quoted original. Link shared concerns while retaining every originating comment ID.

For each concern, identify:

- The specific question, requested action or underlying methodological concern. Treat uncertain interpretations as uncertain; do not speculate about motives.
- The authors' direct answer, supporting evidence and stated revision or reason for declining.
- Whether the evidence addresses the actual concern, including its consequential subparts.
- Any remaining limitation and the smallest concrete next step.

Assess coverage as Fully addressed, Partly addressed, Not addressed, or Cannot assess. Record evidence verification separately as Verified in supplied material, Contradicted by supplied material, or Not independently verified. A well-justified disagreement may fully address a request. A claimed new analysis without enough evidence need not do so.

Distinguish clarification of existing content, a completed revision, a proposed revision and a justified refusal. Do not require additional experiments for every comment. A cross-reference to another answer is acceptable when precise and sufficient to understand the resolution. Flag evasive, unsupported or needlessly hostile responses when they impair the answer; do not require ritual apologies or repeated thanks.

### 2 Check tables and numerical reporting

Inventory all numerical tables and repeated analyses in the letter. Match analyses by outcome, sample, estimator, controls, fixed effects, treatment timing and inference method, rather than assuming similar titles denote identical models.

Compare:

- Coefficients, signs, standard errors, confidence intervals and significance stars.
- Observation counts, fit statistics, units, outcome transformations and reference categories.
- Column numbering and labels, sample restrictions, control and fixed-effect rows, and inference notes.
- Numerical statements in the surrounding responses, opening overview, captions and notes.

Recalculate arithmetic where inputs are available: log-to-percent conversions, coefficient sums, shares, denominators, percentage-point changes, revenue calculations and transfers. Check consistent use of exact versus approximate transformations. Allow reasonable rounding; a difference across genuinely different specifications is not automatically a contradiction. Identical results across different inference methods warrant verification rather than a presumption of error.

Do not derive a significance test for a coefficient sum or contrast without the required covariance information. An overall model F statistic is not automatically a test of pre-treatment leads. Do not infer significance from rounded values alone or treat a nonsignificant estimate as proof of no effect.

If estimates conflict, report both with their locations. Prefer a supplied export only after confirming its specification and version. Otherwise request reconciliation instead of choosing a plausible-looking value.

### 3 Check consistency across responses and revision promises

Compare definitions, samples, time windows, controls, timing, reference periods, methods, results, mechanisms, limitations and interpretations across all authors' responses. Check table, figure, equation, section and appendix references. Preserve reviewer quotations even when their historical numbers differ from the revised analysis.

Assess whether the strength of the conclusions matches the evidence, including causal versus descriptive claims, mechanism evidence, uncertainty, economic versus statistical significance and the distinction between revenue, profit and welfare where applicable.

For each claimed manuscript change, record the linked concern and the stated destination. With the manuscript supplied, check the actual text or result; a matching section title alone is insufficient. Separate results intentionally provided only in the response letter from results explicitly promised for the manuscript or appendix. Response-only evidence is not automatically a missing manuscript revision.

Resolve overlapping findings under one issue ID and list every affected location. Conflicting reviewer requests should be reported with the authors' rationale; do not automatically favor a more supportive reviewer.

### 4 Check the opening revision overview

Map each substantive overview claim to the detailed responses and, when available, manuscript evidence. Check in both directions:

- Does the overview claim a result, analysis or completed revision unsupported or contradicted below?
- Does it omit a major editor concern or materially misrepresent the scope of the revision?

The overview need not list every minor correction. Flag blanket assertions that all concerns are resolved when substantive gaps remain. Check that completed and proposed changes are clearly distinguished and that effect sizes, methods and limitations match the detailed answers. If no overview exists, report that fact and recommend one only when useful or required.

### 5 Check Word formatting and navigation

Inspect heading hierarchy, reviewer/author visual distinction, fonts, spacing, indentation, margins and page numbering for consistency and readability. Check captions, numbering, cross-references, equations, symbols, superscripts, significance notation and links. Look for broken fields, placeholders, accidental highlighting, comments and tracked changes; distinguish intentional markup from unintended residue.

Respect a supplied journal template. Without one, report concrete readability and consistency problems rather than imposing arbitrary font or margin rules.

Render the source Word document for visual inspection without editing it. Check all pages for clipping, overlap, split or unreadable tables, detached captions, repeated-header problems and awkward page breaks. Keep substantive statistical issues distinct from cosmetic formatting issues. If rendering is unavailable, disclose that source layout remains unverified; text extraction alone cannot establish visual correctness.

### 6 Consolidate findings and propose corrections

Give each finding a stable issue ID, all relevant comment/table locations, the conflicting statements or values, the implication, and a correction or verification step.

Record two independent labels:

- Priority: Critical for a central validity or reporting problem; Major for a substantive gap or inconsistency; Minor for a limited presentation problem.
- Finding status: Confirmed discrepancy, Interpretation concern, or Requires verification.

Order by consequence and strength of evidence, not by reviewer order alone. Do not label missing input as a confirmed scientific error. Recommend new analysis only when a specific unresolved concern needs it; describe the needed output without inventing its result. Suggested wording must preserve uncertainty and must not claim that unperformed work is completed.

## Required Word report

Save directly to:

`GPT_audit/YYYY-MM-DD/Response_letter_audit_YYYYMMDD.docx`

Resolve GPT_audit relative to the user-designated revision/project folder; use the current project folder if no different root is designated. Use the user's local audit date. If the supplied package is already inside GPT_audit/YYYY-MM-DD, save beside its Input folder rather than nesting another GPT_audit. Create missing directories, but do not create an Output subfolder. Preserve an existing same-day report by adding a version suffix when needed.

After the title and short input/scope paragraph, use exactly these four top-level sections in this order:

### 1 Reviewer coverage matrix

Use one row per actionable concern, with columns for Comment ID, Concern, Response and evidence, Coverage assessment, Evidence verification, and Remaining action or linked issue ID. Include non-actionable praise briefly without assigning it a fabricated revision requirement. Keep a short status key and coverage counts within this section; make the counts agree with the matrix. Repeat header rows on continuation pages and split by reviewer when necessary for readability.

### 2 Consistency issues

Present the prioritized findings with stable issue IDs, priority, finding status, exact locations, evidence and implications. Include numerical, methodological, interpretation, promised-revision, cross-reference and Word-formatting issues here. Use a compact comparison table for conflicting values where helpful; present longer reasoning in prose. If a check finds no issue, state that without inventing a finding.

### 3 Overview of revision checking

Assess the opening overview against the detailed responses: supported claims, contradictions, important omissions and overstated completion. Identify the linked reviewer concerns and issues. Keep this section distinct from a general audit summary.

### 4 Suggested corrections

For each issue ID, specify the correction, every location needing synchronization and any verification required before replacement. Provide replacement wording when supported by available evidence. Distinguish editorial fixes from corrections requiring estimation output, additional analysis or manuscript verification. Include suggested overview wording only when supported; do not repeat all finding descriptions.

Use stable section/table/comment labels and short text anchors. Add page or line numbers only when verified for the exact input version, specifying which document they refer to. Keep source-reviewer text and authors' text clearly attributed.

Use the available documents skill to create the report. Render the final DOCX, inspect every page, repair layout defects and re-render until clean. Keep rendering intermediates in a temporary QA location and deliver only the final Word report unless other formats are requested. If rendering fails, report the failure and do not describe the deliverable as visually verified.

## Boundaries

Leave all input documents unchanged. Do not submit, publish or send the response letter. Never invent estimates, citations, reviewer intentions, tests, page references or completed revisions. Matching tables establish internal agreement, not empirical correctness. Do not silently broaden a letter-only audit into a manuscript rewrite or re-estimation project. Do not upload unpublished inputs to public services or repositories as part of source research.

## Public references informing this workflow

These are background examples, not instructions to import external skills or apply venue-specific rules. This skill retains a journal response-audit scope rather than conference score strategy or rebuttal drafting.

- [TobiasLee Rebuttal Skill](https://github.com/TobiasLee/Rebuttal-Skill/blob/main/SKILL.md): evidence-grounded answers, uncertainty, and a quality-review checklist.
- [paper-lifecycle rebuttal-response](https://github.com/M1n-n9/paper-lifecycle/blob/master/rebuttal-response/SKILL.md): concern mapping and traceability between evidence and revision actions.
- [AER Skills aer-rebuttal](https://github.com/brycewang-stanford/AER-Skills/blob/main/skills/aer-rebuttal/SKILL.md): separate concern identifiers and explicit treatment of clarification, revision and justified refusal. Do not adopt its assumptions about reviewer preferences.
- [Noble 2017 Ten simple rules for writing a response to reviewers](https://doi.org/10.1371/journal.pcbi.1005730): complete point-by-point coverage, self-contained answers, overview, typography and clarity about what changed.
