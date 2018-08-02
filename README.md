# TX-trie

Tx: Succinct Trie Data structure

Tx is a library for a compact trie data structure. Tx requires 1/4 - 1/10 of the memory usage compared to the previous implementations, and can therefore handle quite a large number of keys (e.g. 1 billion) efficiently. A trie data structure supports exact matching and common prefix matching, which are used for natural language processing etc. Tx uses Level-Order Unary Degree Sequence (LOUDS) for trie representation.

## How to build

  $ ./autogen.sh
  $ ./configure
  $ make

## USAGE
### build index
[wordlist_file]: Word list file name. One word per line. 

Ex\)
```text
apple
orange
banana
```
[index_file]: output index file name. 
```
$ txbuild [wordlist_file] [index_file]
word list 3 elements
outputSize:56 inputSize:17 ratio:3.29412
```
### listup words
```
$ txlist [index_file]
apple
banana
orange
```

### search
```
$ txsearch [index_file]
keyNum:3 nodeNum:18
>apple
query:apple
5
prefixSearch id:0 len:5 lookup:apple
expansionSearch 1
apple
commonPrefixSearch 1
apple (id=0)
predictiveSearch 1
apple (id=0)
>pearch
query:pearch
6
prefixSearch not found
expansionSearch 0
commonPrefixSearch 0
predictiveSearch 0
>
```
