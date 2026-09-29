---
name: lab-reviewer-response
description: Draft post-submission point-by-point reviewer responses, produce an executable manuscript revision map, and apply an approved map to the originally submitted Word manuscript with changed text in red. Use only after a submitted scientific manuscript has received editor or reviewer comments; do not use for pre-submission polishing, peer-review reports written as a reviewer, or general manuscript editing.
---

# Lab Reviewer Response

Use this skill for a returned manuscript revision. The normal inputs are the originally submitted manuscript, the complete editor and reviewer comments, scattered new experimental or analytical results and proposed changes, and any supervisor instructions.

The user's instructions and the current manuscript evidence control the scientific content. The included templates control the lab's response and revision-map presentation. Aim for a courteous, persuasive, evidence-supported answer to the reviewer's actual concerns. Select the key results needed for that answer; do not turn a revision into a demand for an exhaustive new study.

Write from the authors' perspective: make the strongest accurate case for how their results address the concern. Lead with relevant strengths, foreground the most convincing evidence, and explain its significance. Keep rigorous internal evidence assessment separate from the reviewer-facing narrative; do not export an internal list of weaknesses into every reply. Use concessions only when needed to answer an explicit concern or avoid a materially misleading inference, and keep them specific and proportionate. See the persuasive-framing guidance in [lab-style.md](references/lab-style.md).

## Run the mandatory intake gate

At the first activation for every new revision package, respond in chat with an input checklist before drafting any response text or creating any deliverable. Match the user's language. Inventory the supplied files and label each required item `Received`, `Incomplete`, or `Missing`.

Do not draft the point-by-point response until all three required inputs are present and usable:

1. **Originally submitted manuscript:** the exact manuscript version reviewed by the journal, preferably as an editable Word file. The main text is mandatory.
2. **Complete editor and reviewer comments:** the decision letter and all reviewer comments in their original order. Reviewer comments are mandatory even when the decision letter is unavailable.
3. **Added-experiment evidence summary:** a coherent file that records the concrete data, experimental conditions, and result summary intended to answer the reviewers. Supporting figures, tables, spreadsheets, or raw-output files may accompany it, but they do not replace the summary file.

Judge whether the evidence summary is usable for the intended replies: it must identify the concern addressed, what was done and under what essential conditions, the observed result and its source, and completed-versus-planned status. Request controls, sample sizes, statistics, or other details when their absence prevents interpreting a key result or supporting a proposed claim. Do not mark the package incomplete merely because it lacks a comprehensive experimental program or details irrelevant to that claim. A qualitative clarification does not automatically require new quantification. A supplied current-round response draft may serve as the summary file if it contains the necessary evidence information; its assertions alone do not verify the experiments. For concerns needing no new experiment, record the existing evidence or clarification and why it addresses the concern.

Use this chat intake structure:

```text
Before I draft the response, I need to verify the revision package.

Required inputs
[Received/Incomplete/Missing] Originally submitted manuscript: <filename or needed item>
[Received/Incomplete/Missing] Complete reviewer/editor comments: <filename or needed item>
[Received/Incomplete/Missing] Added-experiment evidence summary with data, conditions, and results: <filename or needed item>

Recommended supporting materials
[Received/Missing/Not applicable] Author-written response draft or partial replies for this round (including the first revision)
[Received/Missing/Not applicable] Manuscript already revised against that draft, with SI/figures and tracked/red edits if available
[Received/Missing/Not applicable] Supplementary Information
[Received/Missing/Not applicable] New or revised figures, legends, tables, and source data
[Received/Missing/Not applicable] Detailed methods, statistical outputs, and relevant references
[Received/Missing/Not applicable] Journal decision letter and revision instructions
[Received/Missing/Not applicable] Cover letter, if available
[Received/Missing/Not applicable] Supervisor requirements and preferred response strategy
[Received/Missing/Not applicable] Earlier response letters and revised manuscripts for a later revision round

Drafting status
[Ready / Blocked pending: <items>]

If you already have a response draft or a manuscript revised against it, please
upload them or place them in the project folder for reference. They are optional;
please also identify the originally reviewed manuscript and each draft's version.
```

