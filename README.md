

HTTPServer
===============

本项目是在 https://github.com/Flamel-NW/TinyWebServer-Cpp#:~:text=%E5%80%9F%E9%89%B4%E4%BA%86TinyWebServer,%E6%94%B9%E8%89%AF%E5%92%8C%E5%88%9B%E6%96%B0基础上进行对网络编程的学习研究

* 使用 **线程池 + 非阻塞socket + epoll(ET和LT均实现) + 事件处理(Reactor和模拟Proactor均实现)** 的并发模型
* 使用**状态机**解析HTTP请求报文，支持解析**GET和POST**请求
* 访问服务器数据库实现web端用户**注册、登录**功能，可以请求服务器**图片和视频文件**
* 实现**同步/异步日志系统**，记录服务器运行状态
* 经Webbench压力测试可以实现**上万的并发连接**数据交换


快速运行
------------
* 服务器测试环境
	* Ubuntu版本16.04
	* MySQL版本5.7.29
* 浏览器测试环境
	* Windows、Linux均可
	* Chrome
	* FireFox
	* 其他浏览器暂无测试
