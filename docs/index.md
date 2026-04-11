# python-service-boilerplate

This repository is the shared starter used by the Jenkins bootstrap flow to create new Python services.

## What gets templated

- `Jenkinsfile`
- `catalog-info.template.yaml`
- application source and tests
- container build files

## Backstage contract

Generated services inherit:

- GitHub source metadata
- TechDocs metadata
- Jenkins job mapping via `jenkins.io/job-full-name`
- a generated `catalog-info.yaml` created from `catalog-info.template.yaml`
