# Lambda + https url

## 🔥 Import

```typescript
import * as lambda from 'aws-cdk-lib/aws-lambda';
```

## 🔥 Code

```typescript
declare const myFunction: lambda.Function;

const funUrl = myFunction.addFunctionUrl({
  authType: lambda.FunctionUrlAuthType.NONE,
  cors: {
    allowedOrigins: ['*'],
  },
});
```
