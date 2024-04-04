# external-dns-helm-template-with-cloudflare-configurations


The ExternalDNS Helm template with Cloudflare configurations streamlines the deployment of ExternalDNS, a Kubernetes tool enabling automatic DNS management. This template incorporates Cloudflare-specific configurations, facilitating seamless integration of Kubernetes services with Cloudflare DNS. 

## Prerequisites 

Before deploying ExternalDNS with Cloudflare configurations, ensure the following prerequisites are met:

- Kubernetes cluster is set up and accessible.
- Helm is installed in the Kubernetes cluster.
- Cloudflare account is available with appropriate permissions for managing DNS records

## Deployment Steps
To deploy ExternalDNS with Cloudflare configurations using this Helm template, follow these steps:

1.  Clone this repository to your local machine:
    `git clone https://github.com/NashTech-Labs/external-dns-helm-template-with-cloudflare-configurations.git` 
    
2.  Navigate to the repository directory:
    
    `cd external-dns-helm-template-with-cloudflare-configurations` 
    
3.  Customize the `values.yaml` file to specify Cloudflare API credentials and other configurations as per your environment.
    
4.  Install ExternalDNS using Helm:
    
    
    `helm install external-dns . -f values.yaml` 
    
5.  Verify the deployment by checking ExternalDNS pods:
    
    `kubectl get pods -n <namespace>` 
    
6.  Confirm that ExternalDNS is synchronizing Kubernetes resources with Cloudflare by inspecting DNS records in the Cloudflare dashboard.
