# SQS

## 🔥 Import

```typescript
import * as sqs from 'aws-cdk-lib/aws-sqs';
```

## 🔥 Code

```typescript
const myQueue = new sqs.Queue(this, 'Queue');
```

```typescript
// Use managed key

new sqs.Queue(this, 'Queue', {
  encryption: sqs.QueueEncryption.KMS_MANAGED,
});
```

```typescript
// Use custom key

const myKey = new kms.Key(this, 'Key');

new sqs.Queue(this, 'Queue', {
  encryption: sqs.QueueEncryption.KMS,
  encryptionMasterKey: myKey,
});
```

## 🔥 Output

```typescript
new cdk.CfnOutput(this, 'queueName', {
  value: myQueue.queueName,
});
```
