# 2023 Fall FE Backend Interview

## Architecture Task
You are tasked with developing a server-side application that accepts image uploads every 1.5 seconds. Your application is responsible for compressing and saving the images on disk, and storing each image's name in a database. Without writing any code, briefly describe a possible software schema you could use to solve this task. You should be sure to mention and describe the advantages and disadvantages of:
- The web framework you will use to process and save the image
- What application protocol you will use to receive the image
- The database engine you will use to store files


## Programming Task
Given a set of program nodes that depend on each other, write a Python3 method `getSafeRunOrder` that returns a valid order to run the programs in such that no program will run before all of its dependencies are running.

### Example
```py
nodes = {'a','b','c','d'} 
dependencies = {'a->b','a->d','b->c','d->c'}
```
**Explanation:** In this example, there are 4 programs labelled `a` through `d`. The notation `a->b` means that the program `a` is dependent on the program `b`. You can assume every program's name consists of lower-case `a-z` and has a length of at least 1 (i.e it matches the regular expression `[a-z]+`).

**Valid output:** Valid safe run orders for this input include:
- [`c`, `b`, `d`, `a`]
- [`c`, `d`, `b`, `a`]

Your function can return any of them.

### Starter Code
```py
from typing import Set, List

def getSafeRunOrder(nodes: Set[str], dependencies: Set[str]) -> List[str]:
    return "TODO: Implement the method"

def test():
    nodes = {'a', 'b', 'c', 'd'} 
    dependencies = {'a->b','a->d','b->c','d->c'}
    order = getSafeRunOrder(nodes, dependencies)
    print(order)
    assert order in [['c','b','d','a'],['c','d','b','a']]

if __name__ == "__main__":
    test()
```
