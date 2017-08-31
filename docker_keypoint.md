## docker-machine 


主机A: 192.168.11.131 安装 docker-machine

主机B: 192.168.11.129

1. A 主机中的 docker-machine 可以在主机 B 中远程安装 docker engine，命令如下:
	
		docker-machine create --driver generic \
							  --generic-ip-address=192.168.11.129 \
							  --generic-ssh-key ~/.ssh/id_rsa \
							  ubuntu-16.04

2. 从 A 主机上必须能够以 root 用户免密码登录 B 主机