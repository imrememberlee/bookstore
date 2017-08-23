# gvm安装go
### gvm是第三方开发的Go多版本管理工具，类似ruby里面的rvm工具，node.js里面的nvm工具。使用起来相当的方便，安装gvm使用如下命令：
```
bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
```

### 由于大家都懂得原因需要先修改镜像来下载安装包
可将 GO_SOURCE_URL修改为github上的源码镜像
```
vim ~/.gvm/scripts/install
" GO_SOURCE_URL=https://go.googlecode.com " 修改为 " GO_SOURCE_URL=https://github.com/golang/go "
```

### 安装1.5之后的版本需要先安装1.4版本
```
gvm install go1.4 -B
gvm use go1.4
export GOROOT_BOOTSTRAP=$GOROOT
gvm install go1.8.3
```

### 设置默认使用的go版本
```
gvm use go1.8.3 --default
```