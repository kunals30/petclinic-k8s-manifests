
# Spring PetClinic Kubernetes Deployment

Kubernetes manifests for deploying Spring PetClinic to AWS EKS.

## Resources

- `deployment.yaml` — runs the PetClinic application
- `service.yaml` — provides internal access to the application

## Container Registry

The application image is stored in a Nexus Docker hosted repository.

The EKS worker nodes must have network access to Nexus and be configured to authenticate to the registry.

## GitOps

Argo CD will monitor this repository and synchronize the Kubernetes manifests with the EKS cluster.
