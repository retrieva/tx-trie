# TX-trie

Tx: Succinct Trie Data structure

Tx is a library for a compact trie data structure. Tx requires 1/4 - 1/10 of the memory usage compared to the previous implementations, and can therefore handle quite a large number of keys (e.g. 1 billion) efficiently. A trie data structure supports exact matching and common prefix matching, which are used for natural language processing etc. Tx uses Level-Order Unary Degree Sequence (LOUDS) for trie representation.

## How to build

  $ ./autogen.sh
  $ ./configure
  $ make
