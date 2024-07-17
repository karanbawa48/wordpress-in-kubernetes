
 # WORDPRESS

**This repository contains Kubernetes configurations to deploy a WordPress application backed by a MySQL database.**

## Files

- **mysql-deployment.yaml**: Defines the MySQL deployment configuration.
- **mysql-service.yaml**: Configures the service for MySQL.
- **mysql-storage.yaml**: Sets up the persistent volume and persistent volume claim for MySQL.
- **wordpress-deployment.yaml**: Defines the WordPress deployment configuration.
- **wordpress-service.yaml**: Configures the service for WordPress.
- **wordpress-storage.yaml**: Sets up the persistent volume and persistent volume claim for WordPress.

## Prerequisites

- minikube is installed
- `kubectl` command-line tool configured to interact with your cluster

## Deployment Steps

1. clone the repository.

      `git clone <repository-link>`

2. To deploy the wordpress run the below command.

    `kubectl apply -f WORDPRESS-WITH-KUBERNETES`

3. then run this command to forward the port to localhost.

   `kubectl port-forward svc/wordpress 3838:3838`


