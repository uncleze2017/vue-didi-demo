# Vue2.0 仿滴滴出行项目
最近，掘金上出现很多小伙伴的vue项目，趁着这股热潮我也用vue撸了一个滴滴出行的项目。

## 效果预览
> 在线预览：

> 项目地址：

* 主要技术栈

    * vue2.0(数据绑定)
    * vue-router(SPA)
    * vuex(管理组件状态，实现组件通信）
    * es6、html5、css3
* 组件库 

    mint-ui(有一些组件特别好用，方便快速开发)
* 字体库

    vue-awasome(完美支持font-awasome，此外还可以自定义组件)

* css动画库

   animate.css
* 高德地图 API
## 实现的功能


* 登录弹窗

    ![]()
* 验证弹窗

![]()
* 用户本地存储、退出(localStarage本地存储)
![]()
* 定位
![]()
* 地址输入提示
![]()
* 城市切换
![]()
* 实现出租车下单、呼叫、以及接单(此处处理上利用了假数据)
![]()
## 提问
写项目的时候遇到一个问题，希望网友能帮忙解答一下

#### 问题描述：

在state中建了一个position空对象用于存储address这个数据
于是我就在mutations里边将address作为position的属性存储。代码如下：

<code>

    state.position.city = position.city
    state.position.address =position.address //可以输出state存在address
</code>

虽然state里边有数据，但是，发现页面上的数据没有更新。
2个小时过去了，还是没解决，但是发现从其他页面切回来数据就会更新。
之后，用了如下代码就可以解决数据改变页面也跟着更新。

<code>

    const position = {
      address:result.aois[0].name,
      city: result.addressComponent.city
    }
    state.position = position
</code>
问题解决了，但是还是不懂具体的原因，希望网友帮忙解惑，十分感谢。


 另外给有兴趣写滴滴的朋友推荐先看下这篇文章["滴滴 webapp 5.0 Vue 2.0 重构经验分享"](https://juejin.im/post/58c8d226ac502e00587f60cd)，后悔写项目之前没看到这么好的经验分享，导致现在的代码一团糟，楼主接下来这段时间会将这个项目进行重写，代码乱先凑合着看吧。

 最后插播一个小广告：大四应届生，想找个实习岗，希望各位大佬给个机会。这是[我的简历]()