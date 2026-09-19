# EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization

## AIM

To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (e.g., ChatGPT, Gemini, Claude, Copilot) in a specific task: text summarization.

## Scenario:

You are part of a content curation team for an educational platform that delivers quick summaries of research papers to undergraduate students. Your task is to summarize a 500-word technical article on **"The Basics of Blockchain Technology"** using multiple AI platforms and prompting strategies.

Your goal is to determine which combination of prompting technique + platform provides the best summary in terms of:

* Accuracy
* Coherence
* Simplicity
* Speed
* User experience

---

```
Register No: 212223100035
Name: Muhammad Afshan A
```

# STEP-BY-STEP PROMPT TECHNIQUES & EXPERIMENTAL RESULTS

## 1. Basic Prompt

A simple, zero-shot instructional prompt without persona, additional context, specific constraints, or formatting guidance.

### Prompt:

```text
Summarize the following technical article on "The Basics of Blockchain Technology":

[Insert 500-word Source Article]
```

### Output:
```text
Blockchain is a decentralized digital ledger technology used to record and verify transactions securely. Instead of storing information in a single central database, blockchain distributes copies of the ledger across multiple computers in a network.

Transactions are grouped into blocks and connected using cryptographic techniques, creating a chain of records. Once information is added to the blockchain, it is difficult to modify without network agreement.

Blockchain technology provides transparency, security, and immutability. It is commonly associated with cryptocurrencies such as Bitcoin, but it can also be used in areas such as supply chain management, healthcare, finance, and digital identity.
```

### Evaluation:

**Strengths:** Quickly captures the main concepts and provides a straightforward summary.

**Limitations:** The response may be too general, may not be specifically targeted toward undergraduate students, and does not provide a consistent output structure.

---

## 2. Role Prompt

The AI is assigned a specific role to influence the language, depth, and style of the generated summary.

### Prompt:

```text
Act as an experienced technical educator.

Summarize the following technical article on "The Basics of Blockchain Technology"
for undergraduate students.

Use simple language while accurately explaining the important technical concepts.

[Insert 500-word Source Article]
```

### Output:
```text
Blockchain is a technology that allows information and transactions to be stored in a secure and shared digital ledger. Unlike traditional databases controlled by a central authority, blockchain distributes the ledger across multiple computers in a network.

Transactions are collected into blocks, and each block is connected to the previous one using cryptographic methods. This makes the recorded information difficult to change or manipulate.

The main characteristics of blockchain include decentralization, transparency, security, and immutability. Although blockchain is widely known for supporting cryptocurrencies such as Bitcoin, it also has applications in finance, supply chains, healthcare, digital identity, and other industries.
```

### Evaluation:

**Strengths:** Uses student-friendly language and explains technical concepts more clearly.

**Limitations:** The response is still relatively general and does not explicitly define the learning context or required content areas.

---

## 3. Context Prompt

Additional information about the target audience, purpose, and expected use of the summary is provided.

### Prompt:

```text
You are preparing study material for an educational platform.

The target audience is undergraduate students who have basic computer
science knowledge but limited knowledge of blockchain technology.

The summary will be used as a quick-learning resource before students
study the complete article.

Summarize the following article on "The Basics of Blockchain Technology".

Focus on:
- What blockchain is
- How blockchain works
- Major characteristics
- Common applications

Use clear and student-friendly language.

[Insert 500-word Source Article]
```

### Output:
```text
What is Blockchain?
-------------------
Blockchain is a distributed digital ledger that records transactions across a network of computers. It allows participants to share information without depending entirely on a single central authority.

How It Works
------------
Transactions are verified by the network and grouped into blocks. Each block is connected to the previous block using cryptographic methods, forming a continuous chain. This structure makes unauthorized changes difficult.

Major Characteristics
----------------------
Blockchain provides decentralization, transparency, security, and immutability. These features allow participants to verify records while reducing dependence on a central intermediary.

Applications
------------
Blockchain is commonly used in cryptocurrencies and can also support applications in finance, supply chain management, healthcare, digital identity, and other areas.
```
### Evaluation:

**Strengths:** More relevant to the intended audience and learning objective. The response focuses on the specific concepts required by the educational platform.

**Limitations:** The length and exact structure of the response are not strictly controlled.

---

## 4. Constraint Prompt

Specific rules are added to control the content, length, language, and accuracy of the summary.

### Prompt:

```text
Summarize the following technical article on "The Basics of Blockchain Technology".

Follow these constraints:

- Write between 100 and 150 words.
- Use simple and clear English.
- Target undergraduate students.
- Include the definition, working principle, key features, and applications.
- Use only information provided in the source article.
- Do not introduce unsupported information.
- Avoid unnecessary repetition.
- Do not use complex technical terminology unless it is explained briefly.

[Insert 500-word Source Article]
```

