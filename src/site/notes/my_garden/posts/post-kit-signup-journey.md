---
{"dg-publish":true,"permalink":"/my_garden/posts/post-kit-signup-journey/","title":"我注册 Kit 邮件订阅的全过程：一个普通人踩过的所有坑","tags":["AI学习","工具探索","真实记录"]}
---


# 我注册 Kit 邮件订阅的全过程：一个普通人踩过的所有坑

我花了一整天，才把一个"看起来很简单"的邮件订阅表单搞定。

不是因为我笨。

是因为没有人告诉我，这中间有多少个坑。

今天我把这个过程完整记录下来。如果你也想搭建自己的邮件列表，这篇文章能帮你少走很多弯路。

---

## 为什么要做邮件订阅？

在开始之前，我想说清楚我为什么做这件事。

社交媒体的算法随时可以让你消失。

今天你有1000个粉丝，明天平台改规则，你的内容可能没人看到。

但邮件列表不一样。**那是你真正拥有的受众。**

Dan Koe 说过：邮件列表是创作者最重要的资产之一。不是粉丝数，不是点赞数——是那些主动把邮箱给你、愿意收到你消息的人。

所以我决定从现在就开始建。哪怕第一天只有0个订阅者。

---

## 第一步：选择工具

市面上邮件订阅工具很多：Mailchimp、Beehiiv、Substack、Kit……

我选择 **Kit（原 ConvertKit）** 的原因很简单：

- Dan Koe 用的就是它
- 专门为创作者设计，不是为企业营销
- 免费版支持到1000个订阅者，够我用很久

---

## 第二步：注册和设计表单

注册本身很顺利，5分钟搞定。

麻烦的是**设计表单**。

Kit 提供了几个模板，我选了 Charlotte——左边图片右边表单的双列布局。默认是粉色日落背景图，和我的网站风格完全不搭。

我的网站是白底金色极简风。粉色日落？不行。

于是开始改造：

**配色：** 把按钮颜色从粉色改成金色 `#C9922A`，和网站保持一致。

**背景图：** 这里遇到了第一个坑。

我想用一张有个人品牌感的图——头像加微信公众号二维码。但两张图拼在一起很难看，于是用 Claude 帮我合成了一张完整的竖图：圆形素描头像 + 金色圆环 + 微信二维码，整体白底极简。

效果出乎意料地好。

**第二个坑：表单宽度。**

把图片上传后，左侧图片在文章里消失了。

原因是：Charlotte 模板需要容器足够宽才会显示双列，嵌入文章后容器太窄，自动折叠成单列，图片就没了。

试了各种 CSS 方法，最终放弃——把图片从表单里拿出来，直接作为普通图片放在表单上方。反而更灵活。

---

## 第三步：账号审核——最意外的坑

表单设计好了，满心欢喜准备发布。

结果发现：**输入邮箱后没有任何反应。**

仔细看才发现顶部有一条黄色提示：

> "Some features of your account are disabled."

点进去，是 Kit 的客服机器人。它告诉我：**新账号需要人工审核才能发送邮件。**

这是我完全没预料到的。

客服问了我六个问题：

1. 你的网站和社交媒体链接是什么？
2. 你创作什么内容，如何为受众提供价值？
3. 你会发送联盟营销链接吗？
4. 你是销售自己的产品还是推广别人的业务？
5. 你以前发过营销邮件吗？
6. 你会导入已有订阅者吗？

我一一回答，全部如实说明。

然后等待。审核周期最长24小时。

---

## 第四步：邮箱域名问题

以为回答完问题就结束了。

结果审核团队又来了一封邮件：

> "你当前的邮箱域名经常被标记为垃圾邮件，建议换一个发送地址。"

我用的是163邮箱。确实，163在国际邮件服务里信誉不太好。

解决方案：添加一个 Gmail 邮箱作为发送地址。

操作路径：Kit Settings → Email → Add from address

添加后需要去 Gmail 收确认邮件，点击确认链接，然后设为默认发送地址。

回复客服说明已添加，等待最终审核通过。

---

## 整个过程花了多长时间？

- 注册账号：5分钟
- 设计表单：3小时（大部分时间在纠结配色和图片）
- 处理审核：1天（等待 + 回答问题 + 解决邮箱问题）

**总计：约1天。**

如果你提前知道这些，可能2小时就搞定了。

---

## 给想做邮件订阅的人的建议

**第一：** 用 Gmail 注册和发送，不要用163、QQ邮箱，避免被标记垃圾邮件。

**第二：** 提前准备好网站链接和内容介绍，审核问题基本都是这些。

**第三：** 表单设计不要追求完美，能用就发布，之后可以慢慢改。

**第四：** 从今天就开始建，哪怕第一天0订阅者。你现在种下的种子，半年后会感谢自己。

---

## 写在最后

我不是在告诉你"我成功了，你也行"。

