cat > docs/architecture.md <<'EOF'
# Architecture Overview

NutriLink is a Retrieval-Augmented Generation (RAG) proof-of-concept focusing on Hinds County food assistance and nutrition resource support for the Mississippi Department of Human Services (MDHS).

## High-Level Workflow

1. A user enters a natural-language question in the GUI.
2. The frontend sends the query to an API Gateway endpoint.
3. API Gateway invokes an AWS Lambda function.
4. Lambda sends the query to Amazon Bedrock Knowledge Bases.
5. Bedrock retrieves relevant context from documents stored in Amazon S3.
6. Nova 2 Lite generates a response using the retrieved context.
7. The response is returned to the GUI.

## Architecture Diagram

```text
User
  ↓
HTML / JavaScript Frontend
  ↓
Amazon API Gateway
  ↓
AWS Lambda
  ↓
Amazon Bedrock Knowledge Base
  ↓
Nova 2 Lite
  ↓
Amazon S3 Markdown Documents