# OSX 沙箱

为了防止本地开发环境受到攻击，大部分服务类的应用都应该放到沙箱里运行

# 支持程序列表

请自行修改 LaunchAgents

```
redis
sandbox-exec -f /usr/local/homebrew/etc/sandbox/redis-sandbox.conf /usr/local/homebrew/opt/redis/bin/redis-server /usr/local/homebrew/etc/redis.conf

elasticsearch - 先修改你的 es 路径
sandbox-exec -f elasticsearch.conf /secure/elasticsearch-1.7.3/bin/elasticsearch

百度Mac准入
sandbox-exec -f zhunru.conf /Applications/zhunru.app/Contents/MacOS/BaiduInternalPlatform.bin
```

