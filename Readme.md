# ser_client
项目需求分析：
一、	项目名称：

远程cp   即：rget(remote get)

二、	需求如下：

    syntax: 
1、rget host:/path/to/file
2、rget -r host:/path/to/file 
3、rget -f host:/path/to/file

主要功能：
	1、-r 递归拷贝整个目录
	2、-f 本地有相同文件或者目录的情况下，强制覆盖不提示
需要注意的事情:
	如果要拷贝的目录或者文件在本地存在要提示用户是否覆盖加上-f选项可以强制覆盖
扩展功能（要求必须实现）：
	1、-a 要拷贝文件或者目录的权限和拷贝到本地后的权限要一致。
	2、-v 显示出拷贝文件的进度(进度的格式自己定义，可以简单点)
	3、-t number 多线程拷贝，同时开启number个线程进行拷贝

三、操作环境：

Linux操作系统，vim 编辑器，gcc 编译器，GDB调试工具,编写makefile文件

四、对主要功能的详细描述：

本项目通过对socket的学习，实现了一个远程 cp 功能。本程序分为两部分客户端程序和服务器端程序。 首先我们定义一些约定，即通信协议。


 struct link { int flag; //是否递归拷贝文件夹 1 为递归，0 不递归 
int length; //文件名的长度 
};
Struct info{ Int length; //包长- 2 
charfilename[256];//DIR_TYPE 的时候，放的是目录名，FILE_TYPE
的时候是文件名 
Int filetype; ///标明其类型 DIR_TYPE 或者是 FILE_TYPE 
char errorinfo[256]; //错误信息
五、项目时间安排：
       
        主要功能：6.1~6.7日

        扩展功能：按期末考试之前提交。（最晚7.1日)


