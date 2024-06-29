## This phase consists of creating custom Input/Output Json Schema for the MAS

- The problem with LangChain and LangGraph was building things from scratch.
- Used CrewAI framework which is built on LangChain for Multi-Agent System with a Moderator 

# Inference Outputs:

Example-1:

### Input_data -->

``` python
input_data = {
    "prompts": [
        ["what is happening in this image?", ["/content/Word Embeddings.png"]],
        #["give me an essay related to this image", ["/content/WhatsApp Image 2024-06-27 at 8.21.50 PM.jpeg"]],
        ["also explain me its importance with respect to NLP"]
    ],
    "output_format": "JSON",
    "example_output_structure": "{pic1: [fruit1, colorA] , pic2: [fruit2, colorX], pic3: [fruit3, colorY]}",
    "max_iterations": 5
}
```

Output -->

```json
{
  "image_analysis": {
    "Word_Embeddings.png": [
      {
        "description": "The image depicts a diagram illustrating the concept of word embeddings in natural language processing (NLP). There are several circles representing different words, with lines connecting them to indicate relationships. The words are positioned in a way that shows clustering of similar words based on context and meaning.",
        "objects": ["circles", "lines", "words"],
        "colors": ["various colors representing different clusters"],
        "context": "Word embeddings are a type of word representation that allows words with similar meaning to have a similar representation. They are a crucial part of NLP as they help in capturing the context of words, their meaning, and their relationship with other words."
      }
    ]
  }
```