我只是在记录：**一个普通人，今天做了这件事，踩了这些坑，然后继续往前走了。**

如果你也在这条路上，欢迎加入我的周记。每周一篇，真实记录。

---

<div style="display: flex; align-items: center; gap: 40px; flex-wrap: wrap; margin: 20px 0;">
<div style="flex: 1; min-width: 260px; text-align: center;">
<img src="https://raw.githubusercontent.com/guoyanqi2019-prog/my_garden/main/src/site/img/ai-xiaobaima-profile.png" alt="AI小白马" style="max-width: 360px; width: 100%; border-radius: 12px; display: block; margin: 0 auto;" />
</div>
<div style="flex: 1; min-width: 260px;">
<script src="https://f.convertkit.com/ckjs/ck.5.js"></script>
<form action="https://app.kit.com/forms/9117923/subscriptions" style="background-color: rgb(255, 255, 255); border-radius: 6px;" class="seva-form formkit-form" method="post" data-sv-form="9117923" data-uid="3b70cc7e59" data-format="inline" data-version="5" data-options="{&quot;settings&quot;:{&quot;after_subscribe&quot;:{&quot;action&quot;:&quot;message&quot;,&quot;success_message&quot;:&quot;Success! Now check your email to confirm your subscription.&quot;,&quot;redirect_url&quot;:&quot;&quot;},&quot;analytics&quot;:{&quot;google&quot;:null,&quot;fathom&quot;:null,&quot;facebook&quot;:null,&quot;segment&quot;:null,&quot;pinterest&quot;:null,&quot;sparkloop&quot;:null,&quot;googletagmanager&quot;:null},&quot;modal&quot;:{&quot;trigger&quot;:&quot;timer&quot;,&quot;scroll_percentage&quot;:null,&quot;timer&quot;:5,&quot;devices&quot;:&quot;all&quot;,&quot;show_once_every&quot;:15},&quot;powered_by&quot;:{&quot;show&quot;:true,&quot;url&quot;:&quot;https://kit.com/features/forms?utm_campaign=poweredby&amp;utm_content=form&amp;utm_medium=referral&amp;utm_source=dynamic&quot;},&quot;recaptcha&quot;:{&quot;enabled&quot;:false},&quot;return_visitor&quot;:{&quot;action&quot;:&quot;show&quot;,&quot;custom_content&quot;:&quot;&quot;},&quot;slide_in&quot;:{&quot;display_in&quot;:&quot;bottom_right&quot;,&quot;trigger&quot;:&quot;timer&quot;,&quot;scroll_percentage&quot;:null,&quot;timer&quot;:5,&quot;devices&quot;:&quot;all&quot;,&quot;show_once_every&quot;:15},&quot;sticky_bar&quot;:{&quot;display_in&quot;:&quot;top&quot;,&quot;trigger&quot;:&quot;timer&quot;,&quot;scroll_percentage&quot;:null,&quot;timer&quot;:5,&quot;devices&quot;:&quot;all&quot;,&quot;show_once_every&quot;:15}},&quot;version&quot;:&quot;5&quot;}" min-width="400 500 600 700 800"><div data-style="full"><div data-element="column" style="background-image: url(&quot;https://embed.filekitcdn.com/e/eT41znAKxqkkdPQHNBpD4L/qT9YNZj3aGQZBoPXf9bEFg&quot;);" class="formkit-background"></div><div data-element="column" class="formkit-column"><div class="formkit-header" style="color: rgb(83, 83, 83); font-size: 24px; font-weight: 700;" data-element="header"><h2>加入我的 <br>AI 学习成长日志</h2></div><ul class="formkit-alert formkit-alert-error" data-element="errors" data-group="alert"></ul><div data-element="fields" class="seva-fields formkit-fields"><div class="formkit-field"><input class="formkit-input" name="email_address" style="color: rgb(139, 139, 139); border-color: rgb(221, 224, 228); font-weight: 400;" aria-label="Email Address" placeholder="Email Address" required="" type="email"></div><button data-element="submit" class="formkit-submit formkit-submit" style="color: rgb(255, 255, 255); background-color: rgb(212, 168, 67); border-radius: 3px; font-weight: 700;"><div class="formkit-spinner"><div></div><div></div><div></div></div><span class="">获取免费PDF文档及资源包</span></button></div><div class="formkit-disclaimer" style="color: rgb(139, 139, 139); font-size: 13px;" data-element="disclaimer"><p><strong>每周更新，我的实战与学习经验，陪你成长</strong></p></div><div class="formkit-powered-by-convertkit-container"><a href="https://kit.com/features/forms?utm_campaign=poweredby&amp;utm_content=form&amp;utm_medium=referral&amp;utm_source=dynamic" data-element="powered-by" class="formkit-powered-by-convertkit" data-variant="dark" target="_blank" rel="nofollow">Built with Kit</a></div></div></div></form>
</div>
</div>

---

*AI小白马 · 每周更新 · 真实记录*