If any required input is missing or materially incomplete under the criteria above, stop after the intake message and request only the missing or incomplete material. Do not begin a provisional response. Recommended supporting materials are not hard blockers; mention the consequence of an absence only when it affects the requested output. When all required inputs are usable, state that the intake gate has passed and proceed with the requested operating mode.

## Select the operating mode

- **Draft response and revision map:** Use when reviewer comments and new results are supplied. Deliver a point-by-point response and a separate manuscript revision map.
- **Apply a revision map:** Use when a manuscript and an existing revision map are supplied. Produce a revised manuscript in which every changed textual fragment is red.
- **Full revision package:** Use when all inputs are available and the user asks for the complete workflow. Produce all three deliverables and cross-check them together.

Do not require a prewritten response or a pre-revised manuscript, but actively use them when available. Preserve useful author arguments, wording, and completed edits after checking them against reviewer comments and evidence. Record the reviewed baseline, current response draft, and current working manuscript separately; do not mistake an author's revision for the reviewed baseline. Before further edits, reconcile existing changes with the revision map so they are neither lost nor applied twice.

## Read the relevant guidance

Always read [lab-style.md](references/lab-style.md) and [evidence-consistency.md](references/evidence-consistency.md).

Read [revision-map.md](references/revision-map.md) when creating or applying a manuscript revision map.

Read [response-strategy.md](references/response-strategy.md) when a comment has multiple concerns or uses parallel experiments, when it challenges the central claim, novelty, sample provenance, experimental comparability, statistics, or figure evidence, or when checking SI or a cover letter. It covers concern mapping, evidence synthesis, editorial context, alternative response strategies, manuscript-wide claim changes, and linked experiment/figure/method updates.

Use [lab-response-template.docx](assets/lab-response-template.docx) for the response and [manuscript-revision-map-template.docx](assets/manuscript-revision-map-template.docx) for the revision map. Replace every placeholder; do not leave instructional text in a final deliverable.

Use the `documents` skill for Word reading, editing, rendering, and final visual inspection. Use the PDF or spreadsheet skill only when the supplied evidence is in those formats. Preserve citation fields and use the Zotero skill when the user asks to add or verify references through Zotero.

## Build the scientific response

1. Inventory the files and identify the exact revision round and editorial decision. Confirm which manuscript is the originally submitted baseline and, for later rounds, the version actually reviewed. Do not mistake possible consideration of a new submission for an invited revision.
2. Preserve every editor and reviewer comment verbatim and in its original order. Before drafting a complex reply, map the comment's main concerns and subordinate requests. Use the reviewer's explicit labels/order when present; otherwise infer coherent concern groups from the comment. Reply headings must reflect those groups, not the number of experiments or paragraphs. Keep multiple supporting results under their shared concern and do not silently rewrite the quoted comment.
3. Classify every supplied item as completed evidence, planned work, proposed wording, supervisor instruction, or unresolved. Do not present a plan as a completed experiment.
4. Map every editor/reviewer request, including general and unnumbered comments, to the available evidence, response strategy, and manuscript changes. Address every subrequest explicitly. Link repeated concerns to shared change records while keeping each reply understandable on its own.
5. Start each substantive reply with a brief, context-specific expression of thanks or appreciation, including replies that disagree. Then give the direct answer, selected supporting results, and their combined implication for the concern, followed by applicable manuscript actions, locations, and exact quotations. For parallel experiments, explain each one's role and connect them with accurate transitions before a bounded synthesis. Mention limitations where they materially change that answer; do not append a catalogue of everything each experiment cannot establish.
6. If no manuscript change is needed, explain why and omit a forced revised-text quotation.
7. If the key evidence cannot support the proposed answer, identify the specific gap and use an appropriate narrower claim, reasoned alternative, or author-confirmation flag. Separate essential gaps from optional strengthening in the author handoff. Do not reject relevant evidence for failing to establish unrelated or universal claims, and do not put an unapproved new experimental program into the reviewer-facing reply. Never invent data, sample sizes, statistics, locations, figure numbers, citations, or completed work.

## Produce the revision map

Create one entry for every manuscript-affecting reviewer request. Use stable locations based on document name, section heading, paragraph purpose, and an exact anchor phrase. Page and line numbers may be included as secondary locators but must not be the only locator.

