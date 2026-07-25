# EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization
## AIM
To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (e.g., ChatGPT, Gemini, Claude, Copilot) in a specific task: text summarization.

## Scenario:
You are part of a content curation team for an educational platform that delivers quick summaries of research papers to undergraduate students. Your task is to summarize a 500-word technical article on "The Basics of Blockchain Technology" using multiple AI platforms and prompting strategies.

## Zero-Shot Prompting
### Prompt: "The Basics of Blockchain Technology"
Summarize the following article.
give me in one paragraph
### Chat-GPT:
Blockchain is a decentralized, immutable digital ledger that records transactions securely across multiple participants without intermediaries. While it offers major opportunities such as transparency, efficiency, and security in sectors like finance, supply chain, healthcare, and governance, it faces challenges of scalability, privacy, regulatory uncertainty, and user adoption. Future directions include integration with artificial intelligence, interoperability across different blockchains, and the rise of decentralized finance (DeFi). Recent research highlights novel uses such as hybrid blockchains, social impact applications (e.g., refugee identity, donation tracking), blockchain–IoT integration, data marketplaces, carbon footprint tracking, and decentralized autonomous organizations (DAOs). Overall, blockchain holds vast potential to transform industries, but addressing technical, legal, and environmental hurdles is crucial for realizing a secure, transparent, and sustainable digital future

### Gemini:
Based on the article, blockchain technology is fundamentally a decentralized and distributed ledger system that securely and transparently records transactions across a network of participants. Built on cryptographic principles, it consists of a chain of blocks, with each block containing a set of transactions. These blocks are linked using cryptographic hashes, which ensures that the data is immutable and its integrity is maintained. This decentralized structure eliminates the need for a central authority or intermediary, as transactions are validated and agreed upon through a consensus mechanism among the network's participants.

### Claude:
This research paper examines blockchain technology's fundamentals, challenges, and applications across six domains through experimental studies. Blockchain operates as a decentralized, cryptographically-secured ledger system that eliminates intermediaries but faces significant challenges including scalability limitations, privacy concerns, regulatory uncertainty, and energy consumption issues. The authors conducted experiments on hybrid blockchain architectures (claiming 5,000 transactions per second), social impact applications like refugee identity management and fair trade tracking, IoT integration for enhanced security, blockchain-based data marketplaces with token incentives, carbon footprint tracking systems, and decentralized autonomous organizations (DAOs) for democratic governance. While the paper presents positive experimental results suggesting blockchain's potential across these domains, the findings appear based on small-scale tests that may not reflect real-world performance constraints, and many of the supposedly "novel" applications have been extensively explored in the blockchain community for years, raising questions about both the scalability claims and the novelty assertions made by the researchers.

### Copilot:
The article "The Basics of Blockchain Technology" introduces blockchain as a decentralized, immutable digital ledger system that securely records transactions across a distributed network. It explains how blockchain relies on cryptographic principles and consensus mechanisms to ensure data integrity without the need for a central authority. Each block contains a set of transactions linked by cryptographic hashes, forming a secure chain. The technology’s core strengths—transparency, security, and efficiency—make it transformative across industries like finance, healthcare, supply chain, and governance. Despite its promise, blockchain faces challenges such as scalability, privacy concerns, and regulatory hurdles, which must be addressed to unlock its full potential.
<h2>📊 Evaluation of Zero-Shot Summarization </h2>

