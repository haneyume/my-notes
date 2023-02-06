# DynamoDB -> Lambda

## 🔥 Import

```typescript
import * as dynamodb from 'aws-cdk-lib/aws-dynamodb';

import * as lambda from 'aws-cdk-lib/aws-lambda';
import { DynamoEventSource } from '@aws-cdk/aws-lambda-event-sources';
```

## 🔥 Code

```typescript
declare const myTable: dynamodb.Table;
declare const myFunction: lambda.Function;

myFunction.addEventSource(
  new DynamoEventSource(myTable, {
    startingPosition: lambda.StartingPosition.LATEST,
  }),
);
```
