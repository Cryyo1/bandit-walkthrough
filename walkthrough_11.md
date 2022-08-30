## Solution 

### 1- login with ssh

### 2-  we cat the file and pass the result to base64  to decode  it
```
bandit10@bandit:~$ cat data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```