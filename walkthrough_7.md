## Solution 

### 1- login with ssh

### 2- search for the file using **find**

```
bandit6@bandit:~$ find / -size 33c -group bandit6 -user bandit7

/var/lib/dpkg/info/bandit7.password
```

### 4- cat the file

```
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password 
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```
