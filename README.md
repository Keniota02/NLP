# NLP
Assignments for the exam Natural Language Processing in the second year of Artificial Intelligence Master in Unibo:
1. [Assignment1_2526.ipynb](Assignment1/Assignment1_2526.ipynb): our approach to Task 2 of
the EXIST 2023 challenge: categorizing tweets
into four classes based on sexist intention (Nonsexist,
Direct, Reported, Judgmental). Addressing
the high variability of linguistic forms in
social media, we explored two complementary
architectures: Recurrent Neural Networks (BiLSTMs)
and Transformer-based models. We
designed a robust evaluation pipeline to compare
Baseline and Stacked BiLSTMs initialized
with three pre-trained embeddings: GloVe-
Wiki, GloVe-Twitter, and FastText. We experimented
both with frozen and trainable embeddings,
giving comparable results. Ultimately,
the Transformer-based approach, with
RoBERTa (Antypas and Camacho-Collados,
2023), demonstrated superior performance over
the best RNN configuration. We further validated
the cross-lingual generalization of Transformers
using pysentimiento (Pérez et al.,2024) for the Spanish subset.


2. [Assignment2_2526.ipynb](Assignment2/Assignment2_2526.ipynb): here, we addresses the task of fine-grained
sexism detection (EDOS Task B), which involves
classifying text as non-sexist or assigning
it to one of four specific sexist categories.
We evaluate the zero-shot performance of three
open-source LLMs, i.e. Mistral-7B-Instructv0.3,
Llama-3.1-8B-Instruct and Qwen3-1.7B.
Our methodology involves designing specific
instruction prompts that define each category
and processing the generated text to map model
outputs to class labels. We measure performance
using Macro F1-score and a Fail-Ratio
metric to assess instruction-following capabilities.
Our results indicate that while models
like Mistral demonstrate a capability to classify
sexism with a Macro F1 of approximately 0.34,
other models such as Llama exhibit significant
safety-filter triggers, resulting in high refusal
rates that hinder performance on this specific
downstream task.