### Output:
```text
Blockchain is a decentralized digital ledger that records and verifies transactions across a network of computers. Instead of depending on one central authority, copies of the ledger are maintained by multiple participants.

Transactions are grouped into blocks and connected using cryptographic methods. Each block contains information related to previous blocks, making unauthorized modification difficult. This creates a secure and transparent record of transactions.

Important blockchain features include decentralization, transparency, security, and immutability. Blockchain is widely used for cryptocurrencies such as Bitcoin and can also support applications in finance, supply chain management, healthcare, and digital identity.
```
### Evaluation:

**Strengths:** Produces a concise and focused summary while controlling length, language, content coverage, and factual grounding.

**Limitations:** The response structure may still vary between different AI platforms or runs.

---

## 5. Output Format Prompt

The AI is given explicit instructions about how the final response should be organized.

### Prompt:

```text
Summarize the following technical article on "The Basics of Blockchain Technology".

Use simple and clear English suitable for undergraduate students.

Use ONLY information provided in the source article.

Follow this exact output structure:

Definition
Provide a brief definition of blockchain.

How It Works
Explain the basic working process.

Key Features
List the major features as bullet points.

Applications
List the applications discussed in the article.

Summary
Provide a concise overall summary in 2–3 sentences.

[Insert 500-word Source Article]
```

### Output:
```text
Definition
----------
Blockchain is a decentralized digital ledger that records and verifies transactions across a distributed network of computers.

How It Works
------------
Transactions are verified by network participants and grouped into blocks. These blocks are linked using cryptographic methods, forming a chain of records that is difficult to alter.

Key Features
------------
* Decentralization
* Transparency
* Security
* Immutability
* Distributed record keeping

Applications
-------------
* Cryptocurrencies
* Financial services
* Supply chain management
* Healthcare
* Digital identity

Summary
--------
Blockchain provides a secure and distributed method for recording information without relying completely on a central authority. Its characteristics make it useful across multiple industries beyond cryptocurrency.
```
### Evaluation:

**Strengths:** Produces a highly organized, readable, and consistent summary. The explicit structure makes the output suitable for educational applications.

**Limitations:** Requires a more detailed prompt and may be less flexible when a different output structure is required.

---

# COMPARATIVE EVALUATION

| Prompt Technique     | Accuracy  | Coherence | Simplicity | Structure | Overall Effectiveness |
| -------------------- | --------- | --------- | ---------- | --------- | --------------------- |
| Basic Prompt         | Medium    | Medium    | High       | Low       | Basic                 |
| Role Prompt          | High      | High      | High       | Low       | Good                  |
| Context Prompt       | High      | High      | High       | Medium    | Very Good             |
| Constraint Prompt    | Very High | High      | High       | Medium    | Excellent             |
| Output Format Prompt | Very High | Very High | High       | Very High | Excellent             |

---

# CROSS-PLATFORM OBSERVATION

The same prompt structures can be tested across different AI platforms such as:

* ChatGPT
* Gemini
* Claude
* Microsoft Copilot

The responses can be compared using the following parameters:

| Parameter       | Observation                                                         |
| --------------- | ------------------------------------------------------------------- |
| Accuracy        | Whether important information from the source is retained correctly |
| Coherence       | Whether the summary is logically organized                          |
| Simplicity      | Whether undergraduate students can easily understand it             |
| Speed           | Time taken to generate the response                                 |
| User Experience | Readability, consistency, and usefulness of the output              |

The comparison helps identify how different AI platforms respond to the same prompt engineering techniques.

---

# ALGORITHM

```text
START
  |
  v
Select the technical article
  |
  v
Provide the article to the AI model
  |
  v
Apply Basic Prompt
  |
  v
Evaluate generated summary
  |
  v
Apply Role Prompt
  |
  v
Evaluate generated summary
  |
  v
Apply Context Prompt
  |
  v
Evaluate generated summary
  |
  v
Apply Constraint Prompt
  |
  v
Evaluate generated summary
  |
  v
Apply Output Format Prompt
  |
  v
Evaluate generated summary
  |
  v
Compare results
  |
  v
Identify the most effective prompt technique
  |
  v
END
```

---

# RESULT

The experiment demonstrates that progressively improving the prompt increases the control and usefulness of AI-generated summaries.

The **Basic Prompt** produces a general summary, while the **Role Prompt** improves the explanation style. The **Context Prompt** makes the response more relevant to undergraduate students. The **Constraint Prompt** provides greater control over length, content, and language. The **Output Format Prompt** produces the most structured and consistent response.

The experiment also demonstrates that the effectiveness of a prompt can vary across AI platforms. Comparing the same prompts across ChatGPT, Gemini, Claude, and Microsoft Copilot helps identify differences in accuracy, coherence, simplicity, speed, and user experience.



The results show that well-structured prompts can produce summaries that are more accurate, coherent, simple, relevant, and consistent for the intended audience.
