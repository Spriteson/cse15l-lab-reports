# Lab Report 3 – Servers and Bugs

**find**

*1)*

```
find technical -type d
```
```
technical/
technical//government
technical//government/About_LSC
technical//government/Env_Prot_Agen
technical//government/Alcohol_Problems
technical//government/Gen_Account_Office
technical//government/Post_Rate_Comm
technical//government/Media
technical//plos
technical//biomed
technical//911report
```
It find all the type that is dirctory. It's useful because I can esaily find all the directories.


*2)*
```
find technical/911report -type f
```
```
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/preface.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```
It find all the type that is plain file. It's useful because I can esaily find all the plain files.


*3)*
```
find technical/911report/chapter-10.txt -type f
```
```
technical/911report/chapter-10.txt
```
It will let me know if the file is a plain file. It's useful because I can check if the file is plain file with looking at it.


*4)*
```
find technical/ -path "technical/" 
```
```
technical/
```
It will print an entry for a directory. It's useful because I can check if a directory exsits and get the path for it.


*5)*
```
find technical/ -path "technical//biomed"
```
```
technical//biomed
```
It will print an entry for a directory. It's useful because I can check if a directory exsits and get the path for it.


*6)*
```
find technical/ -path "technical//911report/chapter-11.txt"
```
```
technical//911report/chapter-11.txt
```
It will print an entry for a file. It's useful because I can check if a file exsits and get the path for it.


*7)*
```
find technical//911report -print
```
```
technical//911report
technical//911report/chapter-13.4.txt
technical//911report/chapter-13.5.txt
technical//911report/chapter-13.1.txt
technical//911report/chapter-13.2.txt
technical//911report/chapter-13.3.txt
technical//911report/chapter-3.txt
technical//911report/chapter-2.txt
technical//911report/chapter-1.txt
technical//911report/chapter-5.txt
technical//911report/chapter-6.txt
technical//911report/chapter-7.txt
technical//911report/chapter-9.txt
technical//911report/chapter-8.txt
technical//911report/preface.txt
technical//911report/chapter-12.txt
technical//911report/chapter-10.txt
technical//911report/chapter-11.txt
```
It prints the full file names and directories for technical//911report on the standard output. It's useful because I can print all the files and directories in a given diretory.


*8)*
```
find technical//911report/chapter-11.txt -print
```
```
technical//911report/chapter-11.txt
```
It prints the full file name and directory for technical//911report/chapter-11.txt on the standard output. It's useful because I can print the file in a given diretory if the file exsit.



*9)*
```
find technical//911report/preface.txt -print
```
```
technical//911report/preface.txt
```
It prints the full file name and directory on the standard output. It's useful because I can print the file and directories in a given diretory if the file exsit.


