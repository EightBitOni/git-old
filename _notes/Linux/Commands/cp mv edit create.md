## Working with files


### copy file/folder  


```
cp (filename/folder) (directory)
```

>[!Note]-
>(remember, if the filename/folder name has spaces then you will need to encase the filename with speech marks such as cp "(filename with spaces)" (directory). This applis to other commands such as mv. )  

```
cp ssh.conf /home/newfolder 
```


### move file/folder  

mv (filename) (directory)  

example
```
mv ssh.conf /home/newfolder  
```


### move multiple files/folders simultaneously  

mv (file1) (file2) (file3) -t (directory to move to)

example
```
mv logs.txt keys.conf script.py -t /home/savedWork
```


### Move all files from current directory into another directory  

mv * (directory to move files to)  

mv * /home/scripts  

### rename files/folder  

mv (current filename) (new filename)  

mv ssh.conf NewSSH.conf  

### create a file  

touch (filename)  

touch newFile.txt  

### create a folder  

mkdir (foldername)  

mkdir newFolder  

### open file for editing  

nano (filename)  

nano keys.conf  

### output contents of file  

cat (filename)  

cat keys.conf  

### upload file to a remote machine  

scp (filename) (username)@(IP of remote machine ):/(directory to upload to)

scp example.txt john@192.168.100.123:/home/john/

### run an bash script program  

./(name of script)  

./timer  

### open a file for reading/editing  

nano (filename)  

nano readME.txt

### More Notes
files/folders with special characters such as - (dash), if you try to copy or move these files you will encounter errors because Linux interprets the - as a type of argument, therefore you will have to place -- just before the filename. 
example: 
cp -- -filename.txt /home/folderExample.