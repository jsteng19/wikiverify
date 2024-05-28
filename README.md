# wikiverify

This project explores using LLMs to verify that a cited source supports a passage of text in tertiary-source research material such as Wikipedia articles. Many Wikipedia articles cite reliable sources, but do not include the supporting passage of text directly in their reference. Finding the direct supporting material can be tedious when the source is a book, academic paper, or even a news article.

The core idea of the project is to use embedding to vectorize chunks of text, then use similarity search to find chunks relevant to the supported text in question. Feeding this context to a generative model (GPT) can yield a concise supporting passage of text or determine that there are no directly supporting passages.

Using recursive chunking, even sources containing millions of tokens can be efficiently searched .

Roadmap:

 - Use a similarity score cutoff to determine chunks in context
 - Explore
   different semantic chunking methods for large sources
   Adverse testing: test related but unsupported claims

## Requirements

langchain v0.0.354 \
    openai v1.6.1 \
pinecone-client v3.1.0 \
tiktoken v0.5.2