<table border="1" cellspacing="0" cellpadding="8">
  <tr>
    <th>Criteria</th>
    <th>ChatGPT</th>
    <th>Gemini</th>
    <th>Claude</th>
    <th>Copilot</th>
  </tr>
  <tr>
    <td><b>Accuracy</b></td>
    <td>⭐⭐⭐⭐½ (High) – covers fundamentals, challenges, future uses clearly</td>
    <td>⭐⭐⭐⭐ (High) – correct fundamentals, but misses opportunities/future directions</td>
    <td>⭐⭐⭐⭐ (High) – technically accurate but over-critical and slightly biased</td>
    <td>⭐⭐⭐⭐ (High) – good fundamentals and applications, less detail on future</td>
  </tr>
  <tr>
    <td><b>Coherence</b></td>
    <td>⭐⭐⭐⭐½ (Very High) – smooth flow and well-organized</td>
    <td>⭐⭐⭐⭐ (High) – structured, but more definitional than summary-like</td>
    <td>⭐⭐⭐⭐ (High) – coherent but dense, more like a critique than summary</td>
    <td>⭐⭐⭐⭐ (High) – flows logically, simple structure</td>
  </tr>
  <tr>
    <td><b>Simplicity</b></td>
    <td>⭐⭐⭐⭐ (High) – clear, but dense with technical terms</td>
    <td>⭐⭐⭐½ (Moderate-High) – easy to follow but more textbook style</td>
    <td>⭐⭐⭐ (Moderate) – academic and critical tone, harder for undergrads</td>
    <td>⭐⭐⭐⭐ (High) – simple, undergraduate-friendly</td>
  </tr>
  <tr>
    <td><b>Speed</b></td>
    <td>⭐⭐⭐⭐⭐ (Fast, ~2s)</td>
    <td>⭐⭐⭐⭐½ (Fast, ~3s)</td>
    <td>⭐⭐⭐⭐ (Moderate, ~4s)</td>
    <td>⭐⭐⭐⭐½ (Fast, ~3s)</td>
  </tr>
  <tr>
    <td><b>User Experience (UX)</b></td>
    <td>⭐⭐⭐⭐½ (Well formatted, neat paragraph)</td>
    <td>⭐⭐⭐⭐ (Neat, but slightly long-winded)</td>
    <td>⭐⭐⭐½ (Dense, critique style, less user-friendly)</td>
    <td>⭐⭐⭐⭐ (Clean and readable)</td>
  </tr>
</table>

<p><b>Final Score (avg):</b><br>
• ChatGPT → 4.4<br>
• Gemini → 4.0<br>
• Claude → 3.8<br>
• Copilot → 4.1
</p>


## Few-Shot Prompting
### Prompt:
"Here are examples of summaries for technical articles. 
Example 1
Mini Article:
“Bitcoin uses blockchain technology to allow peer-to-peer payments without banks. Each transaction is stored in a public ledger that anyone can verify.”
Example 2
Mini Article:
“Smart contracts are programs stored on a blockchain. They run automatically when certain conditions are met, reducing the need for intermediaries in business deals.”

Now, summarize the following article."

### Chat-GPT:
Blockchain is a decentralized digital ledger that records transactions securely and transparently. It offers opportunities in finance, supply chains, healthcare, and governance, but faces challenges like scalability, privacy, and regulation. Future directions include AI integration, cross-blockchain interoperability, and decentralized finance (DeFi), with emerging uses in data marketplaces, IoT, carbon tracking, and decentralized organizations.
### Gemini:
Blockchain technology is a decentralized, distributed ledger that securely and transparently records transactions. It uses a chain of cryptographically linked blocks to create an immutable record, removing the need for intermediaries and offering opportunities to improve security and efficiency in sectors like finance, supply chain management, and healthcare.
### Claude:
Blockchain technology faces scalability and privacy challenges but shows promise across multiple sectors. Researchers tested hybrid blockchain systems that combine public and private networks, achieving faster transaction processing. They also explored blockchain applications for refugee identity management, supply chain transparency, carbon emissions tracking, and decentralized organizations, finding improved security and trust in each area.
### Copilot:
Blockchain is a decentralized digital ledger that records transactions securely and transparently across a network. It faces challenges like scalability, privacy, and regulation, but offers opportunities in finance, healthcare, supply chains, and governance. Future directions include integrating AI, enabling cross-chain interoperability, and expanding decentralized finance (DeFi) applications.

<h2>📊 Evaluation of Few-Shot Summarization </h2>

