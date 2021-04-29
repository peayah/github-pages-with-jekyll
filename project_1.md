Lazy Deletion in Binary Search Trees

```
Populate:
Tree size:  6 
Hard size:  6
 50
 L --- 20
        L --- 10
        R --- 30
 R --- 70
        L --- 60

Soft delete 20
Tree size:  5 
Hard size:  6
 50
 L --- 20  deleted
        L --- 10
        R --- 30
 R --- 70
        L --- 60

Collect Garbage (Hard delete)
Tree size:  5 
Hard size:  5
 50
 L --- 30
        L --- 10
 R --- 70
        L --- 60

Add 22
Tree size:  6 
Hard size:  6
 50
 L --- 30
        L --- 10
               R --- 22
 R --- 70
        L --- 60

Lazy-remove 22.
Tree size:  5 
Hard size:  6
 50
 L --- 30
        L --- 10
               R --- 22  deleted
 R --- 70
        L --- 60

Re-insert 22
Hard size should not change.
Tree 1 size:  6 
Hard size:  6
 50
 L --- 30
        L --- 10
               R --- 22
 R --- 70
        L --- 60
```
