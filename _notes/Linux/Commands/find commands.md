## Find Command

### Find files based on filename  

find (directory path) -type f -name (filename)

note: if only know file extention you can use "*.txt"

example:
find /home/Andy -type f -name sales.txt  

### Find Directory based on directory name  

find (directory path) -type d -name (filename)

example:
find /home/Andy -type d -name pictures

### Find files based on size  

find [directory path] -type f -size [size]

find /home/Andy -type f -size 10c

(c for bytes,

k for kilobytes

M megabytes

G for gigabytes

type:'man find' for full information on the  options)  

### Find files based on username  

find [directory path] -type f -user [username]

find /etc/server -type f -user john

### Find files based on group name

find [directory path] -type f -group [group name]

find /etc/server -type f -group teamstar

### Find files modified after a specific date  

find [directory path] -type f -newermt '[date and time]'  

find / -type f -newermt '6/30/2020 0:00:00'

(all dates/times after 6/30/2020 0:00:00 will be considered a condition to look for)  

### Find files based on date modified

find [directory path] -type f -newermt [start date range] ! -newermt [end date range]

find / -type f -newermt 2013-09-12 ! -newermt 2013-09-14

(all dates before 2013-09-12 will be excluded; all dates after 2013-09-14 will be excluded, therefore this only leaves 2013-09-13 as the date to look for.)  

### Find files based on date accessed

find [directory path] -type f -newerat [start date range] ! -newerat [end date range]

find / -type f -newerat 2017-09-12 ! -newerat 2017-09-14

(all dates before 2017-09-12 will be excluded; all dates after 2017-09-14 will be excluded, therefore this only leaves 2017-09-13 as the date to look for.)

### Find files with a specific keyword  

grep -iRl [directory path/keyword]  

grep -iRl '/folderA/flag'


### THM Examples
topson@james:~$ cat ReadMeIfStuck.txt    
Looking for flag 1?:It seems you will have to think harder if you want to find the flag. Perhaps try looking for a f  
ile called additionalHINT if you can't find it..  
Looking for flag 2?: look for a file named readME_hint.txt


topson@james:~$ find /home/topson -type f -name additionalHINT  
/home/topson/channels/additionalHINT


topson@james:~/channels$ cat additionalHINT    
try to find a directory called telephone numbers... Oh wait.. it  contains a space.. I wonder how we can find that..  
..

telephone\ numbers/

topson@james:~$ find /home/topson -type d -name 'telephone numbers'  
/home/topson/corperateFiles/xch/telephone numbers

topson@james:~$ cat corperateFiles/xch/telephone\ numbers/readME.txt    
202-555-0150  
202-555-0125  
617-555-0115  
+1-617-555-0115    
+1-617-555-0186  
+1-617-555-0138  
use the Find command to find a file with a modified date of 2016-09-12 from the /workflows directory

find /home/topson/workflows/ -type f -newermt 2016-09-11 ! -newermt 2016-09-13    
/home/topson/workflows/xft/eBQRhHvx




### **2>/dev/null** at the end of your find command can help filter your results to exclude files/directories that you do not have permission to