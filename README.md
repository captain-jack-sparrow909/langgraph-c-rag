### flow:
1. loading of documents + chunking + embedding + storing in chroma db  - all of this handled in ingestion.py

2. defining how the state would like in state.py file

3. as shown in the diagram, of the nodes is retrieve node is first, we'll be implementing that one, this node is responsible for getting the question that the user asked from the state and then search for relevant documents using chroma retriever and add it to state; this node is implemented in /nodes/retrive.py file

4. now we implement the document grader node, it'll iterate over the docs to determine whether those are indeed relevant to the question or not







diagram of C-RAG: image.png
