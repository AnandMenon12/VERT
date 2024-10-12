
# VERT: A System Verilog Assertion Dataset to improve Hardware Verification with LLMs


Hardware verification is a key part of System-on-Chip (SoC) design, taking up 70% of development time. SystemVerilog assertions are crucial for ensuring design functionality, but manual assertion generation becomes unmanageable as systems grow in complexity. Large Language Models (LLMs) have shown potential for automating this process, though proprietary models like GPT-4o face limitations in accuracy and come with high costs. Open-source LLMs, while more accessible, need fine-tuning to handle complex hardware code. To address this, we introduce VERT, a dataset designed to improve assertion generation using open-source LLMs. Fine-tuned models like Deepseek Coder 6.7B and Llama 3.1 8B achieve up to 96.88% correctness on platforms like OpenTitan and CVA6 when compated to the base models. VERT reduces the reliance on expensive proprietary models, offering a scalable and efficient solution for hardware verification.


## Features

The VERT dataset offers several key features designed to improve the performance of LLMs in automated hardware verification:

### 1. **Comprehensive Assertion Generation**
   - The dataset includes a diverse collection of **SystemVerilog assertions** covering various conditional structures. This variety allows for comprehensive training and fine-tuning of LLMs, helping them accurately generate assertions for different logical flows in hardware design.

### 2. **Synchronous and Asynchronous Variants**
   - The supplemental datasets contain **synchronous** (`synch`) and **asynchronous** versions of code snippets, which allow LLMs to better understand time-sensitive and clock-sensitive conditions in hardware design, improving their ability to handle both combinational and sequential logic.

### 3 **Fine-Tuning Capability**
   - Designed for fine-tuning smaller, open-source LLMs like **Deepseek Coder 6.7B** and **Llama 3.1 8B**, the dataset empowers these models to **outperform proprietary models** such as GPT-4o in both functional and syntactical correctness, achieving **over 20% improvement** in some cases when compared to GPT-4o.
   - The dataset enables **local fine-tuning**, reducing reliance on costly proprietary solutions and ensuring **data privacy** for hardware corporations that may require custom solutions without exposing sensitive design data.


### 5. **Tested for Industry-Standard Platforms**
   - The assertions generated from the dataset have been evaluated on **industry-standard platforms** like OpenTitan, CVA6, and Pulpissimo SoCs, making it highly relevant for real-world hardware verification use cases.

### 6. **Scalability and Cost-Effectiveness**
   - By using smaller, open-source models that can be fine-tuned with VERT, researchers and hardware companies can significantly reduce the computational and financial overhead compared to larger, proprietary models. VERT’s design allows for **scalable, efficient assertion generation** without compromising on performance.

These features make the VERT dataset a powerful tool for automating hardware verification, reducing manual effort, and enabling more efficient verification processes through advanced LLM capabilities.



## Folder Structure

### 1. **VERT/**
   - **VERT.json**: The primary dataset file containing SystemVerilog code snippets paired with assertions.

### 2. **Supplemental_datasets/**
   - **casedataset-if.json**: Dataset containing assertions derived from `if-else` statements in SystemVerilog code.
   - **casedataset-if-synch.json**: Synchronous version of the `if-else` dataset.
   - **casedataset-!if.json**: Dataset for just `if` conditions.
   - **casedataset-!if-synch.json**: Synchronous version of the `if` dataset.
   - **ifdataset-else.json**: Dataset containing assertions for `if-else` conditions.
   - **ifdataset-else-synch.json**: Synchronous version of the `if-else-sync` conditions dataset.
   - **ifdataset-!else.json**: Dataset handling `if-not-else` conditions.
   - **ifdataset-!else-synch.json**: Synchronous version of the `if-not-else` conditions dataset.
   - **ifdataset.json**: General `if-else` dataset for assertion generation.
   - **VERT_withRAG.json**: A variant of the main dataset, enhanced with Retrieval-Augmented Generation (RAG) techniques.
