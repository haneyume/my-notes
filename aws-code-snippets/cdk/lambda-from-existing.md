# Lambda from existing

## 🔥 Import

```typescript
import * as lambda from 'aws-cdk-lib/aws-lambda';
```

## 🔥 Code

```typescript
const myFunction = lambda.Function.fromFunctionArn(
  this,
  'imported-lambda-func',
  'EXTERNAL_LAMBDA_FUNCTION_ARN',
);
```

```typescript
const myFunction = lambda.Function.fromFunctionName(
  this,
  'imported-lambda-func',
  'EXTERNAL_LAMBDA_FUNCTION_NAME',
);
```
