LRU Cache Implementation: 
This project provides a C++ implementation of a Least Recently Used (LRU) Cache. It's designed to store a fixed number of items, automatically evicting the least recently used one when capacity is reached. The goal is to achieve O(1) time complexity for all operations.

How It Works: 
The LRU Cache combines a doubly linked list and an unordered map. The linked list maintains item recency (MRU at head, LRU at tail). The map stores key to linked list iterator mappings for O(1) lookups, allowing fast access to any node.

Core Operations: 
LRUCache(capacity): Initializes the cache with a specified size.
get(key): Returns the value of key. If found, it moves the item to the MRU position. Returns -1 if key isn't present.
put(key, value): Inserts or updates a key-value pair. If capacity is full, the LRU item is evicted before insertion.
Performance & Constraints
All get and put operations are performed in O(1) time complexity on average. The cache capacity ranges from 1 to 3000, with keys and values up to 10 

Example Usage: 
The main function demonstrates the cache's behavior. It shows item insertion, retrieval, and how eviction occurs when new items are added to a full cache. This mirrors the problem's example scenario.







 MyHashMap: 
This project implements a simplified HashMap (unordered map) from scratch in C++. It avoids using built-in hash table libraries, focusing on fundamental data structure concepts. It provides core map operations with average-case O(1) performance.

Features: 
put(key, value): Inserts or updates a key-value pair.
get(key): Retrieves the value for a key, or -1 if not found.
remove(key): Deletes a key-value pair from the map. All operations are designed for average-case O(1) time complexity.

How It Works: 
This custom HashMap uses separate chaining to handle collisions. It employs a std::vector of std::lists, where each list holds (key, value) pairs. A simple modulo hash function distributes keys across a prime number of buckets, ensuring efficient lookups.


Example Usage
The included main function demonstrates how to use the MyHashMap. It covers inserting, retrieving, updating, and removing entries. You can easily compile and run it to see the HashMap in action.
