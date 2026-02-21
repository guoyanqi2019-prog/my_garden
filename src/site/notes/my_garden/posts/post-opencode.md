---
{"dg-publish":true,"permalink":"/my_garden/posts/post-opencode/","title":"OpenCode 让我这个不会编程的人做出了什么","tags":["AI工具探索","OpenCode","Remotion"]}
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
.result-box { background: #f0fff4; border: 1px solid #9ae6b4; border-radius: 8px; padding: 1rem 1.5rem; margin: 1.5rem 0; font-size: 0.9rem; color: #276749; }
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

<div class="article-tag">AI 工具探索</div>

<h1>OpenCode 让我这个不会编程的人做出了什么</h1>

<div class="article-meta">
  <span>作者：AI小白马</span>
  <span>2026年2月21日</span>
  <span>阅读约 8 分钟</span>
</div>

<p>我不会写代码。</p>

<p>但我用 OpenCode，做出了一个可以根据台词自动生成视频的工具。它能分析关键词、自动从网上搜图、配背景音乐、最后输出一个真实可播放的 MP4 文件。</p>

<p>整个过程我没有手写一行代码。</p>

<div class="article-highlight">
  AI 编程工具真正改变的不是"谁能写代码"，而是"谁能把想法变成现实"。
</div>

<hr class="article-divider">

<h2>大多数人对 AI 编程工具的理解是错的</h2>

<p>一提到 AI 编程工具，大多数人的第一反应是：这是给程序员用的，帮他们写代码更快。</p>

<p>我以前也这么想。但实际用下来，发现这个理解完全偏了。</p>

<h3>错误认知一：你需要先懂代码，才能用 AI 编程工具</h3>
<p>不需要。OpenCode 在终端里运行，你用中文描述你想要什么，它来写代码、运行代码、出了错误它自己修复、再运行。整个过程你只需要说人话，它负责翻译成机器能懂的语言。</p>

<h3>错误认知二：AI 写的代码会出很多错，需要你来改</h3>
<p>出错是正常的，但不需要你来改。这正是 OpenCode 最强的地方——它不只是生成代码，它会读报错信息、分析问题、修改代码、重新运行，这个循环它自己来转，不用你参与。我遇到过 Remotion 版本不匹配、音频文件格式错误、视频后半段黑屏等问题，每次都是 OpenCode 自己找到原因、自己修好的。</p>

<h3>错误认知三：没有编程基础做出来的东西很简单</h3>
<p>我最终做出来的是一个完整的自动化视频生成系统：输入一段台词，它自动分析关键词、调用 Pexels API 下载相关图片、准备背景音乐、通过 Remotion 渲染出视频。这不是一个玩具，是一个真实可用的工具。</p>

<hr class="article-divider">

<h2>做出这些东西之后，我发现了什么</h2>

<h3>做 PPT 视频这件事变了</h3>
<p>我第一个用 OpenCode 做的项目，是把"传统 PPT 制作流程"做成一个38秒的快闪视频——开场、场景切换、计时动画、结尾，全部自动生成。以前做这种视频要用剪辑软件一帧一帧调，现在写个脚本跑一下就出来了。</p>

<h3>遇到问题不再是终点</h3>
<p>以前我遇到任何技术问题，基本上就是搜索、看不懂、放弃。现在遇到报错，我直接把错误贴给 OpenCode，它会分析原因、给出修复方案、修改代码、验证结果。我踩过的坑——Remotion 版本不匹配、音频文件只有24字节无法解析、视频后半段黑屏——每一个 OpenCode 都帮我修好了，而且每次修完都留下了详细的说明文档。</p>

<h3>想法和现实之间的距离变短了</h3>
<p>以前我有个想法，能不能做到完全是另一回事，因为我不会编程。现在我有个想法，最多花几个小时，就能有一个可以运行的版本出来。这种感觉很难描述——就像突然多了一双手。</p>

<hr class="article-divider">

<h2>我是怎么做到的：完整过程</h2>

<div class="step-box">
  <h3><span class="step-number">1</span>用中文描述想要做什么</h3>
  <p>不需要用技术语言，就像跟人说话一样。比如："我想做一个工具，输入一段台词，自动生成视频，视频里要有相关图片和背景音乐。" OpenCode 会把这个需求拆解成可执行的技术方案。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">2</span>让它选技术方案</h3>
  <p>我不懂用什么工具，OpenCode 帮我选。它选了 Python 写主逻辑、Remotion 做视频渲染、Pexels API 搜图。我只需要知道"它能做这件事"，不需要知道"为什么用这个"。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">3</span>跟着它的步骤走，遇到报错就反馈</h3>
  <p>它生成代码之后，我负责运行、把报错复制给它。它看到报错自己分析修复，再让我运行，循环几次就通了。整个过程我是"执行者"，它是"决策者"。</p>
</div>

<div class="step-box">
  <h3><span class="step-number">4</span>收到结果，验证效果</h3>
  <p>最终我得到了三个视频：传统PPT制作流程的快闪版、科技感动画版、手绘涂鸦版。还有一套完整的自动化脚本，以后换个台词就能生成新视频。</p>
</div>

<div class="result-box">
  ✅ <strong>最终成果</strong>：一个完整的自动视频生成系统，支持自定义台词、自动下载图片、配置背景音乐、输出 MP4，全程不需要手写任何代码。
</div>

<div class="tip-box">
  💡 <strong>小技巧</strong>：遇到报错不要慌，直接把完整的错误信息复制给 OpenCode，它比你更知道怎么修。我遇到过"Remotion 版本不匹配"这种连问题在哪都不知道的错误，OpenCode 三步就修好了。
</div>

<div class="warn-box">
  ⚠️ <strong>注意</strong>：OpenCode 做出来的第一个版本不一定完美，我的视频就出现过后半段全黑的问题。但这不是终点，继续告诉它问题在哪，它会继续修。
</div>

<hr class="article-divider">

<h2>如果你也想试，从这里开始</h2>

<p><strong>第一步：</strong>装好 OpenCode，打开一个终端，用中文描述你想做的第一件小事。不要想太大，从一个具体的、你真的想要的东西开始。</p>

<p><strong>第二步：</strong>跟着它的步骤走，每一步它都会告诉你下一步做什么。出了报错就把错误信息粘贴给它，不要自己猜。</p>

<p><strong>第三步：</strong>把整个过程记录下来。每一个报错、每一个修复、每一个最终跑通的结果——这些记录本身就是最好的内容，也是你最真实的学习轨迹。</p>

<div class="article-highlight">
  本周挑战：用 OpenCode 做一件你一直想做但以为自己做不到的事。不管结果如何，把过程发出来。
</div>

<p>我做出第一个视频的时候，盯着那个 MP4 文件看了很久。</p>

<p>不是因为视频有多好看，而是因为三个月前我根本不相信自己能做出这种东西。</p>

<div class="article-cta">
  <h3>每周更多这样的探索</h3>
  <p>关注我的微信公众号，获取非程序员视角的 AI 工具和效率分享</p>
  
  <div style="display: flex; flex-direction: column; align-items: center; gap: 1.5rem; margin-top: 1.5rem;">
    <div style="text-align: center;">
      <p style="margin: 0 0 0.8rem; font-size: 0.95rem; color: #ccc; font-weight: 500;">📱 我不是程序员，没有计算机背景</p>
      <p style="margin: 0; font-size: 0.85rem; color: #aaa; max-width: 500px;">只是一个对科技充满好奇的普通人，在这里分享我的学习历程和实战经验</p>
    </div>
    <div style="display: flex; flex-direction: column; align-items: center; gap: 1rem;">
      <img src="https://raw.githubusercontent.com/guoyanqi2019-prog/my_garden/main/src/site/img/ai-xiaobaima-qrcode.png" alt="AI小白马微信公众号二维码" style="max-width: 200px; height: auto; border-radius: 8px; box-shadow: 0 4px 12px rgba(0,0,0,0.2);">
      <p style="margin: 0; font-size: 0.8rem; color: #999;">扫码关注，每周获取最新内容</p>
    </div>
  </div>
</div>

<br>
<a class="article-back" href="/my_garden/posts">← 返回文章列表</a>

</div>
