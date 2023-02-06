# S3 -> SQS

## 🔥 Import

```typescript
import * as s3 from 'aws-cdk-lib/aws-s3';
import * as s3n from 'aws-cdk-lib/aws-s3-notifications';

import * as sqs from 'aws-cdk-lib/aws-sqs';
```

## 🔥 Code

```typescript
declare const myBucket: s3.Bucket;
declare const myQueue: sqs.Queue;

myBucket.addEventNotification(
  s3.EventType.OBJECT_CREATED_PUT,
  new s3n.SqsDestination(myQueue),
  // 👇 only send message to queue if object matches the filter
  // {prefix: 'test/', suffix: '.png'},
);
```
