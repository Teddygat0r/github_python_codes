# Something about the Trie
# 
# A trie (digital tree or prefix tree, came from from retrieval) is an ordered tree data structure 
# that is used to store a dynamic set or associative array where the keys are usually strings.
# Unlike a binary search tree, no node in the tree stores the key associated with that node; 
# instead, its position in the tree defines the key with which it is associated.
# A trie has several advantages over binary search trees. it could be used to replace a hash table.
#
# Advantages:
# 1. Looking up data in a trie is faster in the worst case, O(m) time (where m is the length of a search string), compared to an imperfect hash table. An imperfect hash table can have key collisions. A key collision is the hash function mapping of different keys to the same position in a hash table. The worst-case lookup speed in an imperfect hash table is O(N) time, but far more typically is O(1), with O(m) time spent evaluating the hash.
# 2. There are no collisions of different keys in a trie.
# 3. Buckets in a trie which are analogous to hash table buckets that store key collisions are necessary only if a single key is associated with more than one value.
# 4. There is no need to provide a hash function or to change hash functions as more keys are added to a trie.
# 5. A trie can provide an alphabetical ordering of the entries by key.
# 
# Drawbacks:
# 1. Tries can be slower in some cases than hash tables for looking up data, especially if the data is directly accessed on a hard disk drive or some other secondary storage device where the random-access time is high compared to main memory.[5]
# 2. Some keys, such as floating point numbers, can lead to long chains and prefixes that are not particularly meaningful. Nevertheless a bitwise trie can handle standard IEEE single and double format floating point numbers.
# 3. Some tries can require more space than a hash table, as memory may be allocated for each character in the search string, rather than a single chunk of memory for the whole entry, as in most hash tables.
#  
# implementing the algorithm with python:
# def find(node, key):
#     for char in key:
#         if char not in node.children:
#             return None
#         else:
#             node = node.children[char]
#     return node.value