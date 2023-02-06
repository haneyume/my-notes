# Cognito from existing

## 🔥 Import

```typescript
import * as cognito from 'aws-cdk-lib/aws-cognito';
```

## 🔥 Code

```typescript
const myUserPool = cognito.UserPool.fromUserPoolId(
  this,
  'imported-user-pool',
  'EXTERNAL_USER_POOL_ID',
);
```

```typescript
const myUserPool = cognito.UserPool.fromUserPoolArn(
  this,
  'imported-user-pool',
  'EXTERNAL_USER_POOL_ARN',
);
```

```typescript
const myUserPoolClient = cognito.UserPoolClient.fromUserPoolClientId(
  this,
  'imported-user-pool-client',
  'EXTERNAL_USER_POOL_CLIENT_ID',
);
```
