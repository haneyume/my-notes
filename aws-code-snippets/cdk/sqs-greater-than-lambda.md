# SQS -> Lambda

## 🔥 Import

```typescript
import * as sqs from 'aws-cdk-lib/aws-sqs';

import * as lambda from 'aws-cdk-lib/aws-lambda';
import {
  SqsEventSource,
  SqsEventSourceProps,
} from 'aws-cdk-lib/aws-lambda-event-sources';
```

## 🔥 Code

```typescript
declare const myQueue: sqs.Queue;
declare const myFunction: lambda.Function;

myFunction.addEventSource(new SqsEventSource(myQueue));
```
