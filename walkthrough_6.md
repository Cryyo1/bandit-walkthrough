## Solution 

### 1- login with ssh

### 2- navigate to inhere

```
bandit5@bandit:~$ cd inhere
```

### 3- search for the file using **find**


```
bandit5@bandit:~/inhere$ find . -size 1033c ! -executable
./maybehere07/.file2
```

### 4- cat the file
```
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```