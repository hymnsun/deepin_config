## 2 LINUX 指令

### cat,cd,ls,pwd
```
pwd                             # Print Working Directory
cd -                            # Back to latest dir 
ls -lh                          # easy mode，kB,GB
ls -a 显示所有文件
ls -la 且显示权限等详细信息


### cat        
cat file1
cat file1 > file2               # write to file2
cat file1 file2 > file3         # both write to file2
cat file1 >> file3              # write in tail
```
### touch
```
touch file 
touch file1 file2 file3 
mkdir folder                    # create folder
```

### cp
```
cp file1 file2                  # substitue file2 if 
cp file1 -i file2               # warning mode
cp -R folder1/ folder2/         # ATTENTION TO `-R`
cp file* folder/
```
### mv
```
mv file1 folder/
mv file1 file2                  # rename
```

### mkdir
```
mkdir [-mp] folder
mkdir -p folder/subfolder
```

### rmdir
```
rmdir folder   ## folder is empty
```

### rm
```
rm file1
rm -r folder
```

### vim nano dedit code 
- vim
    - <kbd>i</kbd> : 输入文本
    - <kbd>Esc</kbd>
    - <kbd>shift</kbd> + <kbd>:</kbd>
    - wq 保存退出

### chmod chown chgrp
```
# ls -l
# type + user/group/others  
    # type
    # d:folder;   -:file
    # rwx :000 111

chmod [-R] [who:u/g/o/a][+/-/=][r/w/x] [filename]
chmod u+x test.py
chmod 771 test.py           chmod ug=rwx,o=x test.py
chmod 777 file              chmod a=rwx file

chgrp [-R] groupname file
chown [-R] username file
chown [-R] username:groupname file
```

### ssh movan python
- generate private and public key,public key put on controled PC.
- ssh root@139.a.b.c



### user management

---
### others
- install software
    ```
    sudo apt[-get] install [software]
    sudo apt-get remove [software]
    sudo apt-get upgrade 更新已安装包
    sudo dpkg -i [file_name.deb]
    ```      
- wget

        