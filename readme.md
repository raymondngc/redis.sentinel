Due to the fact that when we bind to 127.0.0.1, Sentinel will report the incorrect ip to external client. We need to bind to the actual IP. Please update the following when you do your test in your local machine .
```
1. bind address in all redis.conf.master and/or redis.conf.slave
2. slaveof IP in the redis.conf.master and/or redis.conf.slave of the slave
3. bind address and monitor ip of mymaster in sentinel.conf.org
```