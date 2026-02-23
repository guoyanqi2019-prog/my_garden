---
{"dg-publish":true,"permalink":"/my_garden/posts/post-website-automation/","title":"我用一个晚上，把网站的自动化更新系统搭起来了","tags":["一人探索","真实记录","工具探索"]}
---


<style>
.article-wrap { max-width: 680px; margin: 0 auto; padding: 3rem 2rem; }
.article-tag { font-size: 0.8rem; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; color: #C9922A; margin-bottom: 1rem; }
.article-wrap h1 { font-size: 2rem; font-weight: 800; color: #111; line-height: 1.2; margin: 0 0 1rem; }
.article-meta { font-size: 0.85rem; color: #bbb; margin-bottom: 2.5rem; display: flex; gap: 1rem; flex-wrap: wrap; }
.article-wrap p { font-size: 1rem; color: #333; line-height: 1.9; margin-bottom: 1.5rem; }
.article-wrap h2 { font-size: 1.2rem; font-weight: 700; color: #111; margin: 2.5rem 0 1rem; }
.article-wrap h3 { font-size: 1rem; font-weight: 700; color: #333; margin: 1.5rem 0 0.5rem; }
.article-divider { border: none; border-top: 1px solid #eee; margin: 2.5rem 0; }
.article-highlight { background: #fdf8f0; border-left: 3px solid #C9922A; padding: 1rem 1.5rem; border-radius: 0 8px 8px 0; margin: 1.5rem 0; font-size: 0.95rem; color: #444; font-style: italic; }
.step-box { background: #f9f9f9; border-radius: 8px; padding: 1.5rem; margin: 1.5rem 0; }
.step-box h3 { margin: 0 0 0.5rem; color: #111; font-size: 0.95rem; }
.step-box p { margin: 0; font-size: 0.9rem; color: #555; line-height: 1.7; }
.step-number { display: inline-block; background: #C9922A; color: #fff; width: 24px; height: 24px; border-radius: 50%; font-size: 0.75rem; font-weight: 700; text-align: center; line-height: 24px; margin-right: 0.5rem; }
.tip-box { background: #fffaf0; border: 1px solid #fbd38d; border-radius: 8px; padding: 1rem 1.5rem; margin: 1.5rem 0; font-size: 0.9rem; color: #744210; }
.warn-box { background: #fff5f5; border: 1px solid #feb2b2; border-radius: 8px; padding: 1rem 1.5rem; margin: 1.5rem 0; font-size: 0.9rem; color: #742a2a; }
.article-back { font-size: 0.85rem; color: #C9922A; text-decoration: none; }
.article-back:hover { text-decoration: underline; }
</style>

<div class="article-wrap">

<a class="article-back" href="/my_garden/posts">← 返回文章列表</a>

<br><br>

<div class="article-tag">一人探索</div>

<h1>我用一个晚上，把网站的自动化更新系统搭起来了</h1>

<div class="article-meta">
  <span>作者：AI小白马</span>
  <span>2026年2月22日</span>
  <span>阅读约 6 分钟</span>
</div>

<p>晚上9点55分，我只是想解决一个小问题。</p>

<p>结果搞到深夜。</p>

<p>但我把一件以前完全不会做的事做成了。</p>

<hr class="article-divider">

<h2>从一个报错开始</h2>

<p>最开始的问题很简单：首页的精选文章，我每次写新文章都要手动去 HTML 里加一条链接。</p>

<p>这件事本身不难，但很烦。更烦的是，我不确定自己加的位置对不对。每次改完都要发布、等待、刷新，然后发现哪里又乱了。</p>

<p>我想要的很简单：<strong>写完文章，一键更新，不用手动改任何东西。</strong></p>

<hr class="article-divider">

<h2>第一个方案：Python 脚本</h2>

<p>我让 Claude 帮我写了一个 Python 脚本。逻辑不复杂：扫描 posts 文件夹里所有文章，读取标题、日期、描述，按 tag 分类，然后自动填入首页和 posts 页面。</p>

<p>脚本写好了，运行成功了。</p>

<p>然后我发现 posts 页面出现了<strong>三份重复内容</strong>。同样的文章列表，出现了三次。</p>

<p>原因是脚本用正则表达式匹配要替换的区域，但正则写得不够精准——每次运行，它找到了旧内容，把新内容追加进去，但没有删掉旧的。运行一次就多一份。</p>

<hr class="article-divider">

<h2>第二个方案：标记注释</h2>

<p>解决方法其实很简单，但我自己想不到——用两个 HTML 注释作为"锚点"：</p>

<div class="article-highlight">
  与其写聪明的代码，不如把问题定义清楚。
</div>

<p>脚本每次只替换这两个注释之间的内容，绝对不会影响外面的任何东西。运行十次，结果都一样干净。</p>

<hr class="article-divider">

<h2>然后是布局的连环问题</h2>

<p>脚本搞定了，但首页的文章卡片显示出了问题。我想要三列卡片，每张卡片有彩色背景、标题、描述。</p>

<p>Digital Garden 渲染出来的效果是：三张卡片竖着排成一列，彩色背景变成了独立的方块，文字飘在旁边。</p>

<p>原因是我用了 emoji 做图标，Digital Garden 对 emoji 的渲染支持有限，撑开了高度，破坏了 flex 布局。删掉 emoji，换成纯色块，还是竖排。换成纯文字列表，还是出问题——标题、描述、日期各自变成了独立的一行。</p>

<p>最后的解决方案是：<strong>放弃所有 CSS class，全部用内联样式。</strong> Digital Garden 没有办法拆分一行 HTML，只能原样渲染。问题解决了。</p>

<hr class="article-divider">

<h2>还有一个细节</h2>

<p>做完之后，我发现文章标题是黑色的，看不出来是链接。改成金色 <code>#C9922A</code>——和网站的整体配色一致。首页、posts 页面、"查看所有文章"按钮，全部统一。</p>

<div class="tip-box">
  💡 所有可点击的东西，用同一种颜色。让人一眼就知道能点。这是从 Dan Koe 网站里学来的。
</div>

<hr class="article-divider">

<h2>最后的工作流</h2>

<p>现在，每次我写完一篇新文章，只需要：</p>

<div class="step-box">
  <h3><span class="step-number">1</span>写文章</h3>
  <p>在 Obsidian 里写，frontmatter 里加上 dg-publish: true。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">2</span>双击更新页面.bat</h3>
  <p>自动扫描所有文章，更新首页精选和 posts 列表。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">3</span>在 Obsidian 点发布</h3>
  <p>三步，30秒，完成。</p>
</div>

<hr class="article-divider">

<h2>我学到了什么</h2>

<p>今晚最重要的不是那个脚本。</p>

<p><strong>我不是程序员，但我把一个程序员才会做的事做成了。</strong></p>

<p>不是因为我突然学会了编程。是因为我能清晰地描述我想要什么，然后和 AI 一起把它做出来。这个能力，比"会写代码"更值钱。因为它可以迁移到任何地方。</p>

<hr class="article-divider">

<p>如果你也有一个"想做但不知道怎么做"的小工具，不需要等自己学会编程。先把你想要的结果描述清楚，然后开始尝试。</p>

<p>最坏的情况是：失败了，但你搞清楚了问题在哪。最好的情况是：一个晚上，搞定了。</p>

<br>
<div style="display:flex;align-items:center;gap:40px;flex-wrap:wrap;margin:20px 0;">
<div style="flex:1;min-width:260px;text-align:center;">
<img src="https://raw.githubusercontent.com/guoyanqi2019-prog/my_garden/main/src/site/img/ai-xiaobaima-profile.png" alt="AI小白马" style="max-width:300px;width:100%;border-radius:12px;" />
</div>
<div style="flex:1;min-width:260px;">
<script src="https://f.convertkit.com/ckjs/ck.5.js"></script>
<form action="https://app.kit.com/forms/9117923/subscriptions" style="background-color:rgb(255,255,255);border-radius:6px;" class="seva-form formkit-form" method="post" data-sv-form="9117923" data-uid="3b70cc7e59" data-format="inline" data-version="5" min-width="400 500 600 700 800"><div data-style="full"><div data-element="column" class="formkit-column"><div class="formkit-header" style="color:rgb(83,83,83);font-size:24px;font-weight:700;" data-element="header"><h2>加入我的<br>AI 学习成长日志</h2></div><ul class="formkit-alert formkit-alert-error" data-element="errors" data-group="alert"></ul><div data-element="fields" class="seva-fields formkit-fields"><div class="formkit-field"><input class="formkit-input" name="email_address" style="color:rgb(139,139,139);border-color:rgb(221,224,228);font-weight:400;" aria-label="Email Address" placeholder="Email Address" required="" type="email"></div><button data-element="submit" class="formkit-submit" style="color:rgb(255,255,255);background-color:rgb(201,146,42);border-radius:3px;font-weight:700;"><div class="formkit-spinner"><div></div><div></div><div></div></div><span>获取免费PDF文档及资源包</span></button></div><div class="formkit-disclaimer" style="color:rgb(139,139,139);font-size:13px;" data-element="disclaimer"><p><strong>每周更新，我的实战与学习经验，陪你成长</strong></p></div></div></div></form>
</div>
</div>

<br>
<a class="article-back" href="/my_garden/posts">← 返回文章列表</a>

</div>
