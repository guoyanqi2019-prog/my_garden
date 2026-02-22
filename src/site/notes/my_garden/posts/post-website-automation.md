---
{"dg-publish":true,"permalink":"/my_garden/posts/post-website-automation/","title":"我用一个晚上，把网站的自动化更新系统搭起来了","tags":["一人探索","真实记录","工具探索"]}
---

数字花园
# 我用一个晚上，把网站的自动化更新系统搭起来了

晚上9点55分，我只是想解决一个小问题。

结果搞到深夜。

但我把一件以前完全不会做的事做成了。

---

## 从一个报错开始

最开始的问题很简单：首页的精选文章，我每次写新文章都要手动去 HTML 里加一条链接。

这件事本身不难，但很烦。

更烦的是，我不确定自己加的位置对不对。每次改完都要发布、等待、刷新，然后发现哪里又乱了。

我想要的很简单：**写完文章，一键更新，不用手动改任何东西。**

---

## 第一个方案：Python 脚本

我让 Claude 帮我写了一个 Python 脚本。

逻辑不复杂：扫描 `posts` 文件夹里所有文章，读取标题、日期、描述，按 tag 分类，然后自动填入首页和 posts 页面。

脚本写好了，运行成功了。

然后我发现 posts 页面出现了**三份重复内容**。

同样的文章列表，出现了三次。

原因是脚本用正则表达式匹配要替换的区域，但正则写得不够精准——每次运行，它找到了旧内容，把新内容追加进去，但没有删掉旧的。

运行一次就多一份。

---

## 第二个方案：标记注释

解决方法其实很简单，但我自己想不到——用两个 HTML 注释作为"锚点"：

```
<!-- AUTO_SECTIONS_START -->
<!-- AUTO_SECTIONS_END -->
```

脚本每次只替换这两个注释之间的内容，绝对不会影响外面的任何东西。

运行十次，结果都一样干净。

这个方法让我想到一个道理：**与其写聪明的代码，不如把问题定义清楚。**

---

## 然后是布局的连环问题

脚本搞定了，但首页的文章卡片显示出了问题。

我想要三列卡片，每张卡片有彩色背景图、标题、描述。

Digital Garden 渲染出来的效果是：三张卡片竖着排成一列，彩色背景变成了独立的方块，文字飘在旁边。

原因是我用了 emoji 做图标（📝🤖✍️），Digital Garden 对 emoji 的渲染支持有限，撑开了高度，破坏了 flex 布局。

删掉 emoji，换成纯色块。还是竖排。

换成纯文字列表。还是出问题——标题、描述、日期各自变成了独立的一行，中间有大段空白。

最后的解决方案是：**放弃所有 CSS class，全部用内联样式。**

Digital Garden 没有办法拆分一行 HTML，只能原样渲染。

问题解决了。

---

## 还有一个细节

做完之后，我发现文章标题是黑色的，看不出来是链接。

改成金色 `#C9922A`——和网站的整体配色一致。

首页、posts 页面、"查看所有文章"按钮，全部统一。

这种统一感，是从 Dan Koe 的网站里学来的：**所有可点击的东西，用同一种颜色。让人一眼就知道能点。**

---

## 最后的工作流

现在，每次我写完一篇新文章，只需要：

1. 在 Obsidian 里写文章，确保 frontmatter 里有 `dg-publish: true`
2. 双击 `更新页面.bat`
3. 在 Obsidian 点发布

三步，30秒，首页和文章列表自动更新。

---

## 我学到了什么

今晚最重要的不是那个脚本。

是这件事：

**我不是程序员，但我把一个程序员才会做的事做成了。**

不是因为我突然学会了编程。

是因为我能清晰地描述我想要什么，然后和 AI 一起把它做出来。

这个能力，比"会写代码"更值钱。

因为它可以迁移到任何地方。

---

如果你也有一个"想做但不知道怎么做"的小工具，不需要等自己学会编程。

先把你想要的结果描述清楚，然后开始尝试。

最坏的情况是：失败了，但你搞清楚了问题在哪。

最好的情况是：一个晚上，搞定了。

---

## 订阅我的周记

