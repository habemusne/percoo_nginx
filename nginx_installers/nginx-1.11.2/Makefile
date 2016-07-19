
default:	build

clean:
	rm -rf Makefile objs

build:
	$(MAKE) -f objs/Makefile

install:
	$(MAKE) -f objs/Makefile install

modules:
	$(MAKE) -f objs/Makefile modules

upgrade:
	/percoo_home/Library/nginx/sbin/nginx -t

	kill -USR2 `cat /percoo_home/Library/nginx/logs/nginx.pid`
	sleep 1
	test -f /percoo_home/Library/nginx/logs/nginx.pid.oldbin

	kill -QUIT `cat /percoo_home/Library/nginx/logs/nginx.pid.oldbin`
