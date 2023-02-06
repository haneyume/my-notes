# DynamoDB from existing

## 🔥 Import

```typescript
import * as dynamodb from 'aws-cdk-lib/aws-dynamodb';
```

## 🔥 Code

```typescript
const myTable = dynamodb.Table.fromTableArn(
  this,
  'imported-table',
  'EXTERNAL_TABLE_ARN',
);
```

```typescript
const myTable = dynamodb.Table.fromTableName(
  this,
  'imported-table',
  'EXTERNAL_TABLE_NAME',
);
```
