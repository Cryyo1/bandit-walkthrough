## Solution 

### 1- login with ssh

``` 
ssh  bandit3@bandit.labs.overthewire.org -p 2220

```

### 2- finiding the password

```
bandit3@bandit:~$ ls inhere/ -lha
total 12K
drwxr-xr-x 2 root    root    4.0K May  7  2020 .
drwxr-xr-x 3 root    root    4.0K May  7  2020 ..
-rw-r----- 1 bandit4 bandit3   33 May  7  2020 .hidden
```
### 3- dispaly the . hidden file

```

andit3@bandit:~$ cat ./inhere/.hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB

```