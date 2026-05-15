# Testing and Evaluation

Testing focused on whether the NutriLink PoC could demonstrate the success metrics defined in the original scope: a functional AWS-based prototype, natural-language query handling, GUI interaction, HER/SWAP-guided resource support, and successful demonstration to reviewers.

## Testing Methods

- Manual testing in Amazon Bedrock Playground using Nova 2 Lite.
- Manual testing through the HTML GUI.
- API Gateway and Lambda integration testing.
- Knowledge base retrieval testing against uploaded markdown documents.
- Live demonstration and walkthrough during the final showcase.

## Results Summary

| Metric / Test Area | Target | Observed Result | Notes |
|---|---|---|---|
| Functional AWS prototype | Working AWS-based prototype | Demonstrated | API Gateway, Lambda, S3, Bedrock Knowledge Base, and Nova 2 Lite were used in the PoC workflow. |
| GUI chatbot interaction | GUI accepts natural-language questions | Partial / Demonstrated | The GUI worked for basic resource-location queries, but response quality was less consistent than Bedrock Playground testing. |
| Natural-language query handling | Approximately 80% handling of defined use cases | Partial | Strong results were observed in Bedrock Playground, but no formal benchmark dataset was completed. |
| Resource lookup | Guide users toward Hinds County food resources | Demonstrated | Resource-oriented questions were successfully demonstrated. |
| HER/SWAP guidance | Support nutrition-informed guidance | Partial | HER/SWAP context was included in the knowledge base, but advanced food comparison logic was not fully implemented in the GUI. |
| Stakeholder demonstration | Present working PoC to reviewers | Demonstrated | A live walkthrough and final showcase demonstration were completed. |

## Key Testing Observation

The strongest model performance was observed in Amazon Bedrock Playground using Nova 2 Lite. The HTML/API workflow demonstrated the intended architecture but did not always reproduce the same response quality observed in direct Playground testing.

## Evaluation Caveat

No formal automated evaluation benchmark was completed. Results are based on manual testing, live demonstration, and observed behavior during the PoC period.