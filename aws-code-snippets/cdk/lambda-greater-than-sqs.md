# Lambda -> SQS

## 🔥 Import

```typescript
import * as lambda from 'aws-cdk-lib/aws-lambda';
import * as destinations from 'aws-cdk-lib/aws-lambda-destinations';

import * as sqs from 'aws-cdk-lib/aws-sqs';
```

## 🔥 Code

```typescript
declare const myFunction: lambda.Function;
declare const myQueue: sqs.Queue;

myFunction.addEventSource(new destinations.SqsDestination(myQueue));
```
