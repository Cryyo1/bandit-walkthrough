## Solution 

### 1- login with ssh

### 2-  we get the human readable part using strings and pass the result to grep ===

```
bandit9@bandit:~$ strings data.txt  | grep ===
========== the*2i"4
========== password
Z)========== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

```