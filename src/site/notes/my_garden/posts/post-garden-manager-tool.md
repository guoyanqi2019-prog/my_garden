---
{"dg-publish":true,"permalink":"/my_garden/posts/post-garden-manager-tool/","title":"我用 AI 做了一个数字花园管理工具","tags":["效率工具","Obsidian","OpenCode"]}
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
.result-box { background: #f0fff4; border: 1px solid #9ae6b4; border-radius: 8px; padding: 1rem 1.5rem; margin: 1.5rem 0; font-size: 0.9rem; color: #276749; }
.article-back { font-size: 0.85rem; color: #C9922A; text-decoration: none; }
.article-back:hover { text-decoration: underline; }
</style>

<div class="article-wrap">

<a class="article-back" href="/my_garden/posts">← 返回文章列表</a>

<br><br>

<div class="article-tag">效率工具</div>

<h1>我用 AI 做了一个数字花园管理工具</h1>

<div class="article-meta">
  <span>作者：AI小白马</span>
  <span>2026年2月23日</span>
  <span>阅读约 6 分钟</span>
</div>

<p>我的数字花园里有十几篇文章。</p>

<p>每次发布新文章，我要手动更新首页精选、更新文章列表页面、检查格式是否统一、颜色有没有用错……这些事不难，但很繁琐。而且每次都要重复做。</p>

<p>我想：能不能有个工具，一键搞定这些事？</p>

<p>问题是，我不会写 GUI 程序。</p>

<div class="article-highlight">
  于是我让 OpenCode 帮我写。两小时后，我有了一个完整的图形界面管理工具。
</div>

<hr class="article-divider">

<h2>大多数人对自己做工具这件事的理解是错的</h2>

<p>很多人觉得，做个管理工具，要么用现成的软件，要么找程序员帮忙。自己动手？想都不敢想。</p>

<p>我以前也这么想。但这次经历让我发现，这个认知已经过时了。</p>

<h3>错误认知一：做工具需要先学编程</h3>
<p>不需要。我全程用中文跟 OpenCode 说我想要什么功能、界面长什么样、点击按钮之后发生什么。它来写代码，我只负责描述需求和测试结果。</p>

<h3>错误认知二：小工具不值得花时间做</h3>
<p>恰恰相反，越是重复性高的小事，越值得自动化。我算了一笔账：每次发布文章花 15 分钟做这些杂事，一年写 50 篇就是 12.5 小时。花 2 小时做一个工具，一年省下 10 小时，而且以后每次点击都是 0 秒。</p>

<h3>错误认知三：AI 写的工具会很简陋</h3>
<p>我做出来的工具有一个完整的 GUI 界面：左侧文章列表、右侧功能 Tab、深色主题、金色品牌色、状态卡片、日志输出……这不是玩具，是我真正在用的生产工具。</p>

<hr class="article-divider">

<h2>这个工具帮我解决了什么问题</h2>

<h3>一键更新首页和文章列表</h3>
<p>以前发布新文章，我要打开首页 Markdown 文件、复制粘贴新文章链接、更新日期……现在点击一个按钮，自动扫描所有已发布文章、更新首页精选、按分类生成文章列表页面。</p>

<h3>批量检查和修复文章格式</h3>
<p>我的文章风格统一用金色 #C9922A，但早期有些文章用的是旧红色。以前要一个个打开检查，现在工具自动扫描、自动替换。还能补全缺失的 CSS 样式、订阅表单、返回按钮。</p>

<h3>可视化查看文章状态</h3>
<p>左侧列表显示所有文章，选中一篇就能看到：标题、日期、分类、发布状态、格式检查结果。哪篇文章缺表单、哪篇颜色没改对，一目了然。</p>

<h3>直接生成 PDF 指南</h3>
<p>我之前有个 PDF 模板脚本，要改代码才能用。现在这个功能也整合进来了，填表单就能生成，不用碰代码。</p>

<hr class="article-divider">

<h2>我是怎么做到的：完整过程</h2>

<div class="step-box">
  <h3><span class="step-number">1</span>从最小的需求开始</h3>
  <p>我没有一开始就想做一个"完整的工具"。我先解决最痛的那个点——更新页面。我跟 OpenCode 说："帮我写一个脚本，扫描 posts 文件夹里所有已发布的文章，更新首页精选和 posts 页面。" 它给出了第一个版本的 update_pages.py。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">2</span>遇到新需求就加新功能</h3>
  <p>用了一段时间，我发现每次还要手动检查文章格式。于是我说："再加一个脚本，批量检查和修复文章格式问题。" 有了第二个版本。然后又发现每次都要打开命令行，很麻烦，于是我说："能不能做一个 GUI 界面？"</p>
</div>

<div class="step-box">
  <h3><span class="step-number">3</span>描述清楚你想要的界面</h3>
  <p>我做 GUI 的时候，直接把想要的效果描述出来："左侧是文章列表，右侧是功能 Tab，深色背景，金色品牌色，有三个 Tab：更新页面、统一格式、文章详情。" OpenCode 把这些描述变成了真实的界面代码。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">4</span>整理文件结构</h3>
  <p>工具做出来之后，我让 OpenCode 帮我把所有程序文件整理到 tools 文件夹，更新路径引用，删除冗余文件。最后还写了一份完整的使用文档和更新记录。</p>
</div>

<div class="result-box">
  ✅ <strong>最终成果</strong>：一个 500+ 行的 GUI 管理工具，包含更新页面、统一格式、文章详情、PDF 生成四个功能模块，还有完整的文档和更新日志。
</div>

<div class="tip-box">
  💡 <strong>小技巧</strong>：不要一上来就想做一个"完美的工具"。先解决最痛的那个问题，用起来，然后慢慢加功能。我的工具是从一个 50 行的脚本长出来的。
</div>

<div class="warn-box">
  ⚠️ <strong>注意</strong>：AI 写的代码第一次运行很可能报错。不要慌，把报错信息复制给它，它会自己修。我的 GUI 第一版就有一堆路径错误，来回修了三次才跑通。
</div>

<hr class="article-divider">

<h2>如果你也想试，从这里开始</h2>

<p><strong>第一步：</strong>找到你每天都在重复做的那件事。可能是整理文件、更新表格、发送提醒邮件——任何你觉得"这事应该能自动化"的事。</p>

<p><strong>第二步：</strong>用自然语言描述你想要什么。不需要技术术语，就像跟人说话一样："我想做一个工具，能自动扫描某个文件夹，生成一个列表。"</p>

<p><strong>第三步：</strong>跑起来就先用，别追求完美。功能简单没关系，先解决一个具体问题。用着用着你会发现新的需求，再加功能。</p>

<div class="article-highlight">
  本周挑战：找出你工作中一件重复性高的事，让 AI 帮你写一个工具来自动化它。哪怕只是一个简单的脚本，也比永远手动执行强。
</div>

<p>做完这个工具之后，我最大的感受不是"我也能写程序了"。</p>

<p>而是——原来我日常工作中那些觉得"本来就该这样"的繁琐流程，很多都是可以改变的。只是以前我不知道怎么改，现在我知道了。</p>

<div class="article-highlight">
  工具的意义不是炫技，而是把时间还给真正重要的事。
</div>

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
