# Manuscript revision map

The revision map connects reviewer requests, evidence, response language, and executable manuscript edits. It is both a human checklist and a handoff specification for the later manuscript-editing pass.

## Global header

Record:

- manuscript short title;
- journal and revision round when known;
- editorial decision and submission route, plus the actually reviewed version for later rounds;
- exact baseline manuscript filename;
- filenames containing reviewer comments and new evidence;
- supervisor requirements;
- date and revision-map status: draft, author-confirmed, or applied.

## One entry per manuscript-affecting change

Use the following fields for each entry:

1. **Change ID:** stable identifier such as `R1.2-M1`.
2. **Reviewer source:** reviewer/referee number and original comment number.
3. **Reviewer concern:** concise statement of the issue; do not replace the full comment in the response.
4. **Evidence status:** completed evidence, planned work, proposed wording, supervisor instruction, or unresolved.
5. **Evidence basis:** exact input file, figure/table/data note, sample size, condition, and relevant value.
6. **Target document:** main manuscript, supplementary information, figure file, table, source data, or another submission file.
7. **Stable location:** section heading, subsection, paragraph purpose, and an exact anchor phrase. Page/line numbers are secondary only.
8. **Operation:** insert, replace, delete, move, add figure/table, revise legend, add method, add citation, or cross-reference.
9. **Change form:** one sentence, paragraph, methods subsection, figure panel, table row, legend, limitation statement, or another concrete form.
10. **Exact text or content specification:** exact proposed wording when possible; otherwise a bounded specification that states what must be written after data confirmation.
11. **Figure/table instructions:** panel destination, response-only number, final manuscript number, legend, statistics, source data, and callout location.
12. **Formatting instructions:** red `#FF0000` for changed text, inherited font/style, treatment of citations, and any journal-specific requirement.
13. **Response linkage:** the reply paragraph and exact quotation that must match this change.
14. **Dependencies or author confirmation:** unresolved facts, final numbering, statistical results, citations, or supervisor decisions.
15. **Verification:** evidence checked, text inserted, response synchronized, references/fields preserved, and visual QA passed.

For linked changes, reuse these fields rather than creating disconnected entries: list all affected reviewer IDs in **Reviewer source**, connect dependent entries in **Dependencies**, and record the old-to-new manuscript/SI panels alongside response-figure IDs in **Figure/table instructions**. A central-claim change must enumerate all affected sections and captions. A new experiment must account for the applicable Results, Methods, figure/SI, legend, statistics, and source-data destinations, with unavailable files explicitly unverified. In **Evidence basis**, record sample provenance, normalization, statistical units, and factual corrections when they affect interpretation. See [response-strategy.md](response-strategy.md) for the conditional checks.

## Location rules

Prefer locators such as:

`Main manuscript > Results > “Structural basis of ...” > paragraph beginning “We next examined ...” > insert after the second sentence.`

Avoid instructions such as `add near page 6`. Pagination can change during revision.

## Formatting rules for downstream manuscript editing

- Inserted text: red `#FF0000` and otherwise inherit the surrounding run and paragraph formatting.
- Replacement: delete the old wording and insert the approved replacement in red.
- Partial sentence edit: keep unchanged fragments in their original color; color only the changed words red.
- New paragraph or subsection: inherit the adjacent paragraph or heading style and color all new textual content red.
- New figure or table: preserve the journal layout; mark the new or changed caption/legend text red. Record the asset filename and final destination.
- Deletion: record the exact deleted wording in the map. Use true tracked deletion only when explicitly requested.
- Citations: preserve live citation fields. Mark missing evidence as `CITATION REQUIRED` in the map, not as a fabricated reference in the manuscript.

## Handoff gate

Before using the map to edit a manuscript, verify that the supplied manuscript matches the baseline filename and scientific version recorded in the map. Stop and reconcile version differences if section headings, anchor phrases, figures, or key claims do not match.
