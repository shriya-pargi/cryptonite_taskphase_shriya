### Linux Luminarium

## Module2: Pondering Paths

### 1. The Root 
In this challenge we need to invoke a program by providing its path on the command line.  
The absolute path starts with `/` and is followed by a program  
In this case the absolute path that starts at the root directory is `/pwn`  
Here, `pwn` is the program.

```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{AIFIzQ0mC6SiZFlgidpxPuSk5lL.dhzN5QDLxQDO0czW}
```

### 2. Program and Absolute paths
In this challenge we need to invoke the `run` program that is the `challenge` directory, in turn in the root directory(`/`)  
The absolute path in this case would be `/challenge/run`  

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{QiCfm8sQFHmXxtdmYYmUf29oOCM.dVDN1QDLxQDO0czW}
```

### 3. Position thy self
In this challenge we get introduced to the `cd` - change directory command.
There are many sub directories in the Linux system.
For its argument we have to go through multiple directories providing its path.
Here we are asked to run a program in a different directory which is yet unknown to us.

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the `cd` utility to change directory appropriately.
```
After switching directories, and running the challenge

```
hacker@paths~position-thy-self:~$ cd /usr/aarch64-linux-gnu/include/gnu
hacker@paths~position-thy-self:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{kHWGdEJCXmJiw8mgIQGB-G2dE5H.dZDN1QDLxQDO0czW}
```

### 4. Position elsewhere
Similar to the previous challenge 

```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var/log directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/usr/bin$ cd /var/log
hacker@paths~position-elsewhere:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{oirxO85mR-SU0nfq1vI-5WgK5K6.ddDN1QDLxQDO0czW}
```

### 5. Position yet elsewhere
Similar to the previous challenge

```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /proc/67 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /proc/67
hacker@paths~position-yet-elsewhere:/proc/67$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{MNPMXidvMcmTemljumtBaWkF3xR.dhDN1QDLxQDO0czW}
hacker@paths~position-yet-elsewhere:/proc/67$
```

### 6. implicit relative paths, from /
In this challenge we follow a relative path that is relative to our current working directory `cwd`  
Now with reference to `/`  we `run` the program  
The main difference between a reltive path and absolute path is that relative paths never start with `/`  

```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{o_9Tro9l9m9aBQnxFGoivLv9VPR.dlDN1QDLxQDO0czW}
```

### 7. explicit relative paths, from /
In this challenge we start by following a relative path using `/`  

```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ challenge/run
Incorrect...
This challenge must be called with a relative path that explicitly starts with a `.`!
```
Here we are asked to follow a relative path that starts with `.`

```
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gikyDMDGJjAz6txwNV4gx--cbY7.dBTN1QDLxQDO0czW}
```

### 8. implicit relative path
In this challenge we learn the significance and use of `.`    
For safety reasons, we don't use the `run` command beacuse it gives us a `command not found` error  
So, instead we use `.`

```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{M_tVwFq8lbrzmaDLvDSy_u7IzUk.dFTN1QDLxQDO0czW}
```

### 9. home sweet home
The prompt `~` is a shorthand for `/home/hacker`   
The expansion of `~` is an absolute path  
For example: ~/~ will be expanded to /home/hacker/~ rather than `/home/hacker/home/hacker`
The file path should point to the home directory  
This should not be more than 3 characters  
Taking the file name as `a` , so the absolute path would be `/a`  

```
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{0c7hAdMpCnoBBgGg3TJq4Py6zb_.dNzM4QDLxQDO0czW}
```

