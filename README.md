
# 继承自自己的quickmobile以及smartphp 、72bian等php开发资源，参考了tp、canphp等开发框架


# 以面向接口、快速开发、缓存优化、模块清晰、前后端分离等思想为指导，开发一个通用的php开发平台。


## 面向接口
系统所有开发均类似开发手机api接口类似的模式。数据格式默认为json，手机接口直接返回json。网页直接返回html代码，然后html请求接口再返回数据。

---管理后台等可选择性的配置支持用传统的开发模式，例如smart或者php模板引擎。

##快速开发
系统会默认实现一些通用模块，这样在开发的时候拿来即用。计划会有会员模块、文章模块、微博模块、支付模块、微信模块

##缓存优化
接口都是可以配置的，配置是否可用，是否允许缓存，允许的缓存多久等

##模块清晰
默认的模块都在apps下面，apps下面的根目录中的每一个文件夹相当于一个app，这些app可以单独运行也可以和其他app一起运行。可以支持独立部署，支持有自己的数据库。

##前后端分离
开发非手机接口的时候，传统的流程是 请求===》服务器接受请求===》控制器调用model拿数据====》控制器把数据给view===》view拿到模板把数据渲染====》控制器输出html网页；
这里的开发模式通常是，请求==》服务器接受请求，返回html模板 ===》html模板请求服务器===》服务器调用model等返回json数据====》html模板拿到数据用angular等之类的工具渲染到页面。

这样意味着用户能第一时间看见页面，后面的数据慢慢展示呗。。。
这意味着很多时候，手机端和网页端只写一个api接口就够了，逻辑自然也是一套逻辑哦！


##万能model
系统内置model，只要继承自动具有增删查改


##自动加载
之前写的72bian、smartphp等，我考虑到等到用的时候才require php的类会影响效率，但这样其实是影响了开发效率。查阅了一些资料，开始我的想法可能是多虑了。
这里支持类的自动加载。


##单元测试
单元测试是框架稳定的保证。不写单元测试的程序员都是耍流氓，嗯哼


大家快加入吧！
