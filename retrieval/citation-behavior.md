# Citation Behavior

## Overview

NutriLink was built as a Retrieval-Augmented Generation proof-of-concept using Amazon Bedrock Knowledge Bases. The system retrieved information from uploaded markdown documents and generated responses using Nova 2 Lite.

## Current Citation Behavior

The frontend GUI did not implement full citation rendering during the PoC.

During testing:

- Responses were generated using retrieved knowledge base context.
- Bedrock Playground showed stronger visibility into retrieved context and source chunks.
- The GUI returned generated responses but did not consistently display document-level citations.
- Source attribution was handled through the knowledge base retrieval process rather than through a polished frontend citation display.

## Why Citation Rendering Matters

For future versions, citation behavior is important because users and reviewers should be able to see:

- Which source document supported the response
- Whether the answer came from local resource data, HER/SWAP guidance, or county-level context
- Whether the answer is grounded in project data or is general model output

## Recommended Future Citation Improvements

Future work should add:

- Source document names in responses
- Retrieved chunk references
- Inline citations
- Confidence or fallback messages
- Clear distinction between retrieved facts and generated explanation
- A message when the system cannot find enough relevant information

## Example Future Citation Format

```text
Answer:
Food assistance resources in Hinds County may include food banks, local pantries, SNAP-related assistance, and community organizations.

Sources:
- local_food_resources.md
- county_profiles.md