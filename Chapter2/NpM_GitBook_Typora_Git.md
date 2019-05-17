# 第1节：GitBooK使用

# NpM_GitBook_Typora_Git
NpM_GitBook_Typora_Git组合使用

### GitBook 是基于 Node.js，所以我们首先需要安装 Node.js

[Node.js](https://github.com/PlatoJobs/NpM_GitBook_Typora_Git/blob/master/node-v12.2.0.pkg)

+ 现在安装 `Node.js` 都会默认安装 `npm（node 包管理工具）`，所以我们不用单独安装 `npm`，打开命令行，执行以下命令安装 `GitBook`
```linux
npm install -g gitbook-cli
```
+ 安装Typora
  1. [Typora](https://typora.io) 切记需要翻墙

  2. [本地Typora](https://github.com/PlatoJobs/NpM_GitBook_Typora_Git/blob/master/Typora.dmg) 下载安装即可



```linux

Last login: Wed May 15 11:47:58 on ttys000
macdeMacBook-Air:~ mac$ npm --version
-bash: npm: command not found
macdeMacBook-Air:~ mac$ npm help
-bash: npm: command not found
macdeMacBook-Air:~ mac$ npm install -g gitbook-cli
-bash: npm: command not found
macdeMacBook-Air:~ mac$ npm install -g gitbook-cli
npm WARN checkPermissions Missing write access to /usr/local/lib/node_modules
npm ERR! path /usr/local/lib/node_modules
npm ERR! code EACCES
npm ERR! errno -13
npm ERR! syscall access
npm ERR! Error: EACCES: permission denied, access '/usr/local/lib/node_modules'
npm ERR!  [Error: EACCES: permission denied, access '/usr/local/lib/node_modules'] {
npm ERR!   stack: "Error: EACCES: permission denied, access '/usr/local/lib/node_modules'",
npm ERR!   errno: -13,
npm ERR!   code: 'EACCES',
npm ERR!   syscall: 'access',
npm ERR!   path: '/usr/local/lib/node_modules'
npm ERR! }
npm ERR! 
npm ERR! The operation was rejected by your operating system.
npm ERR! It is likely you do not have the permissions to access this file as the current user
npm ERR! 
npm ERR! If you believe this might be a permissions issue, please double-check the
npm ERR! permissions of the file and its containing directories, or try running
npm ERR! the command again as root/Administrator (though this is not recommended).

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/mac/.npm/_logs/2019-05-17T02_23_14_256Z-debug.log
macdeMacBook-Air:~ mac$ sudo chown -R $USER /usr/local
Password:
macdeMacBook-Air:~ mac$ npm install -g gitbook-cli
/usr/local/bin/gitbook -> /usr/local/lib/node_modules/gitbook-cli/bin/gitbook.js
+ gitbook-cli@2.3.2
added 578 packages from 672 contributors in 28.567s


```

> 现在你准备构建一本书籍，你在硬盘上新建了一个叫 mybook 的文件夹，按照以前的做法，你会新建一个 Word 文档，写上标题，然后开始巴滋巴滋地笔耕。

  但是现在有了 GitBook，你首先要做的是在 mybook 文件夹下执行以下命令：

```linux
gitbook init
```

执行完后，你会看到多了两个文件 —— `README.md` 和 `SUMMARY.md`，它们的作用如下：

>README.md ---书籍的介绍写在这个文件里
>
>SUMMARY.md----书籍的目录结构在这里配置

编辑 —`SUMMARY.md`文件

接着我们执行 `gitbook serve` 来预览这本书籍，执行命令后会对 Markdown 格式的文档进行转换，默认转换为 html 格式，最后提示 `Serving book on http://localhost:4000`。 嗯，打开浏览器看一下吧：

> 你可以执行 `gitbook build` 命令构建书籍，默认将生成的静态网站输出到 _book 目录。实际上，这一步也包含在 `gitbook serve` 里面，因为它们是 HTML，所以 GitBook 通过 Node.js 给你提供服务了。

结束了。

