## lrucache (least-recently-used cache)
>It is a cache replacement policy that evicts the element which was not used for the longest period of time. For more information visit https://en.wikipedia.org/wiki/Cache_replacement_policies.

##### lrucache:
  
  *description:* **`lrucache(limit = 1024)`** *it creates a empty lru cache with a specified limit*
  
  *space-complexity:* **`O(n)`** *where **n** is the no of elements in the cache*
  
  ```python
  import lrucache
  ob = lrucache.lrucache(limit = 2056)
  # Now u cud insert 2056 things into the cache 
  ```
  
##### put:

  *description:* **`put(k, v = None)`** *it inserts **k, v** into the cache, existing element will be over-written*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  ob.put(1001, 'apple')
  ob.put('red', 'blood')
  ```
  
##### get:

  *description:* **`get(k)`** *it returns **k, v** from the cache, if no such then returns None*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  print(ob.get(1001))
  # will print
  # (1001, 'apple')
  ```

##### pop:

  *description:* **`pop(k)`** *it pops out **k, v** from the cache, if no such then returns None*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  print(ob.pop(1001))
  # will print and delete
  # (1001, 'apple')
  ```

##### getAll:

  *description:* **`getAll()`** *it returns a generator that yields every element present in the cache*
  
  *time-complexity:* **`O(n)`** *where **n** is the no of elements in the cache*
  
  ```python
  for i in ob.getAll():  
    print(i)
  # will print
  # (1001, 'apple')
  # ('red', 'blood')
  ```
 
##### printAll:

  *description:* **`printAll()`** *prints every item generated by **getAll()** on the console*
  
  *time-complexity:* **`O(n)`** *where **n** is the no of elements in the cache*
  
  ```python
  ob.printAll()
  # will print
  # (1001, 'apple')
  # ('red', 'blood')
  ```
 
##### popAll:

  *description:* **`popAll()`** *it returns a generator that pops out every element present in the cache (empties the cache)*
  
  *time-complexity:* **`O(n)`** *where **n** is the no of elements in the cache*
  
  ```python
  for i in ob.popAll():
    print(i)
  # will print and delete
  # (1001, 'apple')
  ```

##### getKeyCount:

  *description:* **`getKeyCount()`** *it returns the no of elements in the cache*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  print(ob.getKeyCount())
  # will print
  # 2
  ```

##### limit:

  *description:* **`limit`** *it returns the max no of elements that could be in the cache*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  print(ob.limit)
  # will print
  # 2056
  ```

##### faults:

  *description:* **`faults()`** *it returns the no of faults occurred until last put*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  print(ob.faults())
  # will print
  # 2
  ```
  
##### increaseLimit:

  *description:* **`increaseLimit(by)`** *it will increase the cache size by the specified **by** value, **by** value could only be positive*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  ob.increaseLimit(2)
  # will increase the limit by 2
  ```
  
##### doublesLimit:

  *description:* **`doublesLimit()`** *it will double the size of the cache*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  ob.doublesLimit()
  # will increase the limit by 2x
  ```
  
##### triplesLimit:

  *description:* **`triplesLimit()`** *it will triple the size of the cache*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  ob.triplesLimit()
  # will increase the limit by 3x
  ```

##### isEmpty:

  *description:* **`isEmpty()`** *it checks whether the cache is empty or not*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  print(ob.isEmpty())
  # will print
  # False
  ```
  
##### isFull:

  *description:* **`isFull()`** *it checks whether the cache is full or not*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  print(ob.isFull())
  # will print
  # False
  ```
  
##### isHalfFull:

  *description:* **`isHalfFull()`** *it checks whether the cache is half-full or not*
  
  *time-complexity:* **`O(1)`**
  
  ```python
  print(ob.isHalfFull())
  # will print
  # False
  ```
