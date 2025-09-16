<div style="text-align: center;">
  <img src="./media/logo.svg" width="100" alt="logo"/>
</div>

## ImageWatch
ImageWatch is a robust and easy-to-deploy solution designed to keep your Docker images up-to-date and
secure. It proactively scans your local Kubernetes clusters and Docker Swarm installations,
identifying any outdated image tags
<br><br>
Screenshot from the client UI:
![Image List UI](./media/ui_image_overview.png)

## Deployment
This repository contains the deployment definitions for running the 
ImageWatch client in a Kubernetes environment.

### Prerequisites
- A Kubernetes cluster (at least version 1.17)
- kubectl command-line tool configured to interact with your cluster
- Helm (optional, for managing deployments)

## Getting started
To get started with ImageWatch, signup on [ImageWatch.app](http://imagewatch.app) and follow these steps:

### Deployment Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Florianisme/ImageWatch
    ```
2. Review and customize the deployment files as needed
   1. Add your license key to the `plain/deployment.yaml` file in the `IMAGEWATCH_API_KEY` environment variable.
3. Deploy the service using kubectl:
   ```bash
   kubectl apply -f plain/
   ```
4. Verify the deployment:
   ```bash
   kubectl get pods -n image-watch
   ```
5. Access the ImageWatch client UI on port 8090 of the deployed pod or set up a service to expose it externally.
