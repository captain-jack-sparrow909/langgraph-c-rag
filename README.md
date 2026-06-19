### flow:
1. loading of documents + chunking + embedding + storing in chroma db  - all of this handled in ingestion.py

2. defining how the state would like in state.py file

3. as shown in the diagram, of the nodes is retrieve node is first, we'll be implementing that one, this node is responsible for getting the question that the user asked from the state and then search for relevant documents using chroma retriever and add it to state; this node is implemented in /nodes/retrive.py file

4. now we implement the document grader node, it'll iterate over the docs to determine whether those are indeed relevant to the question or not

5. web search node

6. Generation node: when we've all the filtered docs and also performing search query for question that we want to answer






Loaders for loading data from web, pdf etc:
Loader → [Document, Document, ...]
           ↓
      TextSplitter → [smaller Document chunks]
           ↓
      Embeddings + VectorStore (stores page_content, indexes metadata)
           ↓
      Retriever → returns relevant [Document, Document, ...]
           ↓
      LLM chain (uses page_content as context)

sample Document: Document(page_content="Paris is the capital of France.", metadata={"topic": "geography"}),




diagram of C-RAG: image.png
