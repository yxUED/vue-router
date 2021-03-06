# vue-router 代码注释

## 项目介绍
为了更好的在公司内部使用vue技术栈，我们尝试自己本地维护vue技术栈用到的核心库，在本地开发维护之前，我们需要去了解vue-router这个核心库的基本原理，而对已有的代码进行注释就是一个很好的学习方式。
### 项目目录

```
vue-router(项目目录)
           |
           |_ _ _
                |_ _ _ _  dist                            //分发目录
                |       |
                |       |_ _ _ _  vue-router.common.js    //基于 CommonJS 的完整构建                              
                |       |
                |       |_ _ _ _  vue-router.esm.js       //基于 ES Module 的完整构建
                |       |
                |       |_ _ _ _  vue-router.js           //基于 UMD 的完整构建,可以用于直接 CDN 引用
                |       |
                |       |_ _ _ _  vue-router.min.js       //vue-router.js的压缩版本
                |
                |_ _ _ _ types                            //接口声明文件的目录
                |       |
                |       |_ _ _ _  index.d.ts              //
                |       |
                |       |_ _ _ _  router.d.ts             //定义vue-router的接口
                |       |
                |       |_ _ _ _  vue.d.ts                //  
                |                      
                |_ _ _ _  LICENSE                         //版权说明
                |
                |_ _ _ _  package.json                    //项目配置文件
                |
                |_ _ _ _  README.md                       //项目说明


```

### 关于vue-router
vue-router是Vue.js官方的路由插件，它和vue.js是深度集成的，适合用于构建单页面应用。vue的单页面应用是基于路由和组件的，路由用于设定访问路径，并将路径和组件映射起来。传统的页面应用，是用一些超链接来实现页面切换和跳转的。在vue-router单页面应用中，则是路径之间的切换，也就是组件的切换。

### vue-router原理
先介绍下前端路由:      
前端路由是直接找到与地址匹配的一个组件或对象并将其渲染出来。改变浏览器地址而不向服务器发出请求有两种方式:   
1. 在地址中加入#以欺骗浏览器，地址的改变是由于正在进行页内导航.   
2. 使用H5的window.history功能，使用URL的Hash来模拟一个完整的URL.   
这两种方式分别对应vue-router的hash模式和history模式.   
hash模式和history的区别:   
由于内容比较长 详情请参考: <a href='https://blog.csdn.net/lla520/article/details/77894985'>https://blog.csdn.net/lla520/article/details/77894985</a>


## 加入我们
注释vue-router路由库的这个事情，我们希望能有更多的人参与，大家一起共同学习进步，只要加入yxUED这个组，就可以直接把您注释的内容提交上来。

### 近期任务
- 在readme中总结归纳vue-router的目录结构和各文件的作用，以及框架的设计思想；
- 在各核心文件中把该文件的作用写清楚；
- 注释各主要文件和核心函数和语句；
- 发布整理过的vue-router到公司内私有仓库，逐步在各项目替换；
- 将一些引用的库本地化，控制在10个以内；
- 关注官网的更新日志，把bug修复和新特性及时同步过来；

### 如何注释
- 先对着官网https://router.vuejs.org/zh-cn/的教程看源码；
- 后对着官网的API依次去源码找对应文件进行注释；
- 最好把github的源码工程clone到本地，对着提交记录学习后把注释写到本工程；
- 参照网上一些源码分析的教程或文章；

## 发布到内部仓库
- 全局安装cnpm: npm install -g cnpm --registry=https://registry.npm.taobao.org
- 设置全局cnpm的registry：cnpm set registry http://192.168.155.xx:7001
- 登陆：cnpm login 分别输入用户名、密码和邮箱（第一次输入的密码即为初始密码）
- 进入发布包的根目录，如： cd ~/mark/vue-router
- 输入： cnpm init 生成一个package.json文件，主要项目名必须为加 @yx/ 前缀，如：@yx/vue-router
- 执行：cnpm publish, 成功后在浏览器端http://192.168.155.xx:7002就能看到
