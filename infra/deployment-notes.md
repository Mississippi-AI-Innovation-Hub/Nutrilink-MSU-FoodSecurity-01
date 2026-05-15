# Deployment Notes

## Deployment Context

NutriLink was deployed as a sandbox proof-of-concept using AWS services. The deployment was intended for demonstration and evaluation only, not production use.

## AWS Services Used

- **Amazon S3** for storing markdown-based knowledge base documents
- **Amazon Bedrock Knowledge Bases** for retrieval-augmented generation
- **Amazon Nova 2 Lite** for natural-language response generation
- **AWS Lambda** for backend query handling
- **Amazon API Gateway** for exposing the Lambda function to the frontend
- **HTML / JavaScript frontend** for chatbot-style user interaction

## General Deployment Flow

1. Prepare markdown documents containing Hinds County resources, HER/SWAP guidance, and county context.
2. Upload the markdown documents into an Amazon S3 bucket.
3. Create an Amazon Bedrock Knowledge Base.
4. Connect the S3 bucket as the Knowledge Base data source.
5. Sync the Knowledge Base.
6. Test retrieval and response quality in Amazon Bedrock Playground.
7. Deploy an AWS Lambda function to call the Knowledge Base.
8. Connect the Lambda function to Amazon API Gateway.
9. Configure the frontend to call the API Gateway endpoint.
10. Test the GUI using sample prompts.

## Important Security Notes

Do not commit:

- AWS access keys
- API keys
- Secret keys
- Live API Gateway endpoints
- AWS account IDs
- Real `.env` files
- Production data
- Protected agency data

Use placeholders in public files.

Example:

```javascript
const API_URL = "YOUR_API_GATEWAY_ENDPOINT";