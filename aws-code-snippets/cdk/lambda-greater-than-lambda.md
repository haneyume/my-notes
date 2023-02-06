# Lambda -> Lambda

## 🔥 Import

```typescript
import * as lambda from 'aws-cdk-lib/aws-lambda';
import * as destinations from 'aws-cdk-lib/aws-lambda-destinations';
```

## 🔥 Code

```typescript
declare const myFunction: lambda.Function;
declare const myFunction2: lambda.Function;

myFunction.addEventSource(new destinations.LambdaDestination(myFunction2));
```
