# Trigger from APIGateway

## 🔥 Doc

{% embed url="https://docs.aws.amazon.com/lambda/latest/dg/services-apigateway.html" %}

## 🔥 Code

```typescript
import { Context, APIGatewayProxyResult, APIGatewayEvent } from 'aws-lambda';

export const handler = async (
  event: APIGatewayEvent,
  context: Context,
): Promise<APIGatewayProxyResult> => {
  const path = event.path;
  const method = event.httpMethod;
  const headers = event.headers;
  const body = event.body;
  const pathParameters = event.pathParameters;

  console.log(path);
  console.log(method);
  console.log(headers);
  console.log(body);
  console.log(pathParameters);

  return {
    statusCode: 200,
    body: JSON.stringify({
      message: 'hello world',
    }),
  };
};
```

## 🔥 Example event

```json
{
  "resource": "/",
  "path": "/",
  "httpMethod": "GET",
  "requestContext": {
    "resourcePath": "/",
    "httpMethod": "GET",
    "path": "/Prod/"
  },
  "headers": {
    "accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9",
    "accept-encoding": "gzip, deflate, br",
    "Host": "70ixmpl4fl.execute-api.us-east-2.amazonaws.com",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Safari/537.36",
    "X-Amzn-Trace-Id": "Root=1-5e66d96f-7491f09xmpl79d18acf3d050"
  },
  "multiValueHeaders": {
    "accept": [
      "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9"
    ],
    "accept-encoding": ["gzip, deflate, br"]
  },
  "queryStringParameters": null,
  "multiValueQueryStringParameters": null,
  "pathParameters": null,
  "stageVariables": null,
  "body": null,
  "isBase64Encoded": false
}
```

## 🔥 Example Proxy integration response object ( Node.js )

```typescript
var response = {
  statusCode: 200,
  headers: {
    'Content-Type': 'application/json',
  },
  isBase64Encoded: false,
  multiValueHeaders: {
    'X-Custom-Header': ['My value', 'My other value'],
  },
  body: '{\n  "TotalCodeSize": 104330022,\n  "FunctionCount": 26\n}',
};
```