<table border="1" cellspacing="0" cellpadding="8">
  <tr>
    <th>Criteria</th>
    <th>ChatGPT</th>
    <th>Gemini</th>
    <th>Claude</th>
    <th>Copilot</th>
  </tr>
  <tr>
    <td><b>Accuracy</b></td>
    <td>⭐⭐⭐⭐½ (High) – captures fundamentals, challenges, opportunities, and future uses clearly</td>
    <td>⭐⭐⭐⭐ (High) – correct fundamentals, but misses future directions like DeFi and AI</td>
    <td>⭐⭐⭐⭐ (High) – accurate, includes experiments and applications, slightly research-heavy</td>
    <td>⭐⭐⭐⭐ (High) – accurate fundamentals and challenges, covers future directions well</td>
  </tr>
  <tr>
    <td><b>Coherence</b></td>
    <td>⭐⭐⭐⭐½ (Very High) – concise, well-structured paragraph</td>
    <td>⭐⭐⭐⭐ (High) – coherent but more definitional in tone</td>
    <td>⭐⭐⭐⭐ (High) – coherent, but leans academic rather than summary-like</td>
    <td>⭐⭐⭐⭐ (High) – flows smoothly, balanced style</td>
  </tr>
  <tr>
    <td><b>Simplicity</b></td>
    <td>⭐⭐⭐⭐ (High) – clear for undergrads, minimal jargon</td>
    <td>⭐⭐⭐½ (Moderate-High) – a bit textbook-like in style</td>
    <td>⭐⭐⭐ (Moderate) – dense and technical, less simple for undergrads</td>
    <td>⭐⭐⭐⭐ (High) – simple and easy to follow</td>
  </tr>
  <tr>
    <td><b>Speed</b></td>
    <td>⭐⭐⭐⭐⭐ (Fast, ~2s)</td>
    <td>⭐⭐⭐⭐½ (Fast, ~3s)</td>
    <td>⭐⭐⭐⭐ (Moderate, ~4s)</td>
    <td>⭐⭐⭐⭐½ (Fast, ~3s)</td>
  </tr>
  <tr>
    <td><b>User Experience (UX)</b></td>
    <td>⭐⭐⭐⭐½ (Neat and balanced length)</td>
    <td>⭐⭐⭐⭐ (Good format, slightly long-winded)</td>
    <td>⭐⭐⭐½ (Dense, reads more like a critique)</td>
    <td>⭐⭐⭐⭐ (Clean and readable)</td>
  </tr>
</table>

<p><b>Final Score (avg):</b><br>
• ChatGPT → 4.4<br>
• Gemini → 3.9<br>
• Claude → 3.8<br>
• Copilot → 4.1
</p>


## Chain-of-thought Prompting:
### Prompt:
"Let's think step-by-step. First, explain how blockchain works, then summarize its key applications."

### Chat-GPT:
How blockchain works — step-by-step

Create a transaction: A user signs a transaction with their private key (e.g., “Alice pays Bob 1 token”) and broadcasts it to the network.

Propagate & collect: Network nodes receive the transaction and pool it with other pending transactions.

Validate: Nodes check the transaction’s correctness (signatures, sufficient balance, format).

Consensus & block formation: A subset of nodes (miners/validators) bundle validated transactions into a block and run the network’s consensus (e.g., proof-of-work, proof-of-stake) to agree on that block.

Linking & immutability: Each block contains a cryptographic hash of the previous block, so once appended the block becomes tamper-evident—changing one block breaks every subsequent hash.

Finality & replication: Once the network accepts the block, it’s replicated to all full nodes; the ledger is updated and the transaction is considered (eventually) final.

Smart contracts (optional): If transactions invoke smart contracts, those programs run deterministically on-chain and automatically enforce agreed rules. 

Key applications — short summary

Payments & finance: Faster, cheaper peer-to-peer and cross-border transfers; infrastructure for tokens, stablecoins and DeFi services.

Supply chain & traceability: Tamper-proof provenance records so consumers and regulators can verify origin and handling.

Healthcare: Secure, auditable patient records and controlled data sharing while improving interoperability.

Governance & public services: Transparent records (e.g., voting, aid distribution) that reduce fraud and boost accountability.

IoT: Decentralized device identity, secure data exchange and improved interoperability between heterogeneous devices.

Data marketplaces: Tokenized marketplaces where data provenance, ownership and payments are enforced by smart contracts.

Environmental tracking / carbon credits: Immutable recording and trading of emissions or credits to support sustainability reporting.

Decentralized organizations (DAOs): On-chain governance structures that automate collective decision-making and resource allocation.
### Gemini:
How Blockchain Works
Blockchain technology functions as a secure and transparent distributed ledger system. Its operation is based on the following principles:


Structure of Blocks and Chains: The system is composed of a chain of "blocks," where each block contains a set of transactions. These blocks are linked together in chronological order using cryptographic hashes.



Immutability and Integrity: The use of cryptographic hashes to link blocks ensures the immutability and integrity of the data stored within the blockchain. This means that once a transaction is recorded, it cannot be altered or deleted, making the ledger tamper-proof.


Decentralization: The technology is decentralized, which eliminates the need for a central authority like a bank or government to manage and validate transactions.


Consensus Mechanism: Instead of a central authority, transactions are validated and agreed upon by consensus among the network's participants. This distributed agreement ensures that all copies of the ledger are consistent and accurate.

Key Applications of Blockchain
The article highlights a wide range of opportunities and applications for blockchain technology across various sectors:


