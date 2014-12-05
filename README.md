Prepare
=======

Prepare 是记录一些总结，比如在换新电脑的时候，配置锋利的开发环境、配置命令行友好环境、一些关于自己的经验等等。

随手描画，请不要吐槽哦！

现在的程序员，生活水平提高了，所以会尝遇到熟悉环境的切换问题，于是就开始总结那些大牛们的说法和想法，为什么每次都可以站在巨人肩膀上看世界呢？       

### 我自个的建议是：
1. 不要把你的代码看的太重，分享出来。大家都会出于好奇运行起来，无意中帮忙检查了代码的健壮性，这何乐而不为呢？                      
2. 把你想的完美idea说出来，大家都会无意中帮你产品做减法和适当的加法，idea就算被偷了，那也无所谓，能执行下去         才是王道，把想法产品化了才是你真正关心的地方。

这些是我的师傅[lerosua](https://github.com/lerosua)教导的.

在YY，我们经常叫他春哥，之所以有句话，不要信我，信疗效。

### 首先肯定是配置好你的Mac机器
1. 最近xcode的更新，iOS SDK的更新，迫不得已需要把Mac机器的系统更新到最新版本，         
我们不吐槽新系统怎么样哈！为了学习更多新的知识，手动尝试更多代码，那么你就忍着跟随升级吧！

2. 不负责的说：电脑准备好了，千万不要一开始就输入Apple ID，下载Xcode，clone项目下来就开始做，这样会很吃亏的，      起码你得把常用Mac的软件Dwon下来吧？比如你经常需要收发邮件、写文档好帮手、浏览器标签同步、印象笔记等等，让你有        一个熟悉又温馨的环境，这不是更好进入状态吗？                

3. 为什么还没到下载Xcode的时候呢？哈哈！其实我也在想，我说这些，不知道会不会被人骂。我个人是赞成git命令和客户端     配合一起使用的，所以需要配置好SSH，git的快捷键等等，如果你是不甘心于工作的话，比如可以安装录像工具、PhotoShop、      Reeder等等软件。娱乐的你们自行选择吧！我是个无趣的人。哈哈！             

4. 下载你的Xcode，很多人喜欢安装多个版本的Xcode，但是个人觉得新版Xcode优化的很不错了，请不要再停留在iOS5了，很多     复杂的工作在iOS7/8已经很完美的支持了，个人是不会屈服于其他无关紧要的外界，利用自己的时间，学习新的技术方案，对       自己还是有很多好处的。

5. 等待下载Xcode的过程是很痛苦的，那么你可以看看自己写的编程规范、自己写的框架、别人的规范、别人的框架，于是         你会看到自己有一些不足，想修改吗？想fix吗？想优化吗？哈哈！Xcode还没下载完，不要急，修炼一下你的内容境界，不要       急于某一关键点，你需要时间去思考为什么自己会这样犯错，别人却不会，别找借口，好好的改变自己，时间都是自己挤出来的。                 
6. 在思考反思中度过，是不是感觉整个人都安静了？别睡着了，是时候配置你的利器了，刚刚下载的Xcode是多么的迟钝，你要    把它变得锋利起来，那是你的武器，很多人说，我是走管理方向的，何必要把编程当作自己的重要部分，好吧！我们不在同一       频道上，你继续，我慢慢写。

7. 这时候就需要跳转到[XHXcodePlugin](https://github.com/xhzengAIB/XHXcodePlugin)，安装适合你使用的插件，如果有更好的插件提供，请告诉我哦！个人精力有限嘛！

8. 新建一个Demo测试一下那些插件，咦！好像可以用哦！那么就好，Xcode回血了，你也清醒了！我们可以开始代码之旅吧！

### 丰富你的电脑

1. 终端的配置
想找到.gitconfig文件，却无从下手，对终端一无所知，在春哥的调教下，终于有一些了解了，于是找到了对应文件，在终端输入以下命令：
````objc
  cd /Users/这里改为你的机器名/
  vi .gitconfig
  这时候处于查看状态，键盘输入i，进入编辑状态
  插入
  [alias]
        co = checkout
        ci = commit -a
        st = status
        br = branch
        tree = log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short


  个人之前的配置文件如下：
  [user]
        name = Jack
        email = xhzengAIB@gmail.com
  [alias]
        co = checkout
        ci = commit -a
        st = status
        br = branch
        l  = log --stat

还有另外一个用法，SSH端口、git地址端口，这里就不放出来了！
````

2. 安装一些好用的App

能同步书签的浏览器-----[Chrome for Mac](https://www.google.com/intl/en/chrome/browser/desktop/index.html)                    
可以写PHP代码的IDE---[Sublime](http://www.sublimetext.com/)                    
SVN工具------------------[Versions](http://versionsapp.com/)                    
处理多邮箱的邮件-------[Foxmail](https://itunes.apple.com/cn/app/foxmail/id617950461?mt=12)             
云笔记--------------------[Evernote](https://evernote.com/intl/zh-tw/download/)                  
Git工具------------------[Github](https://mac.github.com/)
                    
3. 保护身体的App，这个一定得装。

4. 安装Cocoapods，必须得安装啊！不是依赖，而是好管理源码！
把你的VPN连接上，得到特权，来吧！做你喜欢做的事情，【sudo】 gem install cocoapods，那么我们来测试一下是否安装成功。
````objc
  pod search MessageDisplayKit
````
如果出现如下字眼，那说明可以开始使用Cocoapods了。                             
-> MessageDisplayKit (0.2.7)
   An IM App like WeChat App has to send text, pictures, audio, video, location
   messaging, managing address book, more interesting features.
   pod 'MessageDisplayKit', '~> 0.2.7'
   - Homepage: https://github.com/xhzengAIB/MessageDisplayKit
   - Source:   https://github.com/xhzengAIB/MessageDisplayKit.git
   - Versions: 0.2.7, 0.2.6, 0.2.5, 0.2.4, 0.2.3, 0.2.2, 0.2.1, 0.2, 0.1.9, 0.1.8,
   0.1.7, 0.1.6, 0.1.5, 0.1.4, 0.1.3, 0.1.2, 0.1.1, 0.1.0 [master repo]

不过网上有很多方法是不需要VPN就可以安装，那么我说一下注意事项吧！
我觉得需要先用'gem sources -l' 先查看一下源，然后具体再删除不可用、添加可以用的源，以免死板的复制教程中的命令行。

个人的做法如下:
````objc
  gem source -l
  得到如下输出：
  *** CURRENT SOURCES ***

  http://ruby.taobao.org/
  http://rubygems.org/
  这时候我发现已经添加过http://ruby.taobao.org/，所以我不需要重复的添加了，
  但是这时候需要删除另外一个源，那么网上的教程可能是:
  gem sources --remove https://rubygems.org/
  但是我这里确实http，而不是https，所以需要自己对应好，才能删除成功啊！
  然后就进行安装吧！

````

### 总结和注意的项

### 需要重新学习和认识的知识

1. App的icon处理，还是有点闹心的，还是用插件吧！只要设计师给你一个1024像数的icon，你就可以完美的生成其他icon，所以我必备的装备哦！无论是个人开发者还是公司开发者，节省时间嘛！插件的链接[makeappicon](http://makeappicon.com/)。

2. 有趣的配置
在命令行git提交的时候，自动拍照留影。

- 确保你系统有brew，如果没有，那么你可以在google上找答案。
- 安装命令行拍照程序
```
brew install imagesnap
```
- 确保 ~/.git_template/hooks 目录存在
```
mkdir -p ~/.git_template/hooks
```
- 在上面目录下面建立post-commit文件
- 将以下内容键入并保存, file=后面是你保存图片的目录，请自行更改
```
#!/bin/sh
file="/Users/leros/Pictures/snapshot/Git_$(date +%Y-%m-%d-%H.%M.%S).jpg"
echo "Taking capture into ${file}!"
imagesnap -q  -w 3 $file &
```
注意/Users/leros/Pictures/snapshot是我的文件目录，请你自行修改，如果你只是复制的话，那很大可能GG。
- 添加文件执行权限
```
chmod +x ~/.git_template/hooks/post-commit
```
- 以后执行git ci -m "" 的时候，会自动调用这个脚本，生成快照。
- have a fun!

                  
未完待续......