如果你也在探索 AI 工具、想从混乱走向系统，欢迎加入我的学习日志。每周一篇，真实记录，没有废话。
<div style="display: flex; align-items: center; gap: 40px; flex-wrap: wrap; margin: 20px 0;">
<div style="flex: 1; min-width: 260px; text-align: center;">
<img src="https://raw.githubusercontent.com/guoyanqi2019-prog/my_garden/main/src/site/img/ai-xiaobaima-profile.png" alt="AI小白马" style="max-width: 360px; width: 100%; border-radius: 12px; display: block; margin: 0 auto;" />
</div>
<div style="flex: 1; min-width: 260px;">
<script src="https://f.convertkit.com/ckjs/ck.5.js"></script>
<form action="https://app.kit.com/forms/9117923/subscriptions" style="background-color: rgb(255, 255, 255); border-radius: 6px;" class="seva-form formkit-form" method="post" data-sv-form="9117923" data-uid="3b70cc7e59" data-format="inline" data-version="5" data-options="{&quot;settings&quot;:{&quot;after_subscribe&quot;:{&quot;action&quot;:&quot;message&quot;,&quot;success_message&quot;:&quot;Success! Now check your email to confirm your subscription.&quot;,&quot;redirect_url&quot;:&quot;&quot;},&quot;analytics&quot;:{&quot;google&quot;:null,&quot;fathom&quot;:null,&quot;facebook&quot;:null,&quot;segment&quot;:null,&quot;pinterest&quot;:null,&quot;sparkloop&quot;:null,&quot;googletagmanager&quot;:null},&quot;modal&quot;:{&quot;trigger&quot;:&quot;timer&quot;,&quot;scroll_percentage&quot;:null,&quot;timer&quot;:5,&quot;devices&quot;:&quot;all&quot;,&quot;show_once_every&quot;:15},&quot;powered_by&quot;:{&quot;show&quot;:true,&quot;url&quot;:&quot;https://kit.com/features/forms?utm_campaign=poweredby&amp;utm_content=form&amp;utm_medium=referral&amp;utm_source=dynamic&quot;},&quot;recaptcha&quot;:{&quot;enabled&quot;:false},&quot;return_visitor&quot;:{&quot;action&quot;:&quot;show&quot;,&quot;custom_content&quot;:&quot;&quot;},&quot;slide_in&quot;:{&quot;display_in&quot;:&quot;bottom_right&quot;,&quot;trigger&quot;:&quot;timer&quot;,&quot;scroll_percentage&quot;:null,&quot;timer&quot;:5,&quot;devices&quot;:&quot;all&quot;,&quot;show_once_every&quot;:15},&quot;sticky_bar&quot;:{&quot;display_in&quot;:&quot;top&quot;,&quot;trigger&quot;:&quot;timer&quot;,&quot;scroll_percentage&quot;:null,&quot;timer&quot;:5,&quot;devices&quot;:&quot;all&quot;,&quot;show_once_every&quot;:15}},&quot;version&quot;:&quot;5&quot;}" min-width="400 500 600 700 800"><div data-style="full"><div data-element="column" style="background-image: url(&quot;https://embed.filekitcdn.com/e/eT41znAKxqkkdPQHNBpD4L/qT9YNZj3aGQZBoPXf9bEFg&quot;);" class="formkit-background"></div><div data-element="column" class="formkit-column"><div class="formkit-header" style="color: rgb(83, 83, 83); font-size: 24px; font-weight: 700;" data-element="header"><h2>加入我的 <br>AI 学习成长日志</h2></div><ul class="formkit-alert formkit-alert-error" data-element="errors" data-group="alert"></ul><div data-element="fields" class="seva-fields formkit-fields"><div class="formkit-field"><input class="formkit-input" name="email_address" style="color: rgb(139, 139, 139); border-color: rgb(221, 224, 228); font-weight: 400;" aria-label="Email Address" placeholder="Email Address" required="" type="email"></div><button data-element="submit" class="formkit-submit formkit-submit" style="color: rgb(255, 255, 255); background-color: rgb(212, 168, 67); border-radius: 3px; font-weight: 700;"><div class="formkit-spinner"><div></div><div></div><div></div></div><span class="">获取免费PDF文档及资源包</span></button></div><div class="formkit-disclaimer" style="color: rgb(139, 139, 139); font-size: 13px;" data-element="disclaimer"><p><strong>每周更新，我的实战与学习经验，陪你成长</strong></p></div><div class="formkit-powered-by-convertkit-container"><a href="https://kit.com/features/forms?utm_campaign=poweredby&amp;utm_content=form&amp;utm_medium=referral&amp;utm_source=dynamic" data-element="powered-by" class="formkit-powered-by-convertkit" data-variant="dark" target="_blank" rel="nofollow">Built with Kit</a></div></div></div></form>
</div>
</div>




*AI小白马 · 每周更新 · 真实记录*
