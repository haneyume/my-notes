# DynamoDB

## 🔥 Import

```typescript
import * as dynamodb from 'aws-cdk-lib/aws-dynamodb';
```

## 🔥 Code

```typescript
const myTable = new dynamodb.Table(this, 'Table', {
  partitionKey: { name: 'id', type: dynamodb.AttributeType.STRING },
});
```

```typescript
const myTable = new dynamodb.Table(this, 'Table', {
  billingMode: dynamodb.BillingMode.PAY_PER_REQUEST,
  partitionKey: { name: 'id', type: dynamodb.AttributeType.STRING },
  stream: dynamodb.StreamViewType.NEW_AND_OLD_IMAGES,
});
```