Finance: It can be used to streamline cross-border transactions, reduce costs, and enhance transparency. The technology also enables the rise of Decentralized Finance (DeFi) applications for services like decentralized lending and stablecoins.



Supply Chain Management: Blockchain can improve traceability, authenticity, and efficiency in supply chains. This includes applications like providing transparency for fair trade products by tracking their journey from producer to consumer.





Healthcare: In healthcare, blockchain can enhance data interoperability, security, and patient privacy.


Governance: The technology has the potential to enhance transparency and reduce corruption in governance systems. It also facilitates the creation of Decentralized Autonomous Organizations (DAOs), which are governed by smart contracts and allow for collective, democratic decision-making.




Social Impact and Humanitarian Aid: Applications in this area include creating secure digital identity management systems for refugees and enabling transparent tracking of charitable donations from donor to recipient.






Internet of Things (IoT): When integrated with IoT, blockchain can improve the security, privacy, and interoperability of connected devices. It enables secure, decentralized data sharing and trust management within IoT ecosystems.



Environmental Sustainability: Blockchain can be used to develop systems that securely record and verify carbon footprints. This facilitates transparent carbon trading and promotes accountability in environmental efforts.





Data Marketplaces: The technology can be used to create decentralized marketplaces for securely and transparently trading data assets, while ensuring data privacy and ownership rights for individuals.
### Claude:
How Blockchain Works:
Blockchain is a distributed digital ledger that records transactions across multiple computers in a network. Each "block" contains a group of transactions and is cryptographically linked to the previous block, forming a "chain." When someone wants to make a transaction, the network participants (called nodes) must validate it through a consensus mechanism before adding it to the blockchain. Once recorded, the data becomes extremely difficult to alter because changing one block would require changing all subsequent blocks across the majority of the network.
Key Applications from the Research:
The paper examined six main blockchain applications through experiments:

Hybrid Systems - Combining public and private blockchains to balance transparency with privacy, reportedly achieving higher transaction speeds
Social Impact - Using blockchain for refugee identity documents, tracking fair trade products, and monitoring charitable donations to increase transparency and reduce fraud
IoT Integration - Securing Internet of Things devices by recording their data exchanges on blockchain networks
Data Marketplaces - Creating platforms where people can buy and sell data securely while maintaining ownership rights
Carbon Tracking - Recording carbon emissions data to enable transparent environmental reporting and carbon credit trading
Decentralized Organizations - Enabling groups to make collective decisions through blockchain-based voting systems without traditional management structures

However, the research acknowledges significant challenges including slow transaction processing, high energy consumption, regulatory uncertainty, and complex user interfaces that limit widespread adoption.
### Copilot:
🔧 How Blockchain Works
Blockchain is a decentralized digital ledger that records transactions across a network of computers. Each transaction is grouped into a “block,” and these blocks are linked together chronologically to form a “chain.” Here's how it functions:

Decentralization: No single authority controls the data; instead, it's distributed across many nodes.

Immutability: Once data is recorded in a block and added to the chain, it cannot be altered without changing all subsequent blocks.

Consensus Mechanisms: Transactions are validated by network participants through algorithms like Proof of Work or Proof of Stake.

Cryptographic Security: Each block contains a cryptographic hash of the previous block, ensuring data integrity and resistance to tampering.

🌍 Key Applications of Blockchain
Blockchain’s unique properties make it valuable across various sectors:

Finance: Enables secure, transparent, and efficient cross-border payments and decentralized finance (DeFi) services.

Supply Chain: Enhances traceability and authenticity of goods, reducing fraud and improving logistics.

Healthcare: Secures patient data, improves interoperability, and ensures privacy.

Governance: Promotes transparency and accountability in public services and voting systems.

Environmental Tracking: Facilitates carbon footprint tracking and sustainable practices.

Social Impact: Supports identity management for refugees, donation transparency, and fair trade verification.

In short, blockchain is not just a tech buzzword—it’s a foundational shift in how trust and data are managed across digital ecosystems.

<h2>📊 Evaluation of Chain-of-Thought Summarization (“The Basics of Blockchain Technology”)</h2>

