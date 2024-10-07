### Linux Luminarium

## Module2: Pondering Paths

### The Root 
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

### Program and Absolute paths
In this challenge we need to invoke the `run` program that is the `challenge` directory, in turn in the root directory(`/`)  
The absolute path in this case would be `/challenge/run`  

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{QiCfm8sQFHmXxtdmYYmUf29oOCM.dVDN1QDLxQDO0czW}
```

### Position thy self
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

```