# Lambda

## 🔥 Import

```typescript
import * as lambda from 'aws-cdk-lib/aws-lambda';
import { NodejsFunction } from 'aws-cdk-lib/aws-lambda-nodejs';
```

## 🔥 Code

```typescript
const myFunction = new NodejsFunction(this, 'Function', {
  runtime: lambda.Runtime.NODEJS_16_X,
  entry: path.join(__dirname, './lambda/index.ts'),
  handler: 'handler',
});
```

```typescript
const myFunction = new lambda.Function(this, 'Function', {
  code: lambda.Code.fromInline(`
    exports.handler = (event, context, callback) => {
      callback(null, 'Hello World!');
    };
  `),
  runtime: lambda.Runtime.NODEJS_16_X,
  handler: 'index.handler',
  timeout: cdk.Duration.seconds(25),
});
```
