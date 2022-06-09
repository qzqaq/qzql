一.拉取青龙面板镜像
docker pull whyour/qinglong:latest

二.创建docker容器
docker run -dit \
-v $pwd/ql/config:/ql/config \
-v $pwd/ql/log:/ql/log \
-v $pwd/ql/db:/ql/db \
-v $pwd/ql/scripts:/ql/scripts \
-v $pwd/ql/jbot:/ql/jbot \
-p 5700:5700 \
-e ENABLE_HANGUP=true \
-e ENABLE_WEB_PANEL=true \
--name qinglong \
--hostname qinglong \
--restart always \
whyour/qinglong:latest

一.拉取青龙面板镜像
docker pull whyour/qinglong:2.12.2

二.创建docker容器
docker run -dit \
-v $pwd/ql/config:/ql/config \
-v $pwd/ql/log:/ql/log \
-v $pwd/ql/db:/ql/db \
-v $pwd/ql/scripts:/ql/scripts \
-v $pwd/ql/jbot:/ql/jbot \
-p 5700:5700 \
-e ENABLE_HANGUP=true \
-e ENABLE_WEB_PANEL=true \
--name qinglong \
--hostname qinglong \
--restart always \
whyour/qinglong:2.12.2

三.JD_COOKIE
pt_key=?;pt_pin=?;

四.拉取仓库
ql repo 把这句话替换为你找的库地址

五、安装依赖
curl -fsSL https://ghproxy.com/https://raw.githubusercontent.com/shufflewzc/QLDependency/main/Shell/QLOneKeyDependency.sh | sh

太喜欢这个依赖安装了，方便又好看，而且可以一次性多个安装，直接抄我的作业一把安装。
可能报错，应该是占用过多导致的（我猜的，我啥也不懂，我是个费姐姐）。
重新安装就行，亲测nodejs一把安装无压力，python3要一个个点一下重来。
1、Nodejs

    png-js
    @types/node
    require
    typescript
    crypto-js
    prettytable
    dotenv
    jsdom
    date-fns
    tough-cookie
    tslib
    ws@7.4.3
    ts-md5
    jsdom -g
    jieba
    fs
    form-data
    json5
    global-agent
    js-base64
    axios

2、Python3

    requests
    canvas
    ping3
    jieba

3、Linux
    bizCode
    bizMsg
    lxml

