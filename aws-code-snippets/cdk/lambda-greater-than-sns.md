# Lambda -> SNS

## 🔥 Import

```typescript
import * as lambda from 'aws-cdk-lib/aws-lambda';
import * as destinations from 'aws-cdk-lib/aws-lambda-destinations';

import * as sns from 'aws-cdk-lib/aws-sns';
```

## 🔥 Code

```typescript
declare const myFunction: lambda.Function;
declare const myTopic: sns.Topic;

myFunction.addEventSource(new destinations.SnsDestination(myTopic));
```
