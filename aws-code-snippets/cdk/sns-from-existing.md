# SNS from existing

## 🔥 Import

```typescript
import * as sns from 'aws-cdk-lib/aws-sns';
```

## 🔥 Code

```typescript
const myTopic = sns.Topic.fromTopicArn(
  this,
  'imported-sns-topic',
  'EXTERNAL_SNS_TOPIC_ARN',
);
```
