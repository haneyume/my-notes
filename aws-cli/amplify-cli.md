# Amplify CLI

## 🔥 Install Amplify CLI

```sh
npm install -g @aws-amplify/cli
```

## 🔥 Pull Amplify

```sh
amplify pull --appId <YOUR_APP_ID> --envName <YOUR_ENV_NAME>

amplify pull
```

## 🔥 Push Amplify

```sh
amplify push

amplify push --allow-destructive-graphql-schema-updates
```

## 🔥 Mock Amplify

```sh
amplify mock
```

| Command               | Description                                            |
| --------------------- | ------------------------------------------------------ |
| amplify mock          | Run mock server for supported categories               |
| amplify mock api      | Run mock GraphQL server to simulate AppSync            |
| amplify mock function | Locally test/invoke the function in your local backend |
| amplify mock storage  | Run mock server to simulate S3                         |

## 🔥 Configure Amplify

| Category             | Command                   |
| -------------------- | ------------------------- |
| Authentication       | amplify add auth          |
| Storage              | amplify add storage       |
| API (GraphQL)        | amplify add api           |
| API (REST)           | amplify add api           |
| Functions            | amplify add function      |
| Analytics            | amplify add analytics     |
| Notifications        | amplify add notifications |
| Geo                  | amplify add geo           |
| Interactions         | amplify add interactions  |
| Predictions          | amplify add predictions   |
| XR                   | amplify add xr            |
| Custom AWS resources | amplify add custom        |

## 🔥 Codegen

```sh
amplify codegen models
```
