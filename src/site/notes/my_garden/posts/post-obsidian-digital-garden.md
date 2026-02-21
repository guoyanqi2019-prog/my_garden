---
{"dg-publish":true,"permalink":"/my_garden/posts/post-obsidian-digital-garden/","title":"用 Obsidian 建数字花园的完整过程","tags":["效率工具","Obsidian","数字花园"]}
---


<style>
.article-wrap { max-width: 680px; margin: 0 auto; padding: 3rem 2rem; }
.article-tag { font-size: 0.8rem; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; color: #e53e3e; margin-bottom: 1rem; }
.article-wrap h1 { font-size: 2rem; font-weight: 800; color: #111; line-height: 1.2; margin: 0 0 1rem; }
.article-meta { font-size: 0.85rem; color: #bbb; margin-bottom: 2.5rem; display: flex; gap: 1rem; flex-wrap: wrap; }
.article-wrap p { font-size: 1rem; color: #333; line-height: 1.9; margin-bottom: 1.5rem; }
.article-wrap h2 { font-size: 1.2rem; font-weight: 700; color: #111; margin: 2.5rem 0 1rem; }
.article-wrap h3 { font-size: 1rem; font-weight: 700; color: #333; margin: 1.5rem 0 0.5rem; }
.article-divider { border: none; border-top: 1px solid #eee; margin: 2.5rem 0; }
.article-highlight { background: #f9f9f9; border-left: 3px solid #e53e3e; padding: 1rem 1.5rem; border-radius: 0 8px 8px 0; margin: 1.5rem 0; font-size: 0.95rem; color: #444; font-style: italic; }
.step-box { background: #f9f9f9; border-radius: 8px; padding: 1.5rem; margin: 1.5rem 0; }
.step-box h3 { margin: 0 0 0.5rem; color: #111; font-size: 0.95rem; }
.step-box p { margin: 0; font-size: 0.9rem; color: #555; line-height: 1.7; }
.step-number { display: inline-block; background: #e53e3e; color: #fff; width: 24px; height: 24px; border-radius: 50%; font-size: 0.75rem; font-weight: 700; text-align: center; line-height: 24px; margin-right: 0.5rem; }
.tip-box { background: #fffaf0; border: 1px solid #fbd38d; border-radius: 8px; padding: 1rem 1.5rem; margin: 1.5rem 0; font-size: 0.9rem; color: #744210; }
.warn-box { background: #fff5f5; border: 1px solid #feb2b2; border-radius: 8px; padding: 1rem 1.5rem; margin: 1.5rem 0; font-size: 0.9rem; color: #742a2a; }
.article-cta { background: #111; color: #fff; padding: 2rem; border-radius: 8px; margin-top: 3rem; text-align: center; }
.article-cta h3 { color: #fff; margin: 0 0 0.5rem; }
.article-cta p { color: #aaa; font-size: 0.9rem; margin-bottom: 1rem; }
.article-cta a { background: #e53e3e; color: #fff; padding: 0.6rem 1.5rem; border-radius: 4px; text-decoration: none; font-weight: 600; font-size: 0.9rem; }
.article-back { font-size: 0.85rem; color: #e53e3e; text-decoration: none; }
.article-back:hover { text-decoration: underline; }
</style>

<div class="article-wrap">

<a class="article-back" href="/my_garden/posts">← 返回文章列表</a>

<br><br>

<div class="article-tag">效率工具</div>

<h1>非程序员也能搞定：用 Obsidian 建数字花园的完整过程</h1>

<div class="article-meta">
  <span>作者：AI小白马</span>
  <span>2026年2月21日</span>
  <span>阅读约 8 分钟</span>
</div>

<p>我不会写代码。</p>

<p>但你现在看到的这个网站，是我一步一步从零搭起来的。用的工具叫 Obsidian，加一个叫 Digital Garden 的插件，部署在 GitHub 和 Vercel 上，全部免费。</p>

<p>这篇文章记录的是我真实走过的完整过程——包括踩过的坑、卡住的地方、以及最后搞定的方法。</p>

<div class="article-highlight">
  如果你也对科技感兴趣但不会编程，这篇文章就是写给你的。
</div>

<hr class="article-divider">

<h2>大多数人对"建网站"的理解是错的</h2>

<p>一提到"建个人网站"，大多数人脑子里冒出来的画面是：写代码、租服务器、配置域名、调试半天……光想想就头大。</p>

<h3>错误认知一：建网站必须会写代码</h3>
<p>不是的。Obsidian + Digital Garden 的组合，让你只需要写普通的 Markdown 文档，插件帮你把它变成网站。你写笔记，它发布网页，就这么简单。</p>

<h3>错误认知二：免费的方案效果很差</h3>
<p>GitHub 存储 + Vercel 托管，这套组合完全免费，而且速度很快，你现在看到的这个网站就是这么跑起来的。</p>

<h3>错误认知三：一次配好就完事了</h3>
<p>这是我自己踩过的坑。配置过程中会遇到各种小问题，比如图片路径、导航链接、URL 格式……但每个问题都有解法，一个一个解决就好。</p>

<hr class="article-divider">

<h2>搭好之后你能得到什么</h2>

<h3>一个真正属于你的地方</h3>
<p>不依赖任何平台，不担心账号被封、内容被删。你的笔记在本地，代码在 GitHub，网站在 Vercel。三个地方都有备份。</p>

<h3>写作即发布的工作流</h3>
<p>在 Obsidian 里写完一篇笔记，加一行 <code>dg-publish: true</code>，点发布，两分钟后网站更新。整个流程比发微信公众号还简单。</p>

<h3>知识会越来越值钱</h3>
<p>数字花园最大的好处是：文章之间可以互相链接，慢慢形成一张知识网络。时间越长，内容越多，整体价值越高。这是在任何社交平台上都做不到的事。</p>

<hr class="article-divider">

<h2>完整搭建过程：从零开始</h2>

<div class="step-box">
  <h3><span class="step-number">1</span>安装 Obsidian 和 Digital Garden 插件</h3>
  <p>去 obsidian.md 下载安装，打开后在插件市场搜索"Digital Garden"安装。这一步很顺，10分钟搞定。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">2</span>注册 GitHub 和 Vercel 账号</h3>
  <p>GitHub 用来存储你的网站文件，Vercel 用来把文件变成可以访问的网站。两个都免费注册，用邮箱就行。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">3</span>在插件里完成三个配置</h3>
  <p>GitHub 用户名、仓库名、GitHub Token（在 GitHub 设置里生成）。配好之后插件就能把你的笔记推送到 GitHub 了。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">4</span>把 GitHub 仓库连接到 Vercel</h3>
  <p>在 Vercel 里导入你的 GitHub 仓库，选 Eleventy 框架，点部署。几分钟后你就有一个真实可访问的网址了。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">5</span>发布第一篇笔记</h3>
  <p>在 Obsidian 里新建一个文件，顶部加上 <code>dg-publish: true</code> 和 <code>dg-home: true</code>（首页专用），然后用命令面板执行"Publish Active Note"，完成。</p>
</div>

<div class="tip-box">
  💡 <strong>小技巧</strong>：在 Obsidian 根目录下建一个专门的文件夹（比如 my_garden）来存放要发布的内容，图片统一放在 my_garden/assets/ 里，不会把整个笔记库弄乱。
</div>

<hr class="article-divider">

<h2>我踩过的三个坑，帮你省掉</h2>

<h3>坑一：导航链接路径搞错了</h3>
<p>Digital Garden 发布后的 URL 格式是 <code>/my_garden/文件名</code>，不是 <code>/文件名</code>，也不是 <code>/notes/文件名</code>。我来回折腾了好久才搞清楚。方法是：先发布一篇文章，点击看实际 URL，然后按这个格式写导航链接。</p>

<h3>坑二：图片不显示</h3>
<p>图片要放在发布文件夹内（比如 my_garden/assets/），而且建议文件名用英文，中文文件名在 URL 里会被编码成乱码，容易出问题。</p>

<h3>坑三：文件发布了但页面显示"nothing here"</h3>
<p>检查 frontmatter 里的 <code>dg-publish: true</code> 是否正确，冒号后面要有空格，而且必须是小写的 true。写成 True 或者 TRUE 都不行。</p>

<div class="warn-box">
  ⚠️ <strong>注意</strong>：中文文件名可以用，但导航链接里要用 URL 编码，比较麻烦。建议导航页面（posts、about、projects）用英文命名，普通文章用中文没问题。
</div>

<hr class="article-divider">

<h2>如果你也想试，从这里开始</h2>

<p><strong>第一步：</strong>今天下载安装 Obsidian，感受一下这个工具，不用管数字花园的事，先用它记两天笔记。</p>

<p><strong>第二步：</strong>注册 GitHub 账号，建一个名为 my_garden 的仓库，先放在那里不用动。</p>

<p><strong>第三步：</strong>安装 Digital Garden 插件，按插件说明页的 setup guide 一步步配置，遇到问题就截图问 AI。</p>

<div class="article-highlight">
  本周挑战：把你的第一篇笔记发布出去，哪怕只有一句话也算。网址有了，后面的内容可以慢慢填。
</div>

<p>我从零开始到网站上线大概花了两天时间，中间遇到了不少问题，但每一个都解决了。你也可以。</p>

<p>你现在看到的这个数字花园，就是最好的证明。</p>

<!-- CTA -->
<div class="article-cta">
  <h3>每周更多这样的探索</h3>
  <p>关注我的微信公众号，获取非程序员视角的 AI 工具和效率分享</p>
  
  <div style="display: flex; flex-direction: column; align-items: center; gap: 1.5rem; margin-top: 1.5rem;">
    <div style="text-align: center;">
      <p style="margin: 0 0 0.8rem; font-size: 0.95rem; color: #ccc; font-weight: 500;">📱 我不是程序员，没有计算机背景</p>
      <p style="margin: 0; font-size: 0.85rem; color: #aaa; max-width: 500px;">只是一个对科技充满好奇的普通人，在这里分享我的学习历程和实战经验</p>
    </div>
    <div style="display: flex; flex-direction: column; align-items: center; gap: 1rem;">
      <img src="/my_garden/assets/公众号二维码AI小白马.png" alt="AI小白马微信公众号二维码" style="width: 160px; height: 160px; border-radius: 8px; box-shadow: 0 4px 12px rgba(0,0,0,0.2);">
      <p style="margin: 0; font-size: 0.8rem; color: #999;">扫码关注，每周获取最新内容</p>
    </div>
  </div>
</div>

<br>
<a class="article-back" href="/my_garden/posts">← 返回文章列表</a>

</div>
