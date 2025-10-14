# RAG

7 Types of Chunking Strategies in RAG
Several different chunking strategies are employed in RAG chunking, each with its own advantages and use cases:

### 1. Fixed Size Chunking 
Fixed-size chunking is a straightforward approach where text is divided into uniform chunks based on a predefined character count.  

For example, you might split a document into chunks of 500 tokens each, regardless of whether the chunk ends mid-sentence or across paragraphs. 

To mitigate this, an overlap feature can be introduced, where a certain number of tokens or characters from the end of one chunk is repeated at the start of the next. This helps preserve context across chunks and prevents loss of meaning at the boundaries. 

**Advantages**

Simplicity: Easy to implement and understand. 
Efficiency: Fast processing, especially for large datasets. 
Consistency: Uniform chunk sizes across documents. 
Low computational requirements: Doesn't need complex algorithms or models. 

**Disadvantages**

Context fragmentation: May split sentences or logical units of information. 
Inflexibility: Doesn't account for varying content density or structure. 
Potential information loss: Important context might be split across chunks. 
Sub-optimal for heterogeneous content: Less effective for documents with varying structures or lengths. 

### 2. Recursive-Based Chunking 
Recursive Character Text Splitting is a more adaptive approach that breaks text into chunks by using multiple separators in a specified order. It tries each separator (like paragraphs, sentences, or specific markers) in a descending order of importance to find the most meaningful boundaries in the text.  

Partner with Us for Success
Experience seamless collaboration and exceptional results.

Let’s Connect
The method recursively splits text until the chunks meet a specified size, preserving logical structure. 

For example, in a Python code document, it may first try splitting by class definitions, then function definitions, and finally by line breaks. This ensures that chunks are as meaningful as possible. 

**Advantages**

Meaningful Chunks: Preserves semantic and structural integrity by splitting at logical points like paragraphs or sections. 
Flexibility: Adapts to various types of content by using multiple separators, making it useful for both text and code. 
Fine-Grained Control: Allows precise control over chunk size and overlap to fit specific needs without losing important context. 
Handles Complex Content: Particularly useful for structured or hierarchical content like technical documents or programming code. 

**Disadvantages**

Increased Complexity: Requires a more complex setup compared to fixed-size chunking. 
Higher Computational Overhead: Recursive calls and multiple separator checks can slow down processing for large texts. 
Dependence on Separators: If the text lacks clear separators, it may not split effectively, leading to larger or uneven chunks. 
Slower Performance: This can be slower for very large datasets compared to simpler chunking methods. 

### 3. Document-Based Chunking 
Document-based chunking treats the entire document as a single chunk or divides it as little as possible. This method aims to preserve the full structure and context of the document, making it ideal for content where splitting may disrupt the flow or meaning. 

Best suited for tasks that require processing large, detailed texts, such as legal, medical, or scientific document analysis. It ensures that key information and context remain intact across the document. 

For instance, a legal document might be chunked by individual charges, with each charge treated as a chunk. This method maintains the document's structural integrity and ensures that no important legal context is lost. 

**Advantages**

Full Context Preservation: Retains the entire document’s flow and meaning without cutting through critical sections. 
Ideal for Structured Texts: Works well for highly structured documents like legal contracts or medical reports. 
Simplicity: Straightforward to implement without complex chunking rules. 

**Disadvantages**

Scalability Issues: Not ideal for large documents that exceed token or memory limits, as they may be too big to process in a single chunk. 
Reduced Efficiency: Handling large documents as a whole can lead to inefficiencies and higher resource consumption. 
Limited Specificity: Lacks granularity, making it difficult to extract or retrieve specific sections or details within the document. 

### 4. Semantic Chunking 
Semantic chunking breaks text into chunks based on meaning rather than fixed sizes. It ensures that each chunk contains coherent and relevant information by analyzing shifts in the text’s semantic structure. This is typically done by measuring differences in sentence embeddings, which represent the meaning of sentences mathematically. 

For example, the chunker splits the text when it detects a significant change in meaning between two sentences based on their embeddings. Thresholds can be set to control when this break happens, ensuring each chunk is logically connected. 

**Advantages**

