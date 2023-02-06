# SNS -> SMS

## 🔥 Import

```typescript
import * as sns from 'aws-cdk-lib/aws-sns';
import * as subscriptions from 'aws-cdk-lib/aws_sns_subscriptions';
```

## 🔥 Code

```typescript
declare const myTopic: sns.Topic;

myTopic.addSubscription(new subscriptions.SmsSubscription('+15551231234'));
```
