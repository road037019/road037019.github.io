---
title: 自建博客初体验
category: 入门文档
tag: hexo
---

## 1、 博客环境搭建
在会使用git之后，环境搭建的部分还算比较顺利，基本没出现什么大的问题，果然还是多经历就会越来越顺利的，不经历的话就会出现各种各样的奇怪的问题，当经历的多了，就会有自主的能力去规避这些问题，博客的建立主要是参考了[小白独立搭建博客](https://my.oschina.net/ryaneLee/blog/638440)，对作者深表感谢！
## 2、这是我的第一篇博客
```C++
#include <stdio.h>
int main(){
	printf("hello world! \n");
	return 0;
}
```
##  3、博客主题
看到hexo的一个特别好看的主题，名字叫做Even，但是我下载下来之后效果实在不咋的，和Even作者自己做的demo相差甚远，这个简洁的主题的作者也写了一篇关于做hexo主题的[文章](http://www.ahonn.me/2016/12/15/create-a-hexo-theme-from-scratch/)，我实在不奢求自己去做主题，只希望能根据他提供的线索把我的主题做的漂亮一点儿。
## 4、windows下的markdown编辑器
发现了一个markdown编辑器，特别好用，现在使用的就是这款，叫做Yu Writer，这样的话我就可以写静态博客，然后推送到远程了！
## 5、打造属于自己的博客主题
- landscape的主题参见博客：[教你定制Hexo的landscape打造自己的主题](https://www.jianshu.com/p/b96fd206571a)这儿的代码块部分真的是 太不好看了，主要的明色调的博客背景，突然的一块黑色的代码块，简直反人类
- 另一款叫做hexo-theme-BlueLake的主题[hexo-theme-BlueLake](https://github.com/chaooo/hexo-theme-BlueLake)，这个还比较不错，最主要是作者还添加了我心心念的博客搜索功能，代码块还比较友好，博客如何配置作者也写的比较清楚，详见:[BlueLake博客主题的详细配置](http://chaoo.oschina.io/2016/12/29/BlueLake%E5%8D%9A%E5%AE%A2%E4%B8%BB%E9%A2%98%E7%9A%84%E8%AF%A6%E7%BB%86%E9%85%8D%E7%BD%AE.html#comments)
- 文章的搜索框显示的内容“搜博主文章”，在\Hexo\themes\hexo-theme-BlueLake\layout\_partial\search.jade文件下，可以随意改动;  
- 文章的catagories(分类) tag(标签)Even作者都已经写好，在文章的标题一对“---”包括的部分添加category和tag字段就可以了。
- 如何在另一台电脑上写博客呢？


## 6、加上baidu统计
就按照网上的教程，搜索过之后，然后按照Even作者的提示，顺利添加成功。在网站的最下面的“本站访问总量”可以看到效果。

## 7、为博客添加评论系统
在为博客添加评论系统的过程中真的是 各种问题
- 一开始按照上面Even主题作者的推荐，首选 网易云跟帖评论，发现他停止服务了。
- 然后选择畅言，发现需要ICP备案号，这github服务器在国外，我也没有备案号，放弃！
- 多说就不用说了，之前我就知道它停止服务了
- 然后研究 来必力，这东西是韩国人做的，确认邮件动不动就给我来一波韩语，我还得谷歌翻译，这个东西倒是好弄，一会就弄好了，但是，网速是真慢啊，慢到压根刷不出来评论框
- 然后外国的不想选，那就选择友言吧，弄半天没什么反应，上网查了下说 不支持https，呵呵
- 最后一个选择，Disqus，也是外国的网站，但是没办法啊，不选择这个，就没有别的可选择了。。。
然后按照官网提示部署好之后，效果还可以，因为github本来就是在国外，总体上的速度比我想象中的快，还不错。
## 8 设置在不同的电脑上面更新博客
这个之前我是没想到的。
今天看博客(20180421),突然看到有人讨论这个问题，感觉还挺麻烦的。后来想想，也是，本地的网页的主题什么的其实都没有github上面存放，这样的话如果换台电脑，使用hexo如何生成网页？所以一个好的做法是把hexo相关的文件也上传到github，在需要在别的电脑上面使用的时候，从github上面git clone下来，然后就相当于拥有了hexo合成一个网页需要的各种文件，此时再安装下hexo，具体是一下几条命令：

- npm install hexo
- hexo init
- npm install
- npm install hexo-deployer-git
















