# Proposed AWS architecture

| Service | Role |
|---|---|
| S3 and Lambda | Agreements and purchase exports stored per customer and checked as they arrive |
| Textract | Text and tables read from scanned agreement PDFs |
| Bedrock | Rebate terms extracted into tiers, rates and conditions |
| DynamoDB | Agreements, purchases, calculations and the review log |

One AWS account per customer, encrypted at rest and in transit. The public demo calls none of these services.
