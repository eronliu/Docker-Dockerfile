Docker install and start test mysql5.5server
============
To myslq start hanging in data volumes：
-------------
> docker run --name=dbdata -v /var/lib/mysql centos true

Start mysql open ports designated agents hanging in volume：
---------
> docker rum --volumes-from=dbdata --name=mysql5.5 -d -P username/mysql5.5

Connect Test:
-------
> mysql -h x.x.x.x -uroot -pcomall2014

========
