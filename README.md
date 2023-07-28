# Awesome-AI-RE
Collect textbooks, blogs, papers, tools about the application of AI model on Reverse Engineering

## Reverse Engineering
### Textbook
[Reverse Engineering for Beginners](https://ia801300.us.archive.org/20/items/ReverseEngineeringForBeginnersEn/Reverse_Engineering_for_Beginners-en.pdf)

## Traditional Machine Learning

## Context Embeddings

## LLM
### LLM on Codes
[PanGu-Coder2](https://paperswithcode.com/paper/pangu-coder2-boosting-large-language-models)
[ELMo](https://arxiv.org/pdf/1802.05365.pdf)
[BERT](https://arxiv.org/pdf/1810.04805.pdf)
[T5](https://arxiv.org/pdf/1910.10683.pdf)
GPT Family
[LaMDA](https://blog.google/technology/ai/lamda/)
[PaLM](https://arxiv.org/pdf/2204.02311.pdf)
[LLaMA](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/)
[PolyCoder](https://arxiv.org/pdf/2202.13169.pdf)


### OpenAI blog
GPT playground

### ChatGPT with Reverse Engineering
[LmPa: Improving Decompilation by Synergy of Large Language Model and Program Analysis](https://arxiv.org/pdf/2306.02546), arxiv, 2023

### Papers on LLM
[A systematic evaluation of large language models of code](https://dl.acm.org/doi/pdf/10.1145/3520312.3534862)

### Papers on RE + LLM
[Pop Quiz! Can a Large Language Model Help With Reverse Engineering?](https://arxiv.org/pdf/2202.01142), arxiv, 2022
[Jailbreaker: Automated Jailbreak Across Multiple Large Language Model Chatbots](https://arxiv.org/pdf/2307.08715) arxiv, 2023
[LmPa: Improving Decompilation by Synergy of Large Language Model and Program Analysis](https://arxiv.org/pdf/2306.02546), arxiv, 2023

## Papers
### Pop Quiz! Can a Large Language Model Help With Reverse Engineering?](https://arxiv.org/pdf/2202.01142
Abstract: Large language models (such as OpenAI’s Codex) have demonstrated impressive zero-shot multi-task capabilities in the software domain, including code explanation. In this work, we examine if this ability can be used to help with reverse engineering. Specifically, we investigate prompting Codex to identify the purpose, capabilities, and important variable names or values from code, even when the code is produced through decompilation. Alongside an examination of the model’s responses in answering open-ended questions, we devise a true/false quiz framework to characterize the performance of the language model. We present an extensive quantitative analysis of the measured performance of the language model on a set of program purpose identification and information extraction tasks: of the 136,260 questions we posed, it answered 72,754 correctly. A key takeaway is that while promising, LLMs are not yet ready for zero-shot reverse engineering.
Task:
Method:
Result:

### Jailbreaker: Automated Jailbreak Across Multiple Large Language Model Chatbots
Abstract: —The landscape of Artificial Intelligence (AI) services has been significantly influenced by the rapid proliferation of Large Language Models (LLMs), primarily due to their remarkable proficiency in comprehending, generating, and completing text in a manner that mirrors human interaction. Among these services, LLM-based chatbots have gained widespread popularity due to their ability to facilitate smooth and intuitive humanmachine exchanges. However, their susceptibility to jailbreak attacks — attempts by malicious users to prompt sensitive or harmful responses against service guidelines — remains a critical concern. Despite numerous efforts to expose these weak points, our research presented in this paper indicates that current strategies fall short in effectively targeting mainstream LLM chatbots. This ineffectiveness can be largely attributed to undisclosed defensive measures, implemented by service providers to thwart such exploitative attempts. 
Our paper presents JAILBREAKER, a comprehensive framework that offers insight into the intriguing dynamics of jailbreak attacks and the countermeasures deployed against them. JAILBREAKER provides a dual-pronged contribution. Initially, we propose a novel method that utilizes time-based characteristics intrinsic to the generation process to deconstruct the defense mechanisms employed by popular LLM chatbot services. This approach, informed by time-based SQL injection techniques, allows us to unravel valuable details about the functioning of these defensive measures. Through careful manipulation of the chatbots’ time-sensitive reactions, we unravel the complex aspects of their design and establish a proof-of-concept attack to circumvent the defenses of multiple LLM chatbots such as CHATGPT, Bard, and Bing Chat. 
Our second offering is an innovative method for the automatic generation of jailbreak prompts that target robustly defended LLM chatbots. The crux of this approach involves leveraging an LLM to auto-learn successful patterns. By fine-tuning an LLM with jailbreak prompts, we validate the potential of automated jailbreak creation for several high-profile commercial LLM chatbots. Our method generates attack prompts achieving an average success rate of 21.58%, considerably surpassing the 7.33% success rate accomplished by existing prompts. We have conscientiously reported our findings to the impacted service providers. JAILBREAKER establishes a groundbreaking approach to unveil vulnerabilities in LLMs, underscoring the need for more formidable defenses against such intrusions.

Task: use LLM to assist  jailbreak attacks and defense mechanisms
Method:
Result:
Finetune: Yes

### LmPa: Improving Decompilation by Synergy of Large Language Model and Program Analysis
Abstract: Decompilation aims to recover the source code form of a binary executable. It has many applications in security and software engineering such as malware analysis, vulnerability detection and code reuse. A prominent challenge in decompilation is to recover variable names. We propose a novel method that leverages the synergy of large language model (LLM) and program analysis. Language models encode rich multi-modal knowledge, but its limited input size prevents providing sufficient global context for name recovery. We propose to divide the task to many LLM queries and use program analysis to correlate and propagate the query results, which in turn improves the performance of LLM by providing additional contextual information. Our results show that 75% of the recovered names are considered good by users and our technique outperforms the state-of-the-art technique by 16.5% and 20.23% in precision and recall, respectively. 

Task: using GPT family to recover identifier names(functions, variables) from stripped binaries

Model: chatGPT

Method: Prompt Engineering + iterative query and propagation
1. Feed the predicted identifier names back into the prompt
2. Both human-curated and GPT-based name validation and propagation

Result:
1. A detailed user study
