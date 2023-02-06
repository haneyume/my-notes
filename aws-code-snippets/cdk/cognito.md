# Cognito

## 🔥 Import

```typescript
import * as cognito from 'aws-cdk-lib/aws-cognito';
```

## 🔥 Code

```typescript
function createUserPool(scope: Construct) {
  // 🔥 cognito
  const userPool = new cognito.UserPool(scope, 'userpool', {
    userPoolName: 'my-user-pool',
    selfSignUpEnabled: true,
    signInAliases: {
      email: true,
    },
    autoVerify: {
      email: true,
    },
    standardAttributes: {
      givenName: {
        required: true,
        mutable: true,
      },
      familyName: {
        required: true,
        mutable: true,
      },
    },
    customAttributes: {
      country: new cognito.StringAttribute({ mutable: true }),
      city: new cognito.StringAttribute({ mutable: true }),
      isAdmin: new cognito.StringAttribute({ mutable: true }),
    },
    passwordPolicy: {
      minLength: 6,
      requireLowercase: true,
      requireDigits: true,
      requireUppercase: false,
      requireSymbols: false,
    },
    accountRecovery: cognito.AccountRecovery.EMAIL_ONLY,
    removalPolicy: cdk.RemovalPolicy.RETAIN,
  });

  return userPool;
}

function createUserPoolClient(scope: Construct, userPool: cognito.UserPool) {
  // 🔥 User Pool Client attributes
  const standardCognitoAttributes = {
    givenName: true,
    familyName: true,
    email: true,
    emailVerified: true,
    address: true,
    birthdate: true,
    gender: true,
    locale: true,
    middleName: true,
    fullname: true,
    nickname: true,
    phoneNumber: true,
    phoneNumberVerified: true,
    profilePicture: true,
    preferredUsername: true,
    profilePage: true,
    timezone: true,
    lastUpdateTime: true,
    website: true,
  };

  const clientReadAttributes = new cognito.ClientAttributes()
    .withStandardAttributes(standardCognitoAttributes)
    .withCustomAttributes(...['country', 'city', 'isAdmin']);

  const clientWriteAttributes = new cognito.ClientAttributes()
    .withStandardAttributes({
      ...standardCognitoAttributes,
      emailVerified: false,
      phoneNumberVerified: false,
    })
    .withCustomAttributes(...['country', 'city']);

  // 🔥 User Pool Client
  const userPoolClient = new cognito.UserPoolClient(scope, 'userpool-client', {
    userPool,
    authFlows: {
      adminUserPassword: true,
      custom: true,
      userSrp: true,
    },
    supportedIdentityProviders: [
      cognito.UserPoolClientIdentityProvider.COGNITO,
    ],
    readAttributes: clientReadAttributes,
    writeAttributes: clientWriteAttributes,
  });

  return userPoolClient;
}
```

## 🔥 Output

```typescript
new cdk.CfnOutput(this, 'userPoolId', {
  value: userPool.userPoolId,
});

new cdk.CfnOutput(this, 'userPoolClientId', {
  value: userPoolClient.userPoolClientId,
});
```
