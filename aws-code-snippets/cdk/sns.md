# SNS

## 🔥 Import

```typescript
import * as sns from 'aws-cdk-lib/aws-sns';
```

## 🔥 Code

```typescript
const myTopic = new sns.Topic(this, 'Topic');
```

```typescript
const myTopic = new sns.Topic(this, 'Topic', {
  fifo: true,
});
```

## 🔥 Output

```typescript
new cdk.CfnOutput(this, 'topicName', {
  value: myTopic.topicName,
});
```
