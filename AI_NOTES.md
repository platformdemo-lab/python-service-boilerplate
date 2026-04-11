# Python Boilerplate

Used by Jenkins bootstrap job to create new services.

Contains:
- src/app.py
- tests/
- Dockerfile
- Jenkinsfile
- catalog-info.template.yaml
- catalog-info.backstage.yaml

Jenkinsfile uses:
@Library('platform-pipelines') _
pythonService()

SERVICE_NAME is replaced during bootstrap.
catalog-info.template.yaml uses SERVICE_NAME placeholders so generated repos can be discovered by Backstage and linked to GitHub/Jenkins.
catalog-info.backstage.yaml is the local descriptor for the boilerplate repository itself and must not be copied into generated services.
The bootstrap Jenkins job should register the generated repo's catalog-info.yaml back into Backstage after pushing the new repository.
