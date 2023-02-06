# S3 -> Lambda

## 🔥 Import

```typescript
import * as s3 from 'aws-cdk-lib/aws-s3';
import * as s3n from 'aws-cdk-lib/aws-s3-notifications';

import * as lambda from 'aws-cdk-lib/aws-lambda';
```

## 🔥 Code

```typescript
declare const myBucket: s3.Bucket;
declare const myFunction: lambda.Function;

s3Bucket.addEventNotification(
  s3.EventType.OBJECT_CREATED,
  new s3n.LambdaDestination(myFunction),
  // 👇 only send message to queue if object matches the filter
  // {prefix: 'test/', suffix: '.png'},
);
```
