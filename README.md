# hash-tables
hash tables

### Overview

- Hash tables are one of the most important data structures
- They can get/store/delete values in 0(1) time
- A hash function takes in a string and returns and index/number
- Deterministic: same input should always result in the same output
- A hash table uses a list to store values
- Uses the modulo operator to get an index with the array bounds
- Recommended: use the DJB2, FNV-1 hashing algorithm


### Naive example

https://repl.it/@webdevdave/hash-tables#main.py

```
def my_hash(s):
    sb = s.encode()     # converts each letter to a number
    total = 0           # stores total of all numbers
    for c in sb:
        total += c
    return total        
        
        
my_array = [None] * 8                     # create an empty array to hold indexes

# store a vlue
hash_index = my_hash("hello world") % 8   
my_array[hash_index] = 'my value'         

print(my_array)

# to get a value
hash_index = my_hash("hello world") % 8
print(my_array[hash_index])


# remove a value
hash_index = my_hash("hello world") % 8
my_array[hash_index] = None
```

