# System Components

This contain 5 main parts.

### Component 1: Documents

These are the knowledge source.

Examples:

- GDPR Article 6
- GDPR Article 17
- DPDP Act sections
- Cookie policies

Example text:

*Personal data processing requires lawful basis such as consent or legitimate interest.*

These are uploaded to your system.

### Component 2: Document Processing

AI cannot read giant documents efficiently.

So we chunk them.

Example:

Original document:

- Page 1
- Page 2
- Page 3

Split into chunks:

- chunk1
- chunk2
- chunk3
- chunk4

Typical chunk size:

*500 tokens*

Reason:

*LLMs work better with smaller pieces.*

### Component 3: Embeddings

This is where AI magic starts.

Text is converted into numbers.

Example:

*"User data must be encrypted"*

Becomes:

[0.23, -0.44, 0.88, 0.12, ...]

This numeric representation is called an embedding.

Embeddings allow semantic search.

Meaning:

Query:

- "Is storing email allowed?"

AI finds related text like:

- "Processing personal data requires consent"

Even if words differ.

### Component 4: Vector Database

Embeddings are stored in a vector database.

Example database entry:

*Vector: [0.23, -0.44, 0.88...]*

Text:
"Personal data requires consent."

Source:
**GDPR Article 6**

When user asks a question:
1. Query converted to embedding
2. Vector DB finds similar vectors
3. Returns relevant document chunks

So AI sees only relevant information.

### Component 5: LLM (Large Language Model)

Now AI generates the final answer.

Input to LLM:

User question

Relevant regulation text

Example prompt:

You are a compliance expert.

Question:
Can I store user email without consent?

Relevant regulation:
Personal data processing requires lawful basis such as consent.

Explain the compliance risk clearly.

Output:

Risk Level: High

Explanation:
Email is personal data under GDPR. Processing it requires a lawful basis such as consent.

Recommendation:
Add consent checkbox before collecting emails.