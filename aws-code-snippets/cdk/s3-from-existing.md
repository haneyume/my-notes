# S3 from existing

## 🔥 Import

```typescript
import * as s3 from 'aws-cdk-lib/aws-s3';
```

## 🔥 Code

```typescript
const myBucket = s3.Bucket.fromBucketArn(
  this,
  'imported-bucket',
  'EXTERNAL_BUCKET_ARN',
);
```

```typescript
const myBucket = s3.Bucket.fromBucketName(
  this,
  'imported-bucket',
  'EXTERNAL_BUCKET_NAME',
);
```
