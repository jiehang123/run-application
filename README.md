# run-application

这个项目是一个windows系统下的快捷键，可以用来快速启动文件夹，网址和软件等

使用方式：
1. 将该项目用maven打包成jar包（run-application.jar）
2. 将该jar包放到某个文件夹下，比如：（C:\soft\run_application）
3. 在当前文件夹路径下创建一个run.bat文件，内容如下：
```
@echo off
cd %~dp0
java -jar run.jar run.properties %*
```
4. 在当前文件夹路径下创建一个run.properties文件，内容自己定义，比如：
```
### A=B
### A表示快捷键，B是该快捷键对应的具体内容
maven=C:\\soft\\apache-maven-3.5.2
baidu=https://www.baidu.com/
wechat=C:\\soft\\Tencent\\WeChat\\WeChat.exe
```
5. 将当前路径（C:\soft\run_application）添加到环境变量PATH中
6. 使用方式：在“运行”(Win+R)中输入：run maven就能快速打开指定的C:\\soft\\apache-maven-3.5.2文件夹；
运行run baidu能快速打开baidu网页
