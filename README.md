
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

1. Clone the repository.

      `git clone <repository-link>`

2. To deploy the wordpress run the below command.

    `kubectl apply -f WORDPRESS-WITH-KUBERNETES`

3. Then run this command to forward the port to localhost.

   `kubectl port-forward svc/wordpress 3838:3838`

4. Search this url in your browser

   `localhost:3838`

## CLEAN UP

1. To clean all these resources.
   
   `kubectl delete all --all`

2. If you have other rources in kubernetes don't run this command. Run the following commands.

   `kubectl delete -f deploy wordpress mysql`
   
   `kubectl delete -f svc wordpress mysql`
   
   `kubectl delete pv wordpress-storage mysql-storage`
   
   `kubectl delete pvc wordpress-storage mysql-storage`

