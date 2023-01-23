

HTTPServer
===============

本项目是在 [https://github.com/Flamel-NW/TinyWebServer-Cpp](https://github.com/qinguoyi/TinyWebServer)基础上进行对网络编程的学习研究

项目内容
------------
* 使用 线程池 + 非阻塞socket + epoll 的并发模型
* 使用状态机解析HTTP请求报文(HTTP1.1)，支持解析GET和POST请求，并进行报文响应
* 访问服务器数据库实现web端用户注册、登录功能，可以请求服务器图片和视频文件
* 实现同步/异步日志系统，记录服务器运行状态

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
	* Ubuntu版本16.04
	* MySQL版本5.7.29
* 浏览器测试环境
	* Windows、Linux均可
	* Chrome
	* FireFox
	* 其他浏览器暂无测试
> * 服务器运行

<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/000.png" height="400"/> </div>
> * 服务器运行
<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/000.png" height="400"/> </div>
> * 服务器运行
<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/001.png" height="400"/> </div>
> * 服务器运行
<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/002.png" height="400"/> </div>
> * 服务器运行
<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/003.png" height="400"/> </div>
> * 服务器运行
<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/004.png" height="400"/> </div>
> * 服务器运行
<div align=center><img src="https://raw.githubusercontent.com/Eren-cc/httpserver/main/image/005.png" height="400"/> </div>
wenbench
-----------
*


