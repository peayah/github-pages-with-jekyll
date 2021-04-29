Time stands still when code.

I’m a full-stack python developer with industry experience in building websites and working with data in various ways.

I have also taken classes in Database Management and Data Visualization and have April 2021 handed in the final assignment in my last programming class; Advanced Data Structures and Algorithms at Foothill College. As I’m finishing my CS degree, I’d like to start working as a programmer instead of sneaking a few hours after a full day at work.

Constantly Learning — Consistently Problem Solving — Constructively Coding

## Skills
Database Coding: Python, R, SQL
Data Manipulation and Visualization: Tableau, Excel
Web Coding HTML, CSS, JavaScript

## Projects
Here is a sample, more at [my GitHub repository](https://github.com/peayah)

### Project 1
Created a function that solve a subset sum problem for any list of integers and a predetermined total. Am able to use to find the optimal combination of integers from a given list to either get close to or hit a total. Could be used to select the optimal combination of packages of different weights to hit a max weight or find a combination of songs that to fill a predetermined runtime. 
Class Project. Link to code: Upon request



### Project 2
Created a function that travels through a maze built from lists to add edges that when fed into Dijkstra will find shortest path. And also list the coordinates the maze traveller has to pass through to get from start to finish. Class Project. 

Link to code: Upon request

### Project 3
Description: Code that lazy-delete in Binary Search Trees. Traverses tree and is able to differentiate between not deleted, lazy-deleted and hard deleted nodes. 
Class Project. Link to code: Upon request

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
