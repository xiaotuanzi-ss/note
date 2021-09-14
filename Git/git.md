
- github提交报错：LibreSSL SSL_connect: SSL_ERROR_SYSCALL in connection to github.com:443
```
环境：MacOS 10.15.4
科学上网的情况下，能够git clone，但是在git push操作时出现以上问题，搜了搜确实是代理出现了问题，解决方法基本都是关掉代理，本人则重新设置了代理，vim ~/.gitconfig内容如下：

[https "https://github.com"]
proxy = https://127.0.0.1:1086
[http "https://github.com"]
proxy = socks5://127.0.0.1:1086
[user]
name = JohnJim0816
```