FROM xiaoruiguo/redis
MAINTAINER xiaoruiguo sean.xiao@pcit.com
ENV REFRESHED_AT 2014-06-01
ENTRYPOINT [ "redis-server", "--logfile /var/log/redis/redis-replica.log", "--slaveof redis_primary 6379" ]
