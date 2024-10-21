# 🌟 VERT: A SystemVerilog Assertion Dataset to Improve Hardware Verification with LLMs

Hardware verification is a critical aspect of System-on-Chip (SoC) design, accounting for up to **70% of development time**. In this context, **SystemVerilog assertions** play a pivotal role in ensuring design functionality. However, as systems grow more complex, manual assertion generation becomes increasingly challenging. 

To address these challenges, we present **VERT** — a dataset designed to enhance the capabilities of **open-source LLMs** for automated assertion generation. Fine-tuned models, such as **Deepseek Coder 6.7B** and **Llama 3.1 8B**, achieve up to **96.88% correctness** on platforms like **OpenTitan** and **CVA6** compared to base models. VERT minimizes the dependency on costly proprietary models like GPT-4o, offering a scalable and efficient solution for hardware verification.

---

## ✨ Key Features

### 1. **Comprehensive Assertion Generation**
   VERT includes a broad collection of **SystemVerilog assertions** covering a range of conditional structures, enabling LLMs to learn and generate assertions for diverse logical flows within hardware designs.

### 2. **Synchronous and Asynchronous Variants**
   The dataset is supplemented with **synchronous** (`synch`) and **asynchronous** code snippets, aiding LLMs in distinguishing and accurately handling time-sensitive, clock-driven, combinational, and sequential logic.

### 3. **Fine-Tuning Capability**
   VERT is designed to fine-tune smaller, **open-source LLMs** like **Deepseek Coder 6.7B** and **Llama 3.1 8B**, empowering them to outperform proprietary models in both **functional** and **syntactical correctness**. Fine-tuning with VERT yields over a **20% improvement** in certain cases compared to GPT-4o.
   - Enables **local fine-tuning**, reducing reliance on costly proprietary solutions and ensuring **data privacy** for hardware companies.

### 4. **Tested for Industry-Standard Platforms**
   Assertions generated using VERT have been validated on **industry-standard platforms** like **OpenTitan**, **CVA6**, and **Pulpissimo SoCs**, making it highly relevant for real-world hardware verification scenarios.

### 5. **Scalability and Cost-Effectiveness**
   Utilizing smaller open-source models fine-tuned with VERT significantly reduces computational and financial overhead, providing a **scalable, efficient solution** for assertion generation without sacrificing performance.

These features make **VERT** a comprehensive and powerful dataset for automating hardware verification, reducing manual effort, and streamlining the verification process using advanced LLMs.

---

## 📂 Folder Structure

### 1. **VERT/**
   - **VERT.json**: The primary dataset file containing SystemVerilog code snippets paired with assertions.

### 2. **Supplemental_datasets/**
   - **casedataset-if.json**: Dataset containing assertions derived from `if-else` statements in SystemVerilog code.
   - **casedataset-if-synch.json**: Synchronous version of the `if-else` dataset.
   - **casedataset-!if.json**: Dataset for assertions based solely on `if` conditions.
   - **casedataset-!if-synch.json**: Synchronous version of the `if` dataset.
   - **ifdataset-else.json**: Dataset containing assertions for `if-else` conditions.
   - **ifdataset-else-synch.json**: Synchronous version of the `if-else` conditions dataset.
   - **ifdataset-!else.json**: Dataset handling `if-not-else` conditions.
   - **ifdataset-!else-synch.json**: Synchronous version of the `if-not-else` conditions dataset.
   - **ifdataset.json**: General dataset covering various `if-else` conditions for assertion generation.
   - **VERT_withRAG.json**: A variant of the main dataset, enhanced with **Retrieval-Augmented Generation (RAG)** techniques.

---

## 🎯 Summary
The **VERT** dataset provides a robust solution for improving hardware verification through automated assertion generation. By offering diverse, comprehensive, and synchronized datasets, VERT fine-tunes open-source LLMs to achieve high levels of correctness on **industry-standard SoC platforms**. It effectively balances the trade-off between performance and cost, making it a valuable resource for researchers and hardware engineers.