Preserves meaning: Chunks are created around logical content breaks, ensuring coherent units of information. 
Adaptable to diverse content: Works well with documents of varying topics or sections, such as research papers or technical documents. 
Improves retrieval accuracy: Chunks maintain their semantic integrity, making responses to queries more relevant. 

**Disadvantages**

Complex setup: Requires advanced techniques to measure semantic shifts between sentences. 
Higher computational cost: Analyzing meaning differences can be resource-intensive, especially for longer documents. 
Threshold tuning: The quality of chunking depends on setting the right threshold, which may vary for different types of content or domains.  

### 5. Token-Based Chunking
Token-based chunking splits text based on a predefined number of tokens (words or subwords) rather than characters or sentences. Tokens are the smallest meaningful units of text, and the chunk size is controlled by a set token limit.

For example, a document might be divided into chunks of 300 tokens each, ensuring that each chunk is within a model’s token limit for processing, even if it cuts across sentences or paragraphs.

**Advantages**
Optimized for language models: Ensures chunks stay within the token limits of models like GPT, improving processing efficiency.
Precise control over chunk size: Allows for fine-tuning the number of tokens per chunk to match model requirements.
Consistency across content: Divides text into consistent token counts, making processing easier for large datasets.
Partner with Us for Success
Experience seamless collaboration and exceptional results.

Let’s Connect
**Disadvantages**
Context fragmentation: May break sentences or paragraphs mid-way, leading to incomplete information in chunks.
Ignores semantic structure: Focuses only on token count, potentially losing important context or meaning.
Limited flexibility: This doesn't account for varying content density or the natural breaks in text, which may reduce chunk coherence.

### 6. Sentence-Based Chunking
Sentence-based chunking divides text into full sentences, ensuring that each chunk contains complete thoughts. This method helps preserve the logical flow of information by splitting natural sentence boundaries.

For example, a document might be broken into chunks where each contains 5 to 10 sentences, maintaining the semantic integrity of each chunk while keeping the size manageable.

**Advantages**

Preserves context: Each chunk contains full sentences, ensuring no loss of meaning or disruption in the flow of information.
Better readability: Chunks are more coherent and readable, making it easier for models or users to process them.
Natural division: The text is split at logical points, preventing chunks from cutting through ideas mid-sentence.

**Disadvantages**

Variable chunk sizes: Depending on sentence length, chunks can vary significantly in size, making it harder to control chunk consistency.
Inefficient for long sentences: In texts with very long sentences, chunks may exceed token limits or contain too much information in a single chunk.
Less control over chunk size: Chunking based on sentences may result in uneven chunks, which could affect performance in models with strict size limits.

### 7. Agentic Chunking
Agentic chunking breaks down a text into smaller, semantically meaningful sections based on the roles or tasks an AI agent needs to perform. Instead of treating a document or passage as a uniform whole, agentic chunking organizes content into "actionable" chunks—each optimized for a specific purpose, such as answering a question, summarizing, or making decisions. These chunks are structured to give the AI clear cues about the task, making it more efficient and goal-oriented when processing information.

For example, if a document describes a process, agentic chunking would split the text into task-relevant parts like "step 1: preparation," "step 2: execution," and "step 3: conclusion," with each part mapped to a specific agent action or goal.

**Advantages**

Task-Oriented Efficiency: Helps optimize the AI’s performance by tailoring chunks to specific tasks or actions, reducing confusion and improving decision-making.
Better Focus on Relevant Data: The AI can hone in on exactly what it needs for each task, leading to more accurate responses or analysis.
Flexibility: Offers adaptability to a wide range of use cases, such as answering questions, summarizing, or performing tasks based on predefined roles.

**Disadvantages**

Complex Setup: Requires clear definitions of agent roles and task-specific chunking rules, which may involve significant setup time and effort.
Over-Specialization: Risk of oversimplifying or fragmenting complex documents into overly specific tasks, potentially missing broader patterns or nuances.
May Lose Global Context: Since each chunk is optimized for a specific task, there’s a risk of losing the overall context of the document, which could affect the quality of holistic tasks like summarization.


### Links

https://github.com/HKUDS/RAG-Anything

https://github.com/aurelio-labs/semantic-chunkers
