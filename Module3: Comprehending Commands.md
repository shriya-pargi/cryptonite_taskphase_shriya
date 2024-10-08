# Linux Luminarium

## Module3: Comprehending Commands

### 1.  cat: not the pet, but the command!
In this challenge we are introduced to `cat` command that stands for concatenate and is most often used to read files  

```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{Af9K3BRKBmRp04LaAugG6hOfjT5.dFzN1QDLxQDO0czW}
```

### 2. catting absolute paths 
In this challenge we just use `cat` command using an absolute path

```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{I5ECahsEUGtOQ7CtOan1uwBg9bB.dlTM5QDLxQDO0czW}
```

### 3. more catting practice 
same as the previous challenge 

```
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /lib/ssl/certs/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /lib/ssl/certs/flag
pwn.college{QUHxLd_wWnxPn60vfRxEyp3XdDH.dBjM5QDLxQDO0czW}
```

### 4. grepping for a needle in a haystack
`grep` command is used to search for a specific content  

```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{kffqZuRw6CxZkxZUt1aXq7zmYlT.ddTM4QDLxQDO0czW}
```

### 5. listing files 