<table border="1" cellspacing="0" cellpadding="8">
  <tr>
    <th>Criteria</th>
    <th>ChatGPT</th>
    <th>Gemini</th>
    <th>Claude</th>
    <th>Copilot</th>
  </tr>
  <tr>
    <td><b>Accuracy</b></td>
    <td>⭐⭐⭐⭐⭐ (Very High) – detailed step-by-step and broad applications, highly factual</td>
    <td>⭐⭐⭐⭐ (High) – correct fundamentals and wide applications, slightly repetitive</td>
    <td>⭐⭐⭐⭐ (High) – accurate, includes experimental context, but critical tone</td>
    <td>⭐⭐⭐⭐ (High) – accurate and balanced, though less detailed than ChatGPT</td>
  </tr>
  <tr>
    <td><b>Coherence</b></td>
    <td>⭐⭐⭐⭐⭐ (Very High) – clear structure: steps then applications</td>
    <td>⭐⭐⭐⭐ (High) – coherent, organized by sections, easy to follow</td>
    <td>⭐⭐⭐⭐ (High) – structured, but reads like a research report</td>
    <td>⭐⭐⭐⭐½ (High) – well formatted with icons and sections, flows smoothly</td>
  </tr>
  <tr>
    <td><b>Simplicity</b></td>
    <td>⭐⭐⭐⭐ (High) – technical but explained clearly for undergrads</td>
    <td>⭐⭐⭐½ (Moderate-High) – more academic style, long explanations</td>
    <td>⭐⭐⭐ (Moderate) – dense, research-heavy, less accessible for undergrads</td>
    <td>⭐⭐⭐⭐½ (Very High) – simple, clean, with visuals (🔧🌍), very user-friendly</td>
  </tr>
  <tr>
    <td><b>Speed</b></td>
    <td>⭐⭐⭐⭐ (Moderate, ~4s)</td>
    <td>⭐⭐⭐⭐½ (Fast, ~3s)</td>
    <td>⭐⭐⭐⭐ (Moderate, ~4s)</td>
    <td>⭐⭐⭐⭐½ (Fast, ~3s)</td>
  </tr>
  <tr>
    <td><b>User Experience (UX)</b></td>
    <td>⭐⭐⭐⭐½ (Detailed, structured with lists, very clear)</td>
    <td>⭐⭐⭐⭐ (Readable, but long sections of text)</td>
    <td>⭐⭐⭐½ (Dense, more academic tone than summary style)</td>
    <td>⭐⭐⭐⭐½ (Engaging with emojis/icons, good readability)</td>
  </tr>
</table>

<p><b>Final Score (avg):</b><br>
• ChatGPT → 4.6<br>
• Gemini → 4.1<br>
• Claude → 3.8<br>
• Copilot → 4.4
</p>





## Role-based Prompting:
### Prompt:
"You are a professional content curator for students. Summarize the article in simple terms." 
### Chat-GPT:
Blockchain is like a digital notebook shared by many people where transactions are recorded in blocks and linked together so they cannot be easily changed. It removes the need for middlemen like banks, offering benefits such as faster payments in finance, better tracking in supply chains, secure patient data in healthcare, and transparent records in governance. At the same time, it faces challenges like slow transaction speeds, privacy risks, and unclear government regulations. In the future, blockchain may work with artificial intelligence, allow different blockchains to connect, and support new financial services through decentralized finance (DeFi). Researchers are also exploring its use for refugee identity, carbon footprint tracking, data marketplaces, and decentralized organizations. Overall, blockchain promises a more secure, transparent, and efficient digital world but still needs to overcome major hurdles to reach its full potential
### Gemini:
The research paper explores blockchain technology, defining it as a decentralized and immutable distributed ledger system that offers a secure and transparent platform for digital transactions. While it presents significant opportunities, the technology faces critical challenges, including issues with scalability, privacy, and evolving regulatory concerns. Despite these hurdles, blockchain offers transformative potential across numerous sectors by enhancing transparency, security, and efficiency in areas like finance, supply chain management, healthcare, and governance. The paper investigates novel applications such as creating hybrid blockchain architectures , using blockchain for social impact like transparent donation tracking , integrating with the Internet of Things (IoT) , enabling secure data marketplaces , tracking carbon footprints , and facilitating decentralized autonomous organizations (DAOs). Looking forward, the technology's future directions include its integration with artificial intelligence (AI) , achieving interoperability between different blockchain networks , and the continued rise of decentralized finance (DeFi) applications. The paper concludes that further research and collaboration are necessary to overcome the existing challenges and fully unlock blockchain's potential to build a more transparent, secure, and decentralized future.
### Claude:
Blockchain is a digital ledger system that works like a shared, tamper-proof notebook where transactions are recorded across multiple computers, making it secure but currently facing major challenges including slow processing speeds, high energy consumption, privacy concerns, and complex user interfaces. Researchers tested blockchain applications in six areas - hybrid public-private systems for faster transactions, refugee identity management, fair trade tracking, charitable donation transparency, IoT device security, environmental carbon tracking, and decentralized organizational decision-making - finding promising results in small-scale experiments that showed improved security, transparency, and trust. However, these experimental findings may not translate to real-world performance at scale, and many of the studied applications have been explored for years without achieving mainstream adoption due to persistent technical, regulatory, and usability barriers that prevent blockchain from becoming widely accessible to ordinary users.
### Copilot:
Blockchain is a special kind of digital record system that keeps track of transactions in a secure and transparent way, without needing a central authority like a bank. It’s useful in many areas—like finance, healthcare, and supply chains—because it helps make things more trustworthy and efficient. But it’s not perfect yet. It struggles with handling lots of data quickly, keeping private information safe, and fitting into existing laws. The article also explores exciting future uses, like combining blockchain with AI, helping refugees with digital IDs, tracking donations, and even monitoring carbon footprints to fight climate change. Overall, blockchain has big potential, but it needs more work and collaboration to become widely used.

<h2>📊 Evaluation of Role-Based Summarization</h2>

<table border="1" cellspacing="0" cellpadding="8">
  <tr>
    <th>Criteria</th>
    <th>ChatGPT</th>
    <th>Gemini</th>
    <th>Claude</th>
    <th>Copilot</th>
  </tr>
  <tr>
    <td><b>Accuracy</b></td>
    <td>⭐⭐⭐⭐½ (High) – accurate fundamentals, challenges, and future directions well covered</td>
    <td>⭐⭐⭐⭐ (High) – detailed and correct, but lengthy and academic</td>
    <td>⭐⭐⭐⭐ (High) – accurate but leans toward critique of research limitations</td>
    <td>⭐⭐⭐⭐ (High) – correct fundamentals, applications, and future directions</td>
  </tr>
  <tr>
    <td><b>Coherence</b></td>
    <td>⭐⭐⭐⭐½ (Very High) – smooth flow, clear explanations with analogies</td>
    <td>⭐⭐⭐⭐ (High) – well structured, but reads like a research abstract</td>
    <td>⭐⭐⭐⭐ (High) – coherent, but dense and critical in tone</td>
    <td>⭐⭐⭐⭐½ (Very High) – clear, engaging, flows logically</td>
  </tr>
  <tr>
    <td><b>Simplicity</b></td>
    <td>⭐⭐⭐⭐½ (Very High) – very student-friendly, analogy of “digital notebook” works well</td>
    <td>⭐⭐⭐½ (Moderate-High) – heavy terminology, less accessible for undergrads</td>
    <td>⭐⭐⭐ (Moderate) – complex, technical, harder for undergrads</td>
    <td>⭐⭐⭐⭐ (High) – simplified but still covers advanced examples</td>
  </tr>
  <tr>
    <td><b>Speed</b></td>
    <td>⭐⭐⭐⭐⭐ (Fast, ~2s)</td>
    <td>⭐⭐⭐⭐ (Moderate, ~4s)</td>
    <td>⭐⭐⭐⭐ (Moderate, ~4s)</td>
    <td>⭐⭐⭐⭐½ (Fast, ~3s)</td>
  </tr>
  <tr>
    <td><b>User Experience (UX)</b></td>
    <td>⭐⭐⭐⭐½ (Very clear, approachable, student-focused)</td>
    <td>⭐⭐⭐⭐ (Readable but dense and long)</td>
    <td>⭐⭐⭐½ (Dense, academic, less user-friendly)</td>
    <td>⭐⭐⭐⭐ (Readable, nicely simplified)</td>
  </tr>
</table>

<p><b>Final Score (avg):</b><br>
• ChatGPT → 4.6<br>
• Gemini → 4.0<br>
• Claude → 3.7<br>
• Copilot → 4.3
</p>




## Result

Thus, we evaluated four prompting techniques (Zero-Shot, Few-Shot, Chain-of-Thought, Role-Based) across four AI platforms (ChatGPT, Gemini, Claude, Copilot) for text summarization. ChatGPT consistently delivered the most accurate, coherent, and student-friendly outputs, followed by Copilot, while Gemini was more textbook-like and Claude leaned research-heavy. Overall, Role-Based and Chain-of-Thought prompting with ChatGPT gave the best balance of performance.
