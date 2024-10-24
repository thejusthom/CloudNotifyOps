# CloudNotifyOps

**CloudNotifyOps** is a cloud-native, serverless architecture deployed on Google Cloud Platform (GCP), designed to handle real-time event-driven tasks such as automated email notifications and database updates. It leverages Infrastructure as Code (IaC) principles using Terraform and Github Actions to ensure seamless provisioning and management of resources. The project also incorporates DNS configurations, load balancing, and autoscaling for high availability.

## Key Features

- **Serverless Architecture**: Google Cloud Functions and Pub/Sub for real-time event handling and automated workflows.
- **Database Backend**: CloudSQL used as the relational database backend, with efficient configuration and management.
- **Infrastructure as Code (IaC)**: Terraform manages the infrastructure setup, including CloudSQL, CloudDNS, and autoscaling configurations.
- **CI/CD Integration**: Continuous integration and delivery pipeline using GitHub Actions to automate deployment.
- **DNS Management**: CloudDNS configured for streamlined domain management.

## Project Structure

- **Terraform Configuration**: Code to provision and manage the GCP infrastructure.
  - `terraform/main.tf` - Defines CloudSQL, Cloud Functions, and other cloud resources.
  
- **Cloud Functions**: Serverless code triggered by events from Pub/Sub.
  - `functions/` - Contains the Google Cloud Functions for processing events and sending notifications.

- **Java WebApp**: Frontend hosted on GCP App Engine, allowing users to interact with the system.
  - `webapp/` - Source code for the web application, built using Java.

- **CI/CD Pipeline**: Automates the build, test, and deployment process.
  - `.github/workflows/` - GitHub Actions workflow files for the CI/CD pipeline.

## Prerequisites

- **GCP Account**: Set up Google Cloud Platform and enable the required APIs (Cloud Functions, Pub/Sub, CloudSQL).
- **Terraform**: Install Terraform to manage GCP infrastructure.
- **GitHub Actions**: Ensure you have a GitHub repository connected to deploy the pipeline.

## Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/thejusthom/CloudNotifyOps.git
   cd CloudNotifyOps
2. **Provision infrastructure using Terraform**:

   Navigate to the terraform/ directory and initialize Terraform:
   ```bash
   terraform init
   terraform apply
   Deploy Cloud Functions:

3. **Deploy the Cloud Functions with the configured trigger for Pub/Sub events.**
    Deploy the WebApp:

4. **Build and deploy the Java web application on GCP App Engine.**
    Configure CI/CD:

5. **Review and update the GitHub Actions workflow files to fit your project structure.**

## Usage
**Notifications:** The system automatically sends email notifications based on real-time events triggered by Pub/Sub.
**Database Updates:** CloudSQL is updated automatically based on the events processed by Cloud Functions.

