# SQS from existing

## 🔥 Import

```typescript
import * as sqs from 'aws-cdk-lib/aws-sqs';
```

## 🔥 Code

```typescript
const myQueue = sqs.Queue.fromQueueArn(
  this,
  'imported-sqs-queue',
  'EXTERNAL_SQS_QUEUE_ARN',
);
```
