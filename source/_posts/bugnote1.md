---
   title: 记录一次小意外
   date: YYYY-MM-DD HH:mm:ss
   tags:
     - bug
   categories:
     - 技术
   cover: img/error2024-10-22
---
故事的起因是我在一次平常的deploy后我的博客文件就被清空了😫
要崩溃了

![github显示](img/bugnote1/error2024-10-22.png)
随后我排查了域名，dns解析，CNAME，ssh key，公钥等。。。
都没什么用，一看表晚上十一点了，实验室要关门了
回到宿舍打开todesk想继续排查，结果todesk也无了，最后看了一眼内存，发现内存已经15.3/16了，还以为是内存问题，想着第二天去重启一下包没问题的
结果今天一看还是没用
最后debug了下
```bash
$ hexo generate --debug
```
发现卡在opencv的标签上了
![gitbash](gitbash.png)
现在我再上传一边看看
## ---------我是分界线---------------
排查出不是标签问题，不是内存问题，不是
寄喽，还是不行
最后只能删库了，还好之前做了部署和备份，还有点文件可以用。
