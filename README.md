# CharHashing
Collection of functions and classes that use a combination of mid-square method hashing, along with unicode code point representation, to hash strings. The main function of interest, charLoadFactorOptimizer, seeks to maximize the loadFactor of the hash table we return by returning once ever string we pass to the function is admitted entry into the hash table.


add method first identifies the slot where we should insert item
If that slot is None, then we insert item there
If slot is int, then we create a new instance of CharHasher, 
and insert it into that slot with parameters numList = [original entry, item]
If slot is a CharHasher, then we recursively call add for that slot
