# ProofLoop
# ProofLoop — Research That Can Defend Itself

**Your evidence changes. Your paper should know.**

![ProofLoop concept animation](assets/proofloop-loop.gif)

A researcher approves a conclusion and keeps writing. A new paper challenges it—but the original literature review never tells them.

ProofLoop is designed to connect claims, source evidence, and researcher decisions, then bring the researcher back when new evidence deserves attention.

## Product preview

![ProofLoop dashboard, claim review, draft review, and connections prototype](assets/proofloop-prototype.png)

**Design prototype:** the screens contain illustrative research content and connection statuses. They are not proof of live integrations or validated scientific findings. The animation above explains the intended workflow; it is not a recorded execution.

## One connected research journey

Submit a claim → retrieve literature → compare evidence → save references and a review → request a human decision.

The monitoring extension is intended to reassess previously reviewed claims without silently replacing approved conclusions.

| Service | Role |
| --- | --- |
| Semantic Scholar | Literature discovery and available abstracts |
| Groq | Analysis of retrieved evidence |
| Zotero | Reference storage |
| Notion | Evidence reviews and decision records |
| Slack | Approval requests and notifications |

n8n orchestrates the workflow and holds structured records in Data Tables. Rork provides the current frontend design. Hugging Face similarity is optional; MemPalace is excluded from the intended MVP.

## Prototype status

The development transcript reports an n8n input form, year validation, evidence-processing nodes, persistence, and external integration nodes. Credential configuration and a complete live multi-app execution remain unconfirmed. Offline logic checks do not verify delivery through external services.

Word draft checking and ongoing monitoring are intended features; the supplied screenshots do not establish working document access or scheduled checks. MemPalace removal was requested but has not been independently verified in the saved workflow.

## Run the workflow

A sanitized n8n workflow export must be added before this repository is runnable.

1. Import the supplied workflow JSON into n8n.
2. Recreate or map the required Data Tables.
3. Configure credentials and choose the Zotero library, Notion destination, and Slack channel inside n8n.
4. Submit a claim, topic, population, year range, and dependent decision.
5. Inspect the execution and verify actual reference saving, review creation, notification, and researcher response.

Frontend source and deployment instructions must be added after the app is built. Do not commit API keys, credential exports, private drafts, or unredacted execution data.

## Evidence principles

- Link findings to retrieved sources and label abstract-only analysis.
- Deduplicate by source identifiers; a missing DOI does not automatically invalidate a paper.
- Distinguish contradictory results from differences in population and methodology.
- Treat service failure as unavailable evidence retrieval, not an empty successful search.
- Keep evidence age separate from scientific confidence.
- Require researcher review before revising approved conclusions.

## Demo and submission

Suggested demo: evaluate whether LightGBM is an appropriate baseline for industrial machinery fault diagnosis under concept drift, using a 2015–2026 evidence window.

Show a real retrieved paper, source-linked analysis, a saved reference, a review page, and a researcher decision. Label any simulated new-evidence event explicitly.

Still to attach: sanitized workflow JSON, frontend source if built, demo recording, and verified live-run results. No quantitative reliability metrics are claimed yet.

## Team

**Maliha Ehsan** — Solo participant, BS Computer Science, University of Management and Technology.

Prepared for the Multi-App AI Agent Hackathon.
