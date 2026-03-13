# Contributing Guide

Thank you for your interest in contributing to this repository! This project contains Helm value files and ArgoCD application configuration for managing Kubernetes deployments.

## Getting Started

1. **Fork the repository** and clone it locally.
2. Create a new branch for your changes:
   ```bash
   git checkout -b your-branch-name
   ```

## What's in This Repository

- **`values.yaml`** – Helm values file used by the ArgoCD multi-source application.
- **`multi-source-app.yaml`** – ArgoCD `Application` manifest that references the values file in this repository alongside a Helm chart from an OCI registry.

## Making Changes

### Updating Values

When modifying `values.yaml`:

- Keep changes minimal and well-scoped.
- Ensure keys and values are valid YAML.
- Verify the change is compatible with the target Helm chart version specified in `multi-source-app.yaml`.

### Updating the ArgoCD Application Manifest

When modifying `multi-source-app.yaml`:

- Follow the [ArgoCD Application CRD specification](https://argo-cd.readthedocs.io/en/stable/operator-manual/application.yaml).
- Test your changes against a non-production ArgoCD instance before submitting.

## Submitting a Pull Request

1. Push your branch to your fork.
2. Open a pull request against the `main` branch of this repository.
3. Provide a clear description of **what** changed and **why**.
4. Wait for a maintainer to review and merge your changes.

## Code of Conduct

Please be respectful and constructive in all interactions. We follow the [Contributor Covenant](https://www.contributor-covenant.org/) code of conduct.

## Questions

If you have questions or run into issues, please [open an issue](../../issues) in this repository.
