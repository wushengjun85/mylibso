QT 加载动态链接库（Linux 下.so文件）

root@Linux-host:/home/vmuser/C# ls
main.c  mylib.c  mylib.h
root@Linux-host:/home/vmuser/C# gcc -fpic -shared mylib.c -o libmylib.so
root@Linux-host:/home/vmuser/C# ls
libmylib.so  main.c  mylib.c  mylib.h
root@Linux-host:/home/vmuser/C# gcc main.c -o main -L ./ -lmylib
root@Linux-host:/home/vmuser/C# ls
libmylib.so  main  main.c  mylib.c  mylib.h
root@Linux-host:/home/vmuser/C# ./main 
Hello World
Hello fun so
root@Linux-host:/home/vmuser/C# 
