---
name: lab-reviewer-response
description: Draft post-submission point-by-point reviewer responses, produce an executable manuscript revision map, and apply an approved map to the originally submitted Word manuscript with changed text in red. Use only after a submitted scientific manuscript has received editor or reviewer comments; do not use for pre-submission polishing, peer-review reports written as a reviewer, or general manuscript editing.
---

# Lab Reviewer Response

Use this skill for a returned manuscript revision. The normal inputs are the originally submitted manuscript, the complete editor and reviewer comments, scattered new experimental or analytical results and proposed changes, and any supervisor instructions.

The user's instructions and the current manuscript evidence control the scientific content. The included templates control the lab's response and revision-map presentation.

## Run the mandatory intake gate

At the first activation for every new revision package, respond in chat with an input checklist before drafting any response text or creating any deliverable. Match the user's language. Inventory the supplied files and label each required item `Received`, `Incomplete`, or `Missing`.

Do not draft the point-by-point response until all three required inputs are present and usable:

1. **Originally submitted manuscript:** the exact manuscript version reviewed by the journal, preferably as an editable Word file. The main text is mandatory.
2. **Complete editor and reviewer comments:** the decision letter and all reviewer comments in their original order. Reviewer comments are mandatory even when the decision letter is unavailable.
3. **Added-experiment evidence summary:** a coherent file that records the concrete data, experimental conditions, and result summary intended to answer the reviewers. Supporting figures, tables, spreadsheets, or raw-output files may accompany it, but they do not replace the summary file.

Treat the added-experiment evidence summary as incomplete unless it identifies, where applicable, the linked reviewer concern, experiment or analysis performed, samples and groups, conditions and controls, sample size or replicate information, statistical method and values, quantitative or qualitative result, source figure or table, interpretation, limitations, and whether each item is completed or only planned. Do not demand fields that genuinely do not apply, but call out material omissions.

Use this chat intake structure:

```text
Before I draft the response, I need to verify the revision package.

Required inputs
[Received/Incomplete/Missing] Originally submitted manuscript: <filename or needed item>
[Received/Incomplete/Missing] Complete reviewer/editor comments: <filename or needed item>
[Received/Incomplete/Missing] Added-experiment evidence summary with data, conditions, and results: <filename or needed item>

Recommended supporting materials
[Received/Missing/Not applicable] Supplementary Information
[Received/Missing/Not applicable] New or revised figures, legends, tables, and source data
[Received/Missing/Not applicable] Detailed methods, statistical outputs, and relevant references
[Received/Missing/Not applicable] Journal decision letter and revision instructions
[Received/Missing/Not applicable] Supervisor requirements and preferred response strategy
[Received/Missing/Not applicable] Earlier response letters and revised manuscripts for a later revision round

Drafting status
[Ready / Blocked pending: <items>]
```

If any required input is missing or incomplete, stop after the intake message and request only the missing or incomplete material. Do not begin a provisional response. Recommended supporting materials are not hard blockers, but explain briefly how each material omission may reduce specificity, accuracy, placement confidence, or cross-document consistency. When all required inputs are usable, state that the intake gate has passed and proceed with the requested operating mode.

## Select the operating mode

- **Draft response and revision map:** Use when reviewer comments and new results are supplied. Deliver a point-by-point response and a separate manuscript revision map.
- **Apply a revision map:** Use when a manuscript and an existing revision map are supplied. Produce a revised manuscript in which every changed textual fragment is red.
- **Full revision package:** Use when all inputs are available and the user asks for the complete workflow. Produce all three deliverables and cross-check them together.

Do not require a prewritten response or a pre-revised manuscript. Those are outputs of this workflow.

## Read the relevant guidance

Always read [lab-style.md](references/lab-style.md) and [evidence-consistency.md](references/evidence-consistency.md).

Read [revision-map.md](references/revision-map.md) when creating or applying a manuscript revision map.

Use [lab-response-template.docx](assets/lab-response-template.docx) for the response and [manuscript-revision-map-template.docx](assets/manuscript-revision-map-template.docx) for the revision map. Replace every placeholder; do not leave instructional text in a final deliverable.

Use the `documents` skill for Word reading, editing, rendering, and final visual inspection. Use the PDF or spreadsheet skill only when the supplied evidence is in those formats. Preserve citation fields and use the Zotero skill when the user asks to add or verify references through Zotero.

## Build the scientific response

1. Inventory the files and identify the exact revision round. Confirm which manuscript is the originally submitted baseline.
2. Preserve every editor and reviewer comment verbatim and in its original order. Split the work internally when one numbered comment contains several requests, but do not silently rewrite the quoted comment.
3. Classify every supplied item as completed evidence, planned work, proposed wording, supervisor instruction, or unresolved. Do not present a plan as a completed experiment.
4. Map every reviewer request to the available evidence, the proposed response, and any manuscript change. Address every subrequest explicitly.
5. Draft each reply in this order when applicable: concise acknowledgement; direct answer; experiment or analysis performed; result; interpretation with appropriate limits; exact manuscript action and location; quoted revised text.
6. If no manuscript change is needed, explain why and omit a forced revised-text quotation.
7. If the evidence cannot support the requested claim, narrow the claim, state the limitation, or mark the issue for author confirmation. Never invent data, sample sizes, statistics, locations, figure numbers, citations, or completed work.

## Produce the revision map

Create one entry for every manuscript-affecting reviewer request. Use stable locations based on document name, section heading, paragraph purpose, and an exact anchor phrase. Page and line numbers may be included as secondary locators but must not be the only locator.

Each entry must state the operation, scientific purpose, evidence basis, exact proposed wording or content specification, figure/table implications, formatting requirements, dependencies, and the corresponding response quotation. Record deletions explicitly because red inserted text alone cannot show them.

The revision map is an execution specification. It must let another model modify the manuscript without rereading the entire reviewer-response drafting history.

## Apply the revision map

Work on a copy of the originally submitted manuscript. Preserve page setup, styles, section structure, tables, figures, captions, fields, references, headers, footers, and unchanged text unless a mapped change requires otherwise.

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
- Confirm that every claimed experiment, analysis, value, and conclusion is supported by the supplied material.
- Confirm that response quotations exactly match the revised manuscript when a revised manuscript is produced.
- Confirm that every revision-map item is either applied, intentionally deferred, or marked as requiring author confirmation.
- Search for placeholders such as `TBD`, `TODO`, `FIGX`, `Fig. XX`, `page XX`, and `line XX`.
- Render every final DOCX and inspect every page. Reopen the files after saving when Word fields or complex formatting are present.
- Run [check_outputs.py](scripts/check_outputs.py) as a structural backstop. Treat its quote-matching results as warnings that still require scientific and visual review.

Name default outputs `<short-title>_point_by_point_response.docx`, `<short-title>_manuscript_revision_map.docx`, and, when requested, `<short-title>_revised_red.docx`.