Each entry must state the operation, scientific purpose, evidence basis, exact proposed wording or content specification, figure/table implications, formatting requirements, dependencies, and the corresponding response quotation. Record deletions explicitly because red inserted text alone cannot show them.

For a change to a central claim, list every affected section and figure title/legend, not just the paragraph named by the reviewer. For an added experiment, track the linked Results, Methods, figure/SI, legend, statistics, and source-data actions. Use the existing map fields to record these dependencies and the old-to-new panel mapping.

The revision map is an execution specification. It must let another model modify the manuscript without rereading the entire reviewer-response drafting history.

## Apply the revision map

Work on a copy of the reviewed baseline by default. If the user supplies an already revised working manuscript, use a copy of that version for continued editing once its role is clear, and compare it with the reviewed baseline. Preserve verified author changes; reconcile conflicting factual changes with the author. The final red text must show all retained changes relative to the reviewed baseline, including earlier author edits, not just this pass. If the working version is ambiguous, prepare the response/map while clarifying the editing base. Preserve page setup, styles, section structure, tables, figures, captions, fields, references, headers, footers, and unchanged text unless a mapped change requires otherwise.

- Color only newly inserted or replacement text pure red `#FF0000`.
- Keep unchanged text in its original color and formatting, including unchanged fragments within a revised paragraph.
- For a replacement, remove the superseded text and insert the approved replacement in red.
- For a deletion, remove the text and record the deletion in the revision map; use tracked deletion only if the user requests true Track Changes.
- Apply the same red-text rule to new headings, captions, legends, table text, and footnotes.
- Preserve Word citation and bibliography fields. Do not unlink or flatten citations.

After applying the map, update the response's quoted revised text from the actual revised manuscript so the two outputs match exactly.

## Quality gates

Before delivery:

- Confirm that every reviewer comment appears once and every subrequest is answered.
- Compare each complex reply's top-level headings with the reviewer's concern groups and order. Check for a missing label, a duplicated concern, or a paragraph that returns to an earlier group after another group has begun.
- Confirm a courteous opening, clear roles and transitions for parallel evidence, and a shared conclusion that answers the concern within the evidence's scope. Keep optional experimental advice in the author handoff; retain material limitations and do not imply unapproved commitments.
- Review concession sentences: keep those necessary for the actual concern or accuracy, remove generic self-undermining caveats, and consolidate repeated limitations. Ensure the reply clearly states the evidence's strengths and their relevance, without declaring a concern resolved when a central gap remains.
- Confirm that supplied response drafts and pre-revised manuscripts were considered, their version roles recorded, and useful existing work preserved without treating draft assertions as verified data.
- Confirm that editor comments and unnumbered/general assessments are addressed, revised central claims agree across sections, and repeated replies use consistent evidence and figure destinations.
- Verify sample provenance, normalization basis, and what each n represents where these affect the reply. Mark unavailable SI, figures, or source data as unverified.
- Inspect supplied SI figures/tables and reconcile shared values with Methods and replies. Check any supplied cover letter against the actual title, editorial route, major changes, and enclosed files; do not infer SI revision completeness without its baseline.
- Confirm that every claimed experiment, analysis, value, and conclusion is supported by the supplied material.
- Confirm that response quotations exactly match the revised manuscript when a revised manuscript is produced.
- Confirm that every revision-map item is either applied, intentionally deferred, or marked as requiring author confirmation.
- Compare baseline and revised text independently of red formatting; log factual changes and deletions, and check authorship/administrative edits against author instructions.
- Search for placeholders such as `TBD`, `TODO`, `FIGX`, `Fig. XX`, `page XX`, and `line XX`.
- Render every final DOCX and inspect every page. Reopen the files after saving when Word fields or complex formatting are present.
- Run [check_outputs.py](scripts/check_outputs.py) as a structural backstop. Treat its quote-matching results as warnings that still require scientific and visual review.

Name default outputs `<short-title>_point_by_point_response.docx`, `<short-title>_manuscript_revision_map.docx`, and, when requested, `<short-title>_revised_red.docx`.
