配置新网站
=========

## 需要安装的包：

* nginx
* python3
* git
* pip
* virtualenv

以 Ubuntu 为例，可以执行下面的命令安装：

sudo apt-get install nginx git python3 python3-pip
sudo pip3 install virtualenv

## 配置 Nginx 虚拟主机

* 参考 nginx.template.conf
* 把 SITENAME 替换成所需的域名，例如 staging.my-domain.com

## systemd 任务

* 参考 gunicorn-systemd.template.service
* 把 SITENAME 替换成所需的域名，例如 staging.my-domain.com

## 文件夹结构：

假设有用户账户，家目录为 /home/username

/home/username
    └ ─ ─ sites
	    └ ─ ─ SITENAME
		    ├ ─ ─ database
			├ ─ ─ source
			├ ─ ─ static
			└ ─ ─ virtualenv
