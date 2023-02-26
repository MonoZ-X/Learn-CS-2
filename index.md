# Feliks Zemdegs 
![image](https://user-images.githubusercontent.com/91028131/221386172-49e76651-3d33-4f3b-92ce-4e096d85f5c3.png)

```
// Code to scramble a 3 x 3 rubik's cube, referenced from a github user a while ago (don't remember)

import random
import system
from scrambleImage import scramble

moves = ["U", "D", "F", "B", "R", "L"]
direction = ["", "'", "2"]
rand = random.randint(25, 28)

def scramble():
    s = valid([[random.choice(moves), random.choice(direction)] for x in range(rand)])
    cube = scramble(s, rand)
    return ''.join(str(s[x][0]) + str(s[x][1]) + ' ' for x in range(len(s))) + "[" + str(slen) + "]"

def check(ar):
    for x in range(1, len(ar)):
        while ar[x][0] == ar[x-1][0]:
            ar[x][0] = random.choice(moves)
    for x in range(2, len(ar)):
        while ar[x][0] == ar[x-2][0] or ar[x][0] == ar[x-1][0]:
            ar[x][0] = random.choice(moves)
    return ar
 
s = scramble()
print(s)
```

CheckList:
- [x] Add headers
- [x] Add an image
- [x] Add a code example
- [x] Make a task list
- [ ] Merge pull request
