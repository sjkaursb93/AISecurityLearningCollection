# AI Security Learning Collection
The purpose of this learning collection is to provide links to get you started on the journey of AI security implementation in Azure. The content talks about:
- Azure Open AI Security Best Practices
- LLMs Security Best Practices
- AI Security best practices in General

 


# When you start working on OpenAI Models in Azure
- **Monitoring** - is the most important security concept which results in accountability (verify explicitly).  Use this preview feature to start monitoring for GenAI apps in production - [Model monitoring for generative AI applications (preview) - Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/prompt-flow/how-to-monitor-generative-ai-applications?view=azureml-api-2)
- **Content Filtering** - Integrated into Azure Open AI service, content filtering can help ensemble of multiple class classification models to detect violence, hate, sexual and self harm at 4 levels safe, low, medium, and high.It also provide optional binary classifiers to detect jail breaking risk. More information can be found here [How to use content filters (preview) with Azure OpenAI Service - Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/content-filters)
- **Jailbreaking risk detection and protection** - Prompt Shields protects applications powered by foundation models from two types of attacks direct (jailbreak) and indirect prompt injection attacks. This feature is built on existing jailbreak risk detection feature. [Check this out for more details](https://techcommunity.microsoft.com/t5/ai-azure-ai-services-blog/azure-ai-announces-prompt-shields-for-jailbreak-and-indirect/ba-p/4099140). [Quick start Prompt Shields](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/quickstart-jailbreak#analyze-attacks).
- **Using Defender for cloud for to secure the AI applications** - It is the new [security posture and threat protection](https://techcommunity.microsoft.com/t5/microsoft-defender-for-cloud/secure-your-ai-applications-from-code-to-runtime-with-microsoft/ba-p/4127665) capabilities to enable organizations to protect their enterprise-built Gen AI applications through the entire life cycle.
- **New Tools to Build Secure Gen AI Applications in Azure** - If you are using Azure AI Studio, tools such as prompt shields, groundness detection, saftey system messages can help you safeguard your applications.More details are available [here](https://azure.microsoft.com/en-us/blog/announcing-new-tools-in-azure-ai-to-help-you-build-more-secure-and-trustworthy-generative-ai-applications/) 

# LLM Security Guidance
## Attacks on LLMs
- Check the updated guidance published by OWASP and MITRE. What is OWASP top 10 list – It is a list of top ten critical vulnerabilities often seen in LLM applications. To understand vulnerabilities, their potential impact, ease of exploitation etc, visit these links.
    - [OWASP Top 10 for Large Language Model Applications | OWASP Foundation](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
    - [OWASP ML top 10](https://owasp.org/www-project-machine-learning-security-top-10/)
    - [ATLAS Matrix | MITRE ATLAS™](https://atlas.mitre.org/matrices/ATLAS/)
    - I'd also recommend this [MSRC AI Bug Bar](https://www.microsoft.com/en-US/msrc/aibugbar?msockid=2374e47992096e7a2adef0c193de6fb5). It describes Microsoft severity classification for common vulnerability types for systems involving Artificial Intelligence or Machine Learning (AI/ML)

## Understanding the Risks and Attack Surfaces
- The first step – understand the attack. The next step what are the steps to prevent the attacks. Note: not one solution fits all. Something I have learnt and implemented over and over is what is the risk it poses to your organization. How you measure the risk, what are the compensating controls? I’ll add some links to this section to help you make that decision to a step forward to protect your AI solutions.
 
    - Here is a nice read on [Catastrophic AI Risks](https://www.safe.ai/ai-risk)
    - Use [AI Incident Databases](https://incidentdatabase.ai/) to check the real world harms scenarios by deployment of AI Systems.
    - Use [AI Vulnerability Database](https://avidml.org/#:~:text=AI%20Vulnerability%20Database%20%28AVID%29%20is%20an%20open-source%20knowledge,for%20Artificial%20Intelligence%20%28AI%29%20models%2C%20datasets%2C%20and%20systems.). This is an open source knowledge base of failure modes for AI models, datasets and systems.
    - Use this [AI Risk Database](https://airisk.io/) to check the model in AI risk database.
- Threat Modelling - – This guide [Threat Modeling LLM Applications - AI Village](https://aivillage.org/large%20language%20models/threat-modeling-llm/) explains how use trust boundaries and DFDs to do threat modelling for your LLMs. In addition, it also provides recommendations to remediate the vulnerabilities.
    - Use this document to understand the questions for threat modelling. It also provides the detail on specific tasks and steps to protect against these threats  Check this article as well for threat modelling [Threat-Modeling AI ML](https://learn.microsoft.com/en-us/security/engineering/threat-modeling-aiml)

# Best Practices to Remediate vulnerabilities and reduce the attack surface
- One of the best place to start is these [guidelines for creating secure AI systems](https://www.ncsc.gov.uk/files/Guidelines-for-secure-AI-system-development.pdf). These guidelines will help AI systems to function as intended, are available when needed and work without revealing the sensitive data to unauthorized parties.
- Monitoring is important to detect and monitor the LLM interactions for any undesired behaviors.
    - [Monitoring models in production (preview) - Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/concept-model-monitoring?view=azureml-api-2)
    - [Monitor performance of models deployed to production (preview) - Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-monitor-model-performance?view=azureml-api-2&tabs=azure-cli)
- Use of Moderation API if using OpenAI [Moderation - OpenAI API](https://platform.openai.com/docs/guides/moderation) to evaluate use inputs before sending them to OpenAI’s completion or chat API.
- [PyRIT for generative AI Red teaming](https://www.microsoft.com/en-us/security/blog/2024/02/22/announcing-microsofts-open-automation-framework-to-red-team-generative-ai-systems/)
- [Best practices to architect secure generative AI applications](https://techcommunity.microsoft.com/t5/security-compliance-and-identity/best-practices-to-architect-secure-generative-ai-applications/ba-p/4116661)
- [HiddenLayer Model Scanner](https://techcommunity.microsoft.com/t5/ai-ai-platform-blog/hiddenlayer-model-scanner-helps-developers-assess-the-security/ba-p/4140576) helps developers assess the security of open models in the model catalog
- [LLMs Security Guidance](https://learn.microsoft.com/en-us/ai/playbook/technology-guidance/generative-ai/mlops-in-openai/security/security-recommend)
- [LLMs Security Planning](https://learn.microsoft.com/en-us/ai/playbook/technology-guidance/generative-ai/mlops-in-openai/security/security-plan-llm-application)
- [Understanding and Mitigating AI jailbreak attacks](https://www.microsoft.com/en-us/security/blog/2024/06/04/ai-jailbreaks-what-they-are-and-how-they-can-be-mitigated/)

# Additional Resources

- [How to Evaluate LLMs: A Complete Metric Framework - Microsoft Research](https://www.microsoft.com/en-us/research/group/experimentation-platform-exp/articles/how-to-evaluate-llms-a-complete-metric-framework/)
- [Securing Your LLM’s based Applications: Ways to Prevent Prompt Injection | by Aashir Javed | Medium](https://medium.com/@aashirjaved/securing-your-llms-based-applications-ways-to-prevent-prompt-injection-c9968472e7a8#:~:text=Ways%20to%20prevent%20prompt%20injection%201%20Sanitize%20the,Prompt%20debiasing%20...%204%20GPT-3%20vs%20GPT-4%20)
- [AI Security 101](https://atlas.mitre.org/resources/ai-security-101#llm-security)
- [Navigating New Application Security Challenges Posed By GenAI](https://techcommunity.microsoft.com/t5/security-compliance-and-identity/navigating-new-application-security-challenges-posed-by-genai/ba-p/4128243)
- [GitHub Repo by Omar Santos](https://github.com/The-Art-of-Hacking/h4cker/tree/master/ai_research/AI%20Security%20Best%20Practices)
- [Inside AI Security with Mark Russinovich](https://build.microsoft.com/en-US/sessions/d29a16d5-f9ea-4f5b-9adf-fae0bd688ff3?source=sessions)
- https://journeyofthegeek.com/?s=openai&submit=Search
- https://github.com/rod-trent/OpenAISecurity/tree/main/Must_Learn
- [Not with a bug but with a sticker references](https://www.ram-shankar.com/papers)  

  
