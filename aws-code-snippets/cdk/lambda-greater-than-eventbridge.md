# Lambda -> EventBridge

## 🔥 Import

```typescript
import * as lambda from 'aws-cdk-lib/aws-lambda';
import * as destinations from 'aws-cdk-lib/aws-lambda-destinations';

import * as events from '@aws-cdk/aws-events';
```

## 🔥 Code

```typescript
declare const myFunction: lambda.Function;
declare const myEventBus: events.EventBus;

myFunction.addEventSource(new destinations.EventBridgeDestination(myEventBus));
```
