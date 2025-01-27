## FinanceBench

### Abstract
- Test suite to evaluate LLMs on open book financial question answering
- 10k questions with answers and evidence strings
- closely reflects real-world conditions
- 16 SOTA configs
- 150 cases sampled & manually reviewed, giving 16*150 = 2400 cases (on GitHub)
- GPT4 Turbo was wrong 81% of the time
- Longer context window improves performance but is not feasible in real world settings (latency, can’t support large financial docs)


### Introduction
- LLMs can augment & automate labor intensive task of financial analysis to help make better investment decisions.
- No ways to evaluate model’s performance on finance specific tasks
    - So, can’t understand strength and weakness of models
    - Assess the performance in high stakes, live scenarios
    - Tack changing capabilities over time
 
- Challenges posed by the financial domain to LLMs 
  - One
      - Domain specific knowledge is needed to train these LLMs (we don’t know how much was done in the Pre-Training stage)
      - BloombergGPT solves this being specialised for the Financial domain only
  - Two
      - Up to date data needed. But many models’ data are months or years old
  - Three
      - LLMs can’t do math (hallucinations in calculations)
  - Four
      - Both unstructured inputs (qualitative questions in the form of free-text) and tabular (structured) input
      - Many LLMs are bad at tabular data (without additional training)
  - Five
      - Small pieces of info across multiple documents & parse long paragraphs of text


- So FinanceBench introduced to evaluate LLMs in Finance
- 4 SOTA, 4 Configs (Oracle, closed book, 2 vector stores, Long context window)

