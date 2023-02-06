# S3 -> SNS

## 🔥 Import

```typescript
import * as s3 from 'aws-cdk-lib/aws-s3';
import * as s3n from 'aws-cdk-lib/aws-s3-notifications';

import * as sns from 'aws-cdk-lib/aws-sns';
```

## 🔥 Code

```typescript
declare const myBucket: s3.Bucket;
declare const myTopic: sns.Topic;

myBucket.addEventNotification(
  s3.EventType.OBJECT_CREATED_PUT,
  new s3n.SnsDestination(myTopic),
  // 👇 only send message to topic if object matches the filter
  // {prefix: 'test/', suffix: '.png'},
);
```
