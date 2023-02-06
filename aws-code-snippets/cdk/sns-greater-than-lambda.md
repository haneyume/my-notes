# SNS -> Lambda

## 🔥 Import

```typescript
import * as sns from 'aws-cdk-lib/aws-sns';
import * as subscriptions from 'aws-cdk-lib/aws_sns_subscriptions';

import * as lambda from 'aws-cdk-lib/aws-lambda';
```

## 🔥 Code

```typescript
declare const myTopic: sns.Topic;
declare const myFunction: lambda.Function;

myTopic.addSubscription(new subscriptions.LambdaSubscription(myFunction));
```
