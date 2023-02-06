# SNS -> SQS

## 🔥 Import

```typescript
import * as sns from 'aws-cdk-lib/aws-sns';
import * as subscriptions from 'aws-cdk-lib/aws_sns_subscriptions';

import * as sqs from 'aws-cdk-lib/aws-sqs';
```

## 🔥 Code

```typescript
declare const myTopic: sns.Topic;
declare const myQueue: sqs.Queue;

myTopic.addSubscription(new subscriptions.SqsSubscription(myQueue));
```
