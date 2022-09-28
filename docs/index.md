---
home: true
# heroImage: /img/web.png
heroText: HUMAN-ROBOT
tagline: 属于人机共融的世界已到来，此篇献给为了HUMAN和ROBOT付出全部心血的你。—— YongLD
# actionText: 立刻进入 →
# actionLink: /web/
# bannerBg: auto # auto => 网格纹背景(有bodyBgImg时无背景)，默认 | none => 无 | '大图地址' | background: 自定义背景样式       提示：如发现文本颜色不适应你的背景时可以到palette.styl修改$bannerTextColor变量
pageClass: vdoing-index-class

features: # 可选的
  - title: Robot Issue
    details: 机器人技术文档、教程和总结
    link: /robotissue/
    imgUrl: https://cdn.jsdelivr.net/gh/YongLD/ld-blog@main/docs/.vuepress/public/img/robotissue.gif
  - title: MMML AI
    details: MultiModal Machine Learning 多模态应用
    link: /mmml/
    imgUrl: https://cdn.jsdelivr.net/gh/YongLD/ld-blog@main/docs/.vuepress/public/img/robot1.gif
  - title: CV AI
    details: Computer Vision 计算机视觉应用
    link: /cvai/ # 可选
    imgUrl: https://cdn.jsdelivr.net/gh/YongLD/ld-blog@main/docs/.vuepress/public/img/cvrobot.gif # 可选

# 文章列表显示方式: detailed 默认，显示详细版文章列表（包括作者、分类、标签、摘要、分页等）| simple => 显示简约版文章列表（仅标题和日期）| none 不显示文章列表
# postList: detailed
# simplePostListLength: 10 # 简约版文章列表显示的文章数量，默认10。（仅在postList设置为simple时生效）
# hideRightBar: true # 是否隐藏右侧边栏
---


<!-- 小熊猫 -->
<!-- <img src="/img/panda-waving.png" class="panda no-zoom" style="width: 130px;height: 115px;opacity: 0.8;margin-bottom: -4px;padding-bottom:0;position: fixed;bottom: 0;left: 0.5rem;z-index: 1;"> -->


<!--
## 关于

### 📚Blog
这是一个兼具博客文章、知识管理、文档查找的个人网站，主要内容是Web前端技术。如果你喜欢这个博客&主题欢迎到[GitHub](https://github.com/xugaoyi/vuepress-theme-vdoing)点个Star、获取源码，或者交换[友链](/friends/) ( •̀ ω •́ )✧

### 🎨Theme
本站主题是根据[VuePress](https://vuepress.vuejs.org/zh/)的默认主题修改而成。取名`Vdoing`(维度)，旨在轻松打造一个`结构化`与`碎片化`并存的个人在线知识库&博客，让你的知识海洋像一本本书一样清晰易读。配合多维索引，让每一个知识点都可以快速定位！ 更多[详情](https://github.com/xugaoyi/vuepress-theme-vdoing)。

<a href="https://github.com/xugaoyi/vuepress-theme-vdoing" target="_blank"><img src='https://img.shields.io/github/stars/xugaoyi/vuepress-theme-vdoing' alt='GitHub stars' class="no-zoom"></a>
<a href="https://github.com/xugaoyi/vuepress-theme-vdoing" target="_blank"><img src='https://img.shields.io/github/forks/xugaoyi/vuepress-theme-vdoing' alt='GitHub forks' class="no-zoom"></a>

</br>


## 特色功能
博客部分特色功能介绍

#### 一站式技术搜索

   博客内容中包含部分技术教程，可以利用搜索框快速搜索到相关文档，即使博客中没有的，你还可以选择最下方的 `在XXX中搜索“xxx”` 快速到达你想要找的内容。

#### 深色模式与阅读模式
关爱程序员，保护视力，点击右下角的主题模式按钮试试吧~

#### Demo演示模块
   为了更直观的展示一些代码的效果，博客添加了demo模块插件，可查看demo、源码，以及跳转到codepen在线编辑。**示例**：

::: demo [vanilla]
```html
<html>
  <div id="vanilla-box"></div>
</html>
<script>
  var box = document.getElementById('vanilla-box')
  box.innerHTML = 'Hello World! Welcome to EB'
</script>
<style>
#vanilla-box {
  color: #11a8cd;
}
</style>
```
:::


## :email: 联系

- **WeChat or QQ**: <a href="tencent://message/?uin=894072666&Site=&Menu=yesUrl" class='qq'>894072666</a>
- **Email**: <a href="mailto:894072666@qq.com">894072666@qq.com</a>
- **GitHub**: <https://github.com/xugaoyi>

</br>  -->

<ClientOnly>
  <WebInfo />
  <IndexBigImg />
  <Fantasy />
</ClientOnly>

<script>
// 已经不再使用
/*
触发全屏相关的代码
export default {
  mounted() {
    this.fullScreen();
    // 监听滚动
    window.addEventListener('scroll', () => {
      const index_class = document.getElementsByClassName('vdoing-index-class')[0];
      if(index_class){
        if(document.documentElement.scrollTop == 0){
          this.fullScreen();
        }else{
          this.exitScreen();
        }
      }
   });
  },
  watch: {
    $route(to, from) {
      if (to.path == "/" && Object.keys(this.$route.query).length == 0) {
       // 监听滚动
        window.addEventListener('scroll', () => {
          if(document.documentElement.scrollTop == 0){
            this.fullScreen();
          }else{
            this.exitScreen();
          }
        });
        this.fullScreen();
      }
    },
  },
  methods: {
    // 进入全屏
    fullScreen() {
      var el = document.documentElement;
      var rfs = el.requestFullScreen || el.webkitRequestFullScreen || el.mozRequestFullScreen || el.msRequestFullScreen;
      if (rfs) {
        rfs.call(el);
      } else if (typeof window.ActiveXObject !== "undefined") {
        // for IE，这里其实就是模拟了按下键盘的 F11，使浏览器全屏
        var wscript = new ActiveXObject("WScript.Shell");
        if (wscript != null) {
          wscript.SendKeys("{F11}");
        }
      }
    },
    // 退出全屏
    exitScreen() {
      var el = document;
      var cfs = el.cancelFullScreen || el.webkitCancelFullScreen || el.mozCancelFullScreen || el.exitFullScreen;
      if (cfs) {
        cfs.call(el);
      } else if (typeof window.ActiveXObject !== "undefined") {
        // for IE，这里和 fullScreen 相同，模拟按下 F11 键退出全屏
        var wscript = new ActiveXObject("WScript.Shell");
        if (wscript != null) {
          wscript.SendKeys("{F11}");
        }
      }
    }
  },
}
*/

</script>