# Python Boilerplate

Used by Jenkins bootstrap job to create new services.

Contains:
- src/app.py
- tests/
- Dockerfile
- Jenkinsfile
- catalog-info.yaml

Jenkinsfile uses:
@Library('platform-pipelines') _
pythonService()

SERVICE_NAME is replaced during bootstrap.
catalog-info.yaml also uses SERVICE_NAME placeholders so generated repos can be discovered by Backstage and linked to GitHub/Jenkins.
catalog-info.backstage.yaml is the local descriptor for the boilerplate repository itself.
