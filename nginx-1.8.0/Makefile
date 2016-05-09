
default:	build

clean:
	rm -rf Makefile objs

build:
	$(MAKE) -f objs/Makefile
	$(MAKE) -f objs/Makefile manpage

install:
	$(MAKE) -f objs/Makefile install

upgrade:
	/downloads/install/nginx_tmp/sbin/nginx -t

	kill -USR2 `cat /downloads/install/nginx_tmp/logs/nginx.pid`
	sleep 1
	test -f /downloads/install/nginx_tmp/logs/nginx.pid.oldbin

	kill -QUIT `cat /downloads/install/nginx_tmp/logs/nginx.pid.oldbin`
