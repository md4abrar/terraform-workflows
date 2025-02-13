# GitHub actions Workflows

Welcome to the Terraform Workflows repository. This project provides a collection of reusable workflows and configurations to streamline and standardize Terraform deployments using GitHub Actions.

## Overview

Managing infrastructure as code with Terraform can become complex, especially when integrating with CI/CD pipelines. This repository offers predefined GitHub Actions workflows to automate common Terraform tasks, ensuring consistency and best practices across deployments.

## Features

- **Speculative Plans**: Automatically generate Terraform plans for pull requests to preview potential changes without applying them.
- **Automated Applies**: Apply Terraform configurations upon merging pull requests or pushing to the main branch.
- **Linting and Formatting**: Ensure Terraform code adheres to best practices with automated linting and formatting checks.
- **Security Scans**: Integrate security checks to identify vulnerabilities in Terraform configurations.

## Getting Started

To incorporate these workflows into your project:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/md4abrar/terraform-workflows.git
   cd terraform-workflows
   ```

2. **Configure Workflows**:
   - Navigate to the `.github/workflows/` directory.
   - Review and customize the workflow YAML files as needed to fit your project's requirements.

3. **Set Up Secrets**:
   - Ensure that necessary secrets, such as `TF_API_TOKEN` for Terraform Cloud authentication, are added to your GitHub repository settings under "Secrets and variables".

4. **Trigger Workflows**:
   - Workflows are designed to trigger on specific GitHub events, such as pull requests and pushes to the main branch. Ensure your development process aligns with these triggers.

## Workflow Details

### Speculative Plan Workflow

This workflow runs when a pull request is opened or modified. It performs the following steps:

1. **Checkout Code**: Retrieves the latest code from the repository.
2. **Set Up Terraform**: Configures the Terraform CLI.
3. **Initialize Terraform**: Prepares the working directory for use with Terraform.
4. **Validate Configuration**: Ensures the Terraform configuration is syntactically valid.
5. **Generate Plan**: Creates an execution plan to preview changes.

### Apply Workflow

Triggered upon merging a pull request or pushing to the main branch, this workflow:

1. **Checkout Code**: Retrieves the latest code.
2. **Set Up Terraform**: Configures the Terraform CLI.
3. **Initialize Terraform**: Prepares the working directory.
4. **Apply Configuration**: Applies the Terraform configuration to update infrastructure.

## Customization

Feel free to modify the workflows to better suit your project's needs. For instance, you can add steps for:

- Running tests
- Notifying teams via Slack or email
- Deploying applications post-infrastructure changes

## Contributing

We welcome contributions to enhance these workflows. Please fork the repository, create a feature branch, and submit a pull request with your changes.

## License

This project is licensed under the [MIT License](LICENSE).

---

*Note: This README provides a general template. Please ensure to update it with specific details from your repository and workflows.*

