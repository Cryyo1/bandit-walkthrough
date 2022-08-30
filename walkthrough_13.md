## Solution 

### 1- login with ssh

### 2- we convert hexdump file to bianry using xxd

```
bandit12@bandit:/tmp/solu$ xxd -r data.txt data2
bandit12@bandit:/tmp/solu$ file data2
data2: gzip compressed data, was "data2.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
```

### 3- a long serie of unziping files using gunzip , bunzip2 and extracting archives usin tar
```
bandit12@bandit:/tmp/solu$ mv data2 data2.bin.gz
bandit12@bandit:/tmp/solu$ gunzip data2.bin.gz 
bandit12@bandit:/tmp/solu$ file data2.bin 
data2.bin: bzip2 compressed data, block size = 900k
```

```
bandit12@bandit:/tmp/solu$ mv data2.bin data2.bin.bz2
bandit12@bandit:/tmp/solu$ bunzip2 data2.bin.bz2 
bandit12@bandit:/tmp/solu$ file data2.bin 
data2.bin: gzip compressed data, was "data4.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
```
```
bandit12@bandit:/tmp/solu$ mv data2.bin data2.bin.gz
bandit12@bandit:/tmp/solu$ gunzip data2.bin.gz
bandit12@bandit:/tmp/solu$ file data2.bin 
data2.bin: POSIX tar archive (GNU)
```

```
bandit12@bandit:/tmp/solu$ mv data2.bin data2.bin.tar
bandit12@bandit:/tmp/solu$ tar -xvf data2.bin.tar 
data5.bin
bandit12@bandit:/tmp/solu$ file data5.bin 
data5.bin: POSIX tar archive (GNU)
```

```
bandit12@bandit:/tmp/solu$ mv data5.bin data5.bin.tar
bandit12@bandit:/tmp/solu$ tar -xvf data5.bin.tar 
data6.bin
bandit12@bandit:/tmp/solu$ file data6.bin 
data6.bin: bzip2 compressed data, block size = 900k
```

```
bandit12@bandit:/tmp/solu$ mv data6.bin data6.bin.bz2
bandit12@bandit:/tmp/solu$ bunzip2 data6.bin.bz2 
bandit12@bandit:/tmp/solu$ file data6.bin 
data6.bin: POSIX tar archive (GNU)
```

```
bandit12@bandit:/tmp/solu$ mv data6.bin data6.bin.tar 
bandit12@bandit:/tmp/solu$ tar -xvf data6.bin.tar 
data8.bin
bandit12@bandit:/tmp/solu$ file data8.bin 
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
```
```
bandit12@bandit:/tmp/solu$ mv data8.bin data8.bin.gz
bandit12@bandit:/tmp/solu$ gunzip data8.bin.gz 
bandit12@bandit:/tmp/solu$ file data8.bin 
data8.bin: ASCII text
bandit12@bandit:/tmp/solu$ cat data8.bin 
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

```

### note that for bzip files, tar file, gzip files you need to add extention to them for unziping and extracting