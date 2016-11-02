# OSX 沙箱

为了防止本地开发环境受到攻击，大部分服务类的应用都应该放到沙箱里运行

另外，为了防止准入、Hi 程序监控员工，也必须放到沙箱里

# 支持程序列表

请自行修改 LaunchAgents

```
redis
sandbox-exec -f redis-sandbox.conf /usr/local/homebrew/opt/redis/bin/redis-server /usr/local/homebrew/etc/redis.conf

elasticsearch - 先修改你的 es 路径
sandbox-exec -f elasticsearch.conf /secure/elasticsearch-1.7.3/bin/elasticsearch

百度Mac准入
sandbox-exec -f zhunru.conf /Applications/zhunru.app/Contents/MacOS/BaiduInternalPlatform.bin

百度Hi
sandbox-exec -f baidu_hi.conf /Applications/百度Hi.app/Contents/MacOS/BaiduHi
```

