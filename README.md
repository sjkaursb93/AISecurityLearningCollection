# AI Security Learning Collection
The purpose of this learning collection is to provide links to get you started on the journey of AI security implementation in Azure. The content talks about:
- Azure Open AI Security Best Practices
- LLMs Security Best Practices
- AI Security best practices in General

# Before you get started
Keep in mind the principles of **Responsible AI.** The purpose of the RAI initiative is to provide the principles and practices to develop AI in an ethical, fair, and responsible manner. Use these links to be aware of RAI principles. 

- [Overview of Responsible AI practices for Azure OpenAI models - Azure AI services](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/overview)
- [Responsible AI for LLMs ](https://techcommunity.microsoft.com/t5/ai-machine-learning-blog/deploy-large-language-models-responsibly-with-azure-ai/ba-p/3876792)
- [RAI Getting Started](https://github.com/sqlshep/RAI-Hack/blob/main/README.md)
- Other RAI Frameworks
     - [OpenAI Safety](https://openai.com/safety)
 
# OpenAI Security Best Practices
Azure OpenAI is part of Azure Cognitive Services. When setting up OpenAI in azure it is not just that service but also associated resources which needs to be implemented securely. It is imperative to understand how to implement zero trust architecture in Azure for these services.

- Here is the FAQ list of OpenAI, which can help answer general questions related to model, data, privacy etc. - [Azure OpenAI Service frequently asked questions - Azure AI service](https://learn.microsoft.com/en-us/azure/ai-services/openai/faq#using-your-data)
- **Identity**  - Identity is the first entry point and must be secure. RBAC helps implement least privileges which is the one of the principles of zero trust. Use this guidance to implement RBAC in Azure OpenAI - [Role-based access control for Azure OpenAI - Azure AI services](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/role-based-access-control)
- **OpenAI Managed Identity** -  The use of managed identity lets you authorize access to OpenAI without storing the credentials in the resources, e.g. VMs. Use this link to configure managed identities [How to configure Azure OpenAI Service with managed identities - Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/managed-identity)
- **Infratructure** - When setting up OpenAI, Azure allows you to use Selected Network/Private Endpoints only connection to OpenAI. Considering Zero Trust again – this set up validates the concept of Verify Explicitly, Assume Breach and Least Privileges. Here is the networking guidance for OpenAI - [Configure Virtual Networks for Azure AI services - Azure AI services](https://learn.microsoft.com/en-us/azure/ai-services/cognitive-services-virtual-networks?context=%2Fazure%2Fai-services%2Fopenai%2Fcontext%2Fcontext&tabs=portal)
- **Data** is the ultimate target of any breach. We use defense in depth layered approach starting from Identity, Networking, Keys and ultimately data. Use this article to use OpenAI on your data securely - [Using your data with Azure OpenAI securely - Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/use-your-data-securely)
- **Keys** - It is another important thing to protect. There are many examples out there which shows the reason of breach as “hard coded credentials”. Use this article to learn how to protect the API and Endpoint Keys using Azure Key vault - [How to Secure Azure OpenAI Keys Using Environment Variables, Azure Vault, and Streamlit Secrets - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/healthcare-and-life-sciences/how-to-secure-azure-openai-keys-using-environment-variables/ba-p/3821162#:~:text=To%20ensure%20the%20security%20and%20confidentiality%20of%20your,audit%20key%20usage%20to%20detect%20any%20unauthorized%20access.)
- Here is the additional general guidance to help implement the secure architecture for Azure Cognitive Services including Azure OpenAI. : [Azure security baseline for Cognitive Services](https://learn.microsoft.com/en-us/security/benchmark/azure/baselines/cognitive-services-security-baseline#security-profile)

## Other Blogs
- https://journeyofthegeek.com/?s=openai&submit=Search

# When you start working on OpenAI Models in Azure
- **Monitoring** - is the most important security concept which results in accountability (verify explicitly).  Use this preview feature to start monitoring for GenAI apps in production - [Model monitoring for generative AI applications (preview) - Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/prompt-flow/how-to-monitor-generative-ai-applications?view=azureml-api-2)
- **Content Filtering** - Integrated into Azure Open AI service, content filtering can help ensemble of multiple class classification models to detect violence, hate, sexual and self harm at 4 levels safe, low, medium, and high.It also provide optional binary classifiers to detect jailbreaking risk. More information can be found here [How to use content filters (preview) with Azure OpenAI Service - Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/content-filters)
- **Jailbreaking risk detection** - Jailbreak is a technique which takes advantage of weakness of prompting system. . Jailbreaking risk detection is available as an option with new Azure AI Content Safety Studio. [Quickstart: Content Safety Studio - Azure AI services](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/studio-quickstart) && [Quickstart: Detect jailbreak risk (preview) - Azure AI services](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/quickstart-jailbreak)
## Other Blogs
- https://github.com/rod-trent/OpenAISecurity/tree/main/Must_Learn

# LLM Security Guidance
## LLM Specific Threats 
- Check the updated guidane published by OWASP and MITRE. What is OWASP top 10 list – It is a list of top ten critical vulnerabilities often seen in LLM applications. To understand vulnerabilities, their potential impact, ease of exploitation etc, visit these links.
    - [OWASP Top 10 for Large Language Model Applications | OWASP Foundation](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
    - [ATLAS Matrix | MITRE ATLAS™](https://atlas.mitre.org/matrices/ATLAS/)
- The first step – understand the attack. The next step what are the steps to prevent the attacks. Note: not one solution fits all. Something I have learnt and implemented over and over is what is the risk it poses to your organization. How you measure the risk, what are the compensating controls? I’ll add some links to this section to help you make that decision to a step forward to protect your AI solutions.
- Threat Modelling - – This guide [Threat Modeling LLM Applications - AI Village](https://aivillage.org/large language models/threat-modeling-llm/) explains how use trust boundaries and DFDs to do threat modelling for your LLMs. In addition, it also provides recommendations to remediate the vulnerabilities.
- Use this document to understand the questions for threat modelling. It also provides the detail on specific tasks and steps to protect against these threats  Check this article as well for threat modelling [Threat-Modeling AI ML](https://learn.microsoft.com/en-us/security/engineering/threat-modeling-aiml)
- Monitoring is important to detect and monitor the LLM interactions for any undesired behaviors.
    - [Monitoring models in production (preview) - Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/concept-model-monitoring?view=azureml-api-2)
    - [Monitor performance of models deployed to production (preview) - Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-monitor-model-performance?view=azureml-api-2&tabs=azure-cli)

# General Best Practices and Additional Links
- Use of Moderation API if using OpenAI [Moderation - OpenAI API](https://platform.openai.com/docs/guides/moderation) to evaluate use inputs before sending them to OpenAI’s completion or chat API.
- Use this [AI Risk Database](https://airisk.io/) to check the model in AI risk database.
- [How to Evaluate LLMs: A Complete Metric Framework - Microsoft Research](https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/articles/how-to-evaluate-llms-a-complete-metric-framework/)
- [Securing Your LLM’s based Applications: Ways to Prevent Prompt Injection | by Aashir Javed | Medium](https://medium.com/@aashirjaved/securing-your-llms-based-applications-ways-to-prevent-prompt-injection-c9968472e7a8#:~:text=Ways%20to%20prevent%20prompt%20injection%201%20Sanitize%20the,Prompt%20debiasing%20...%204%20GPT-3%20vs%20GPT-4%20)



  
