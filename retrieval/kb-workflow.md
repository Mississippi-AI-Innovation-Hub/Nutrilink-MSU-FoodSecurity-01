# Knowledge Base Workflow

## Overview

NutriLink used Amazon Bedrock Knowledge Bases to support Retrieval-Augmented Generation for food assistance and nutrition guidance.

## Document Preparation

Project information was organized into markdown files before upload.

Example document categories included:

- Hinds County resource information
- County profile information
- HER/SWAP nutrition guidance
- Demo questions and prompts

Markdown was used because it is easy to structure with headings, lists, and short sections.

## S3 Upload

The prepared markdown files were uploaded into an Amazon S3 bucket used as the source for the Bedrock Knowledge Base.

## Knowledge Base Sync

After uploading or updating documents in S3, the Knowledge Base needed to be synced so the new content could be indexed and retrieved.

General process:

1. Upload markdown documents to S3.
2. Open the Bedrock Knowledge Base.
3. Go to the connected data source.
4. Run sync.
5. Wait for sync to complete.
6. Test queries in Bedrock Playground.

## Retrieval and Generation Flow

1. User asks a natural-language question.
2. Bedrock Knowledge Base searches the indexed documents.
3. Relevant chunks are retrieved.
4. Nova 2 Lite generates a response using the retrieved chunks.
5. Response is returned to the user.

## Observed Behavior

- Bedrock Playground testing produced the most accurate and consistent results.
- The GUI/API workflow worked but was less consistent than direct Playground testing.
- Resource-location questions performed best.
- Broader nutrition guidance questions required clearer prompt wording and better document structure.

## Future Improvements

- Improve markdown formatting and section titles.
- Separate county resources from nutrition guidance.
- Add metadata by county, topic, and source type.
- Add citation rendering in the frontend.
- Create a repeatable evaluation set.
- Tune retrieval parameters and prompt structure.