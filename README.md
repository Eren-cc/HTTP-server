

HTTPServer
===============

本项目是在 [TinyWebServer](https://github.com/qinguoyi/TinyWebServer)基础上进行对网络编程的学习研究

项目内容
------------
* 使用 线程池+数据库连接池（经典池化操作+posix标准手搓实现） + 非阻塞socket + epoll 的并发模型
* 使用状态机解析HTTP请求报文(HTTP1.1)，支持解析GET和POST请求，并进行报文响应
* 访问服务器数据库实现web端用户注册、登录功能，可以请求服务器图片和视频文件
* 实现同步/异步日志系统，记录服务器运行状态
* 定时器用于处理不常用链接（信号+链表实现）

一些改进：
------------
* 将listenfd设置为阻塞，clientfd设置为非阻塞，epoll只保留ET(边缘触发)
* 对代码风格进行了一些改进，增加了更详细的注释便于初学者学习使用
* 对前端页面进行了一些无关紧要的修改

一些缺憾：
------------
* 仅支持get与post两类http请求
* 报文未进行任何加密，服务器部署在局域网内时明文传输
* 为了并发度牺牲了cgi和其对页面的校验
* 未实现文件上传

运行
------------
* 服务器测试环境
	* Ubuntu版本20.04
	* MySQL版本5.7.29
* 浏览器测试环境
	* Windows、Linux均可
	* Chrome
	* FireFox
> * 服务器运行

<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/000.png" height="400"/> </div>

> * 主页面

<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/002.png" height="400"/> </div>

> * 登录

<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/001.png" height="400"/> </div>

> * 图片展示

<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/003.png" height="400"/> </div>

> * 视频播放展示

<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/004.png" height="400"/> </div>

> * 文件上传（未实现）

<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/005.png" height="400"/> </div>

webbench
-----------
* 服务器为个人PC，内存为 8.00 GB (7.74 GB 可用)
> * webbench服务器压测

<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/7.png" height="200"/> </div>

