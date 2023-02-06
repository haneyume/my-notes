# Trigger from Cognito

## 🔥 Doc

{% embed url="https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools-working-with-aws-lambda-triggers.html" %}

## 🔥 Code

```typescript
import { CognitoUserPoolTriggerEvent } from 'aws-lambda';

export const handler = async (
  event: CognitoUserPoolTriggerEvent,
): Promise<void> => {
  console.log(event);

  return;
};
```

## 🔥 Example event

```json
{
  "version": "string",
  "triggerSource": "string",
  "region": "AWSRegion",
  "userPoolId": "string",
  "userName": "string",
  "callerContext": {
    "awsSdkVersion": "string",
    "clientId": "string"
  },
  "request": {
    "userAttributes": {
      "string": "string"
    }
  },
  "response": {}
}
```
