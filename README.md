shadowsocks
===========
这是一个轻量级shadowsocks代理
运用了sock5协议
tcp转发相关知识
usage
----------
首先，确保你安装了python3

	$ python --version
	Python 3.6.4

然后编辑‘config.json’,改变对应参数
	server    你的服务器ip或者域名
	port      服务器端口
	password  密码(暂时没用)

advanced
---------
* 确保config.json与sock5server.py文件放在同一个子目录
然后打开终端 python sock5server.py
* 如果需要后台运行 linux系统下 nohup python3 sock5server.py > log
* 服务器端部署完毕后 请在客户端自行连接对应部署Ip和端口，(注意勾选sock5协议)
* log为python运行日志文件
logger.log为sock5server.py程序日志

这个程序目前的状况
-----------------
* 实现了多线程自动转发
  但是流量是明文
* 直接部署在服务器很危险
* 希望小伙伴也可以贡献加密方法
