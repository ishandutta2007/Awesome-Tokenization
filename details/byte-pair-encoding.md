# Byte-Pair Encoding (BPE)\n\n### Overview
Byte-Pair Encoding (BPE) is a bottom-up subword tokenization algorithm originally designed for data compression. In NLP, BPE builds a vocabulary of frequent characters and character combinations.

### Algorithmic Steps
1. Initialize the vocabulary with all unique base characters/bytes in the training corpus.
2. Tokenize the corpus at the character level.
3. Count the frequency of all adjacent token pairs in the corpus.
4. Merge the most frequent pair and add it to the vocabulary.
5. Repeat steps 3–4 until the target vocabulary size is reached.

### Diagram: BPE Merging Process
```mermaid
stateDiagram-v2
    State1: Base Vocab: [a, b, c, d]
    State2: Iteration 1: Merge 'ab' -> Vocab: [a, b, c, d, ab]
    State3: Iteration 2: Merge 'ab' + 'c' -> Vocab: [a, b, c, d, ab, abc]
    
    [*] --> State1
    State1 --> State2 : Find most frequent pair 'ab'
    State2 --> State3 : Find most frequent pair 'abc'
```

### Back-link
[← Back to README](../README.md)
