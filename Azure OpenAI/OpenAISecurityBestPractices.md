# OpenAI Security Best Practices


 When setting up Azure OpenAI, you're not just deploying a single service. You're also provisioning and integrating several associated Azure resources such as:

- Azure Virtual Networks (VNets)
- Private Endpoints
- Azure Key Vault
- Azure API Management
- Azure Monitor 
- Azure Storage 

These components must be configured securely to ensure the confidentiality, integrity, and availability of your AI workloads.

## Secure AI Deployment

A secure AI Deployment in Azure might look like this:

- Use private endpoints to restrict access to resources over the public internet.
- Integrate with Azure Virtual Networks (VNets) for network isolation.
- Store secrets and keys in Azure Key Vault and restrict access.
- Apply security policies and monitoring using Azure Monitor and Defender for Cloud.
- Use Azure API Management to control and monitor API access.
- Regularly update and patch all resources to mitigate vulnerabilities.


## Identity


Ensure that only authorized users and applications can access Azure OpenAI resources. Use Microsoft Entra for authentication and role-based access control (RBAC) to manage permissions. Regularly review and update access policies to follow the principle of least privilege. In the context of Azure OpenAI, RBAC helps you control access to:

	- The Azure OpenAI resource itself
	- Associated resources like Azure Key Vault, Storage, API Management, etc.
	- Deployment and usage of models (e.g., GPT-4, embeddings)
	- Monitoring and logging configurations

**Reference:** 
- [Role-based access control for Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/how-to/role-based-access-control)
- [Managed identity for Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/how-to/managed-identity)
- [Disable Local Authentication](https://learn.microsoft.com/en-us/azure/ai-services/disable-local-auth)

## Networking

Azure OpenAI supports secure networking through Selected Networks and Private Endpoints, enabling access only from trusted virtual networks. This setup aligns with Zero Trust principles by enforcing explicit verification, minimizing exposure, and assuming breach. It ensures that AI services are accessible only through tightly controlled and monitored network paths.

**Reference:** [Azure Cognitive Services and Virtual Networks](https://learn.microsoft.com/en-us/azure/ai-services/cognitive-services-virtual-networks?tabs=portal)

## Data


Next step, your data. How to configure Azure OpenAI on your data with  focus on secure, scalable, and compliant deployment? The reference walks you through setting up Azure AI Search, Azure Storage, and Azure OpenAI with virtual networks, private endpoints, and managed identities. This also covers implementing document-level access control using Microsoft Entra ID, enabling fine-grained permissions for enterprise data.

**Reference:** [Use your data securely with Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/use-your-data-securely)

## Keys


These are critical assets that must be secured. Many security breaches have been traced back to hard-coded credentials in code. Refer to the link to learn how to protect the API Keys.

**Reference:** [How to secure Azure OpenAI keys using environment variables, Azure Vault, and more](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/how-to-secure-azure-openai-keys-using-environment-variables-azure-vault-and-stre/3821162)


## Monitoring

Monitoring and Observability are essential for collecting metrics that help you track security, performance, and operational health of your Azure OpenAI workloads. These insights enable proactive issue detection, cost optimization, and compliance enforcement.



**Reference:** 
- [Monitor Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/how-to/monitor-openai)
- [Monitor Azure OpenAI Reference](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/monitor-openai-reference)
- [Observability concepts in Azure AI Foundry](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/observability)
