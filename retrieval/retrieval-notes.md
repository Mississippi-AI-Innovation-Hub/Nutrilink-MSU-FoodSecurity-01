# Retrieval Notes

## Retrieval Approach

NutriLink used a Retrieval-Augmented Generation approach.

Instead of relying only on the foundation model's general knowledge, the system retrieved context from uploaded project documents before generating a response.

## Model and Retrieval Setup

- **Foundation model:** Amazon Nova 2 Lite
- **Retrieval system:** Amazon Bedrock Knowledge Bases
- **Document storage:** Amazon S3
- **Document format:** Markdown
- **Primary focus:** Hinds County, Mississippi

## Documents Used for Retrieval

The PoC used curated markdown documents related to:

- Hinds County food resource information
- HER/SWAP nutrition guidance
- County-level food insecurity context
- County Health Rankings and Roadmaps-related context
- Demo and evaluation prompts

## Strongest Use Cases

The strongest observed retrieval performance was for questions such as:

- Where can I find food assistance in Hinds County?
- What organizations help with food insecurity?
- What is HER/SWAP guidance?
- What types of food resources are available?

## Weaker or Partial Use Cases

The system was less consistent for:

- Detailed personalized nutrition advice
- Condition-specific health recommendations
- Complex meal classification
- Broad policy questions
- Questions requiring data not present in the uploaded documents

## Playground vs GUI Behavior

Direct testing in Amazon Bedrock Playground produced stronger and more consistent results than testing through the HTML GUI and API workflow.

This suggests the Knowledge Base and model performed adequately, while the frontend/API orchestration needed additional refinement.

Potential causes include:

- Different prompt formatting
- API request structure
- Lambda response handling
- Retrieval configuration differences
- Token or response parsing limitations
- Limited frontend error handling

## Recommended Retrieval Improvements

Future versions should:

- Use clearer markdown headings.
- Add document metadata.
- Separate data by topic and county.
- Add fallback responses when retrieval confidence is low.
- Include citations in the frontend.
- Build a formal evaluation query set.
- Compare Playground and API prompts side-by-side.