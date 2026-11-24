# Paper Note: Chain-of-Thought Prompting Elicits Reasoning in Large Language Models

- **Notes by:** Genavive Ramirez · Algoverse AI (Summer 2025)
- **Paper:** *Chain-of-Thought Prompting Elicits Reasoning in Large Language Models* (Wei et al., 2022)
- **Link:** [arXiv:2201.11903](https://arxiv.org/abs/2201.11903)

### Problem Addressed
This paper addresses a pertinent reasoning flaw in large language models, that being their weaknesses in completing tasks that require multi-step reasoning. These tasks may be math word problems or logical challenges, despite the fact that these models are extensively supplied with massive datasets, yet are often devoid of dynamic reasoning. This critical shortcoming reflects in erroneous outputs.

### Proposed Method: Chain-of-Thought (CoT) Prompting
Rather than continuously feeding these models with a dense quantity of data, perhaps simply refining prompts may suffice and be a viable solution to reducing faulty model outputs. This paper introduces the chain-of-thought prompting method, in which LLMs are supplied with intermediate reasoning steps that are intended to mirror humans’ thought process. 

This CoT solution involves the alteration of the examples fed to the model, without extensive training/data, and showing step-by-step CoT’s in place of mere input/output pairs.

### Key Findings & Benchmarks
- **Model Scale & GSM8K:** Previous methods such as standard prompting show plateaus in performance regardless of the model's increasing volume. Tested on **PaLM 540B** on the **GSM8K** math benchmark, the addition of CoT prompting pushes accuracy near 100% on in-domain symbolic reasoning tasks, starkly outperforming smaller models like **LaMDA 137B**.
- **Out-of-Distribution (OOD) Generalization:** Even on OOD tasks where the model encounters new and longer sequences than originally trained on, CoT helps the model handle these new problems better—something standard prompting entirely fails at.

### Limitations & Takeaway
While CoT enables the model to better follow this new paradigm of reasoning steps, accuracy is not always guaranteed, as the model may still produce errors despite  seemingly coherent reasoning paths. This paper explicates that the model’s perceived reasoning skills may be more of an imitation than a fundamental understanding.

Overall, this paper affirms that CoT prompting critically defines the capabilities of LLMs, leading to the discovery that LLM reasoning failures can be attributed to unrefined prompting entries rather than internal limits alone.
