# Kiwi TCMS Kubernetes Deployment

This repository includes Kubernetes deployment files for setting up Kiwi TCMS with a MariaDB database. The deployment encompasses services, persistent volume claims, and deployments for both Kiwi web and MariaDB.

## Deployment Files

- **kiwitcms-deployment.yaml**: Deploys the Kiwi web application.
- **kiwitcms-pvc.yaml**: Configures the Persistent Volume Claim for Kiwi web uploads.
- **kiwitcms-service.yaml**: Sets up the Kubernetes service for Kiwi TCMS.
- **mariadb-deployment.yaml**: Defines the MariaDB deployment with necessary environment variables.
- **mariadb-pvc.yaml**: Specifies the Persistent Volume Claim for MariaDB.
- **mariadb-service.yaml**: Configures the Kubernetes service for MariaDB.

## Deployment Instructions

1. Apply MariaDB deployment and service files.
   ```bash
   kubectl apply -f mariadb-deployment.yaml
   kubectl apply -f mariadb-pvc.yaml
   kubectl apply -f mariadb-service.yaml
   ```

2. Deploy the Kiwi TCMS web application.
   ```bash
   kubectl apply -f kiwitcms-deployment.yaml
   kubectl apply -f kiwitcms-pvc.yaml
   kubectl apply -f kiwitcms-service.yaml
   ```
3. Access Kiwi TCMS at
   ```plaintext
   https://<KIWITCMS_WEB_SERVICE_EXTERNAL_IP>
   ```

Customize the deployment files to match your environment and specifications.

For more details, refer to individual deployment files in this repository.
