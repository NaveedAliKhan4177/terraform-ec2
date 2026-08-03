# 🚀 AWS ECS CI/CD with GitHub Actions

Automatically build a Docker image, push it to **Amazon ECR**, and deploy the latest version to **Amazon ECS** whenever code is pushed to the `main` branch.

## 📌 Workflow

```text
Push to main
      │
      ▼
Build Docker Image
      │
      ▼
Push to Amazon ECR
      │
      ▼
Update ECS Task Definition
      │
      ▼
Deploy to Amazon ECS
```

## ⚙️ Prerequisites

- AWS Account
- Amazon ECR Repository
- Amazon ECS Cluster & Service
- ECS Task Definition (`task-definition.json`)
- Docker
- GitHub Actions

## 🔐 GitHub Secrets

Configure the following repository secrets:

| Secret | Description |
|---------|-------------|
| `AWS_ACCESS_KEY_ID` | AWS Access Key |
| `AWS_SECRET_ACCESS_KEY` | AWS Secret Access Key |

## 🌍 Environment Variables

Update these values in the workflow:

```yaml
AWS_REGION:
ECR_REPOSITORY:
ECS_CLUSTER:
ECS_SERVICE:
ECS_TASK_DEFINITION:
CONTAINER_NAME:
```

## 📁 Project Structure

```text
.
├── .github/
│   └── workflows/
│       └── deploy.yml
├── .aws/
│   └── task-definition.json
├── Dockerfile
└── README.md
```

## ✨ Features

- 🐳 Build Docker image
- 📦 Push image to Amazon ECR
- 🚀 Deploy to Amazon ECS
- 🔄 Automatic deployment on every push to `main`
- ⏳ Waits for service stability

## 📄 License

This project is licensed under the MIT License.
