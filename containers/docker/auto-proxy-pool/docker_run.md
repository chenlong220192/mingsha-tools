- docker run
```
docker run -dit \
  --name auto_proxy_pool  \
  --restart always  \
  -p 9999:8080  \
  -v /data/containers/auto_proxy_pool:/run/data \
  --privileged=true \
  mzzsfy/auto-proxy-pool:latest
```

proxy.yml
```
defaultCheckUrl: http://baidu.com/ #检测代理是否有效，不用改
changeRequest:
  - hostRegex: .+\.taobao\.com #正则表达式
    proxy: proxy
upstream:
  proxy: #自定义名字
    template: '{{$x := regexFindAll "\\d{1,3}(\\.\\d{1,3}){3}:\\d{2,5}" . -1}}{{range $s := $x}}{{printf "http://%s" $s}}{{end}}'
    apiUrl: http://api.xiequ.cn/VAD/GetIp.aspx?act=get&uid=132548&vkey=803E2B382A62129C7CF1F69E2D34290D&num=200&time=30&plat=1&re=0&type=0&so=1&ow=1&spl=1&addr=&db=1
    checkRetryNumber: 5 #检测代理次数，超过次数则获取新代理
    apiRetryNumber: 10 #上游重试次数，超过次数则采用直连
    lifecycle: -1 #自动失效时间，-1为不自动失效，单位秒
    maxSize: 1 #保留几个上游
    requestInterval: 100ms #请求时间间隔，在这个时间内只会请求一次api
```
