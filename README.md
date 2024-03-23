<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">车辆检测、跟踪和计数</font></font></h1><a id="user-content-vehicle-detection-tracking-and-counting" class="anchor" aria-label="永久链接：车辆检测、跟踪和计数" href="#vehicle-detection-tracking-and-counting"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最后页面更新：</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">12/04/2017</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（添加了 Python API 和 OpenCV 3.x 支持）</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最新版本：</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1.0.0</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（有关更多信息，请参阅发行说明）</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">大家好，</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有多种方法可以执行车辆检测、跟踪和计数。</font><font style="vertical-align: inherit;">以下是执行此操作的最简单方法的分步：</font></font></p>
<ol dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">首先，您需要检测移动物体。</font><font style="vertical-align: inherit;">进行车辆检测的一种简单方法是使用背景扣除 (BS) 算法。</font><font style="vertical-align: inherit;">您可以尝试使用背景扣除库，例如</font></font><a href="https://github.com/andrewssobral/bgslibrary#bgslibrary"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">BGSLibrary</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于车辆跟踪，您需要使用跟踪算法。</font><font style="vertical-align: inherit;">最简单的方法是使用 blob 跟踪器算法（请参阅</font></font><a href="https://code.google.com/p/cvblob/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">cvBlob</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或</font></font><a href="http://opencvblobslib.github.io/opencvblobslib/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenCVBlobsLib</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">）。</font><font style="vertical-align: inherit;">因此，将前景蒙版发送到</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">cvBlob</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenCVBlobsLib</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font><font style="vertical-align: inherit;">例如，</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">cvBlob</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">库提供了一些方法来获取</font><font style="vertical-align: inherit;">移动物体的</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">质心</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">、</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">轨迹</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ID 。</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您还可以设置绘制</font><font style="vertical-align: inherit;">跟踪对象的</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">边界框</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">、</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">质心</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">和</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">角度。</font></font></strong><font style="vertical-align: inherit;"></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">然后，检查移动物体的</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">质心</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是否穿过</font><font style="vertical-align: inherit;">视频中的</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">感兴趣区域（即虚拟线）。</font></font></strong><font style="vertical-align: inherit;"></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">瞧！</font><font style="vertical-align: inherit;">好好享受 ：）</font></font></li>
</ol>
<p align="center" dir="auto"><a target="_blank" rel="noopener noreferrer nofollow" href="https://raw.githubusercontent.com/andrewssobral/simple_vehicle_counting/master/doc/images/vehicle_counting_screen.png"><img src="https://raw.githubusercontent.com/andrewssobral/simple_vehicle_counting/master/doc/images/vehicle_counting_screen.png" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">引文</font></font></h2><a id="user-content-citation" class="anchor" aria-label="永久链接：引文" href="#citation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您在出版物中使用此代码，请将其引用为：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>@ONLINE{vdtc,
    author = "Andrews Sobral",
    title  = "Vehicle Detection, Tracking and Counting",
    year   = "2014",
    url    = "https://github.com/andrewssobral/simple_vehicle_counting"
}
</code></pre><div class="zeroclipboard-container">
   
  </div></div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于 Windows 用户</font></font></h2><a id="user-content-for-windows-users" class="anchor" aria-label="永久链接：适用于 Windows 用户" href="#for-windows-users"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">不再有 Visual Studio 2013 模板项目。</font><font style="vertical-align: inherit;">请改用 CMAKE。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用 CMAKE 中的 OpenCV 3.x 和 Visual Studio 2015 进行编译</font></font></h4><a id="user-content-compiling-with-opencv-3x-and-visual-studio-2015-from-cmake" class="anchor" aria-label="永久链接：使用 CMAKE 的 OpenCV 3.x 和 Visual Studio 2015 进行编译" href="#compiling-with-opencv-3x-and-visual-studio-2015-from-cmake"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">依赖项：</font></font></strong></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenCV 3.x（使用 OpenCV 3.2.0 测试）</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">GIT（使用 git 版本 2.7.2.windows.1 进行测试）。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">适用于 Windows 的 CMAKE（使用 cmake 版本 3.1.1 进行测试）。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Microsoft Visual Studio（使用 VS2015 测试）。</font></font></li>
</ul>
<p dir="auto"><em><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：OpenCV 2.4.x 和 Visual Studio 2013 的过程类似。</font></font></em></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请按照以下说明操作：</font></font></p>
<ol dir="auto">
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">转到 Windows 控制台。</font></font></p>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">克隆 git 存储库：</font></font></p>
</li>
</ol>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>git clone --recursive https://github.com/andrewssobral/simple_vehicle_counting.git
</code></pre><div class="zeroclipboard-container">
    
  </div></div>
<ol start="3" dir="auto">
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">转到</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">simple_vehicle_counting/build</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件夹。</font></font></p>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">设置你的 OpenCV 路径：</font></font></p>
</li>
</ol>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>set OpenCV_DIR=C:\OpenCV3.2.0\build
</code></pre><div class="zeroclipboard-container">
    
  </div></div>
<ol start="5" dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启动CMAKE：</font></font></li>
</ol>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cmake -DOpenCV_DIR=%OpenCV_DIR% -G "Visual Studio 14 Win64" ..
</code></pre><div class="zeroclipboard-container">
    
  </div></div>
<ol start="6" dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在系统路径中包含 OpenCV 二进制文件：</font></font></li>
</ol>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>set PATH=%PATH%;%OpenCV_DIR%\x64\vc14\bin
</code></pre><div class="zeroclipboard-container">
    
  </div></div>
<ol start="7" dir="auto">
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在 Visual Studio 中</font><font style="vertical-align: inherit;">打开</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">bgs.sln文件并切换到</font></font></strong><font style="vertical-align: inherit;"></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">“RELEASE”</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模式</font></font></p>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">单击</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">“ALL_BUILD”</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">项目并构建！</font></font></p>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果一切顺利，将</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">simple_vehicle_counting.exe</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">复制到</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">simple_vehicle_counting/</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">并运行！</font></font></p>
</li>
</ol>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于Linux用户</font></font></h2><a id="user-content-for-linux-users" class="anchor" aria-label="永久链接：对于 Linux 用户" href="#for-linux-users"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于Linux和Mac用户，提供了CMakefile来编译源代码。</font></font></p>
</li>
<li>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">查看最新的项目源码并编译：</font></font></li>
</ul>
</li>
</ul>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>~/git clone --recursive https://github.com/andrewssobral/simple_vehicle_counting.git
~/cd simple_vehicle_counting
~/simple_vehicle_counting/cd build
~/simple_vehicle_counting/build/ cmake ..
~/simple_vehicle_counting/build/ make
</code></pre><div class="zeroclipboard-container">
    
  </div></div>
<ul dir="auto">
<li>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行演示：</font></font></li>
</ul>
</li>
</ul>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>~/simple_vehicle_counting/run_simple_vehicle_counting.sh
</code></pre><div class="zeroclipboard-container">
   
  </div></div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Docker镜像</font></font></h2><a id="user-content-docker-image" class="anchor" aria-label="永久链接：Docker 镜像" href="#docker-image"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Docker 镜像可在以下位置获取：</font></font></li>
<li>
<ul dir="auto">
<li><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Ubuntu 16.04 + VNC + OpenCV 2.4.13 + Python 2.7 + 车辆检测、跟踪和计数</font></font></strong>
<a href="https://hub.docker.com/r/andrewssobral/vehicle_detection_tracking_counting/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">https://hub.docker.com/r/andrewssobral/vehicle_detection_tracking_counting/</font></font></a></li>
</ul>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">示例代码</font></font></h2><a id="user-content-example-code" class="anchor" aria-label="固定链接：示例代码" href="#example-code"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-c++ notranslate position-relative overflow-auto" dir="auto"><pre>#<span class="pl-k">include</span> <span class="pl-s"><span class="pl-pds">&lt;</span>iostream<span class="pl-pds">&gt;</span></span>
#<span class="pl-k">include</span> <span class="pl-s"><span class="pl-pds">&lt;</span>opencv2/opencv.hpp<span class="pl-pds">&gt;</span></span>

#<span class="pl-k">include</span> <span class="pl-s"><span class="pl-pds">"</span>package_bgs/PBAS/PixelBasedAdaptiveSegmenter.h<span class="pl-pds">"</span></span>
#<span class="pl-k">include</span> <span class="pl-s"><span class="pl-pds">"</span>package_tracking/BlobTracking.h<span class="pl-pds">"</span></span>
#<span class="pl-k">include</span> <span class="pl-s"><span class="pl-pds">"</span>package_analysis/VehicleCouting.h<span class="pl-pds">"</span></span>

<span class="pl-k">int</span> <span class="pl-en">main</span>(<span class="pl-k">int</span> argc, <span class="pl-k">char</span> **argv)
{
  <span class="pl-c"><span class="pl-c">/*</span> Open video file <span class="pl-c">*/</span></span>
  CvCapture *capture = <span class="pl-c1">0</span>;
  capture = <span class="pl-c1">cvCaptureFromAVI</span>(<span class="pl-s"><span class="pl-pds">"</span>dataset/video.avi<span class="pl-pds">"</span></span>);
  <span class="pl-k">if</span>(!capture){
    std::cerr &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span>Cannot open video!<span class="pl-pds">"</span></span> &lt;&lt; std::endl;
    <span class="pl-k">return</span> <span class="pl-c1">1</span>;
  }

  <span class="pl-c"><span class="pl-c">/*</span> Background Subtraction Algorithm <span class="pl-c">*/</span></span>
  IBGS *bgs;
  bgs = <span class="pl-k">new</span> PixelBasedAdaptiveSegmenter;

  <span class="pl-c"><span class="pl-c">/*</span> Blob Tracking Algorithm <span class="pl-c">*/</span></span>
  cv::Mat img_blob;
  BlobTracking* blobTracking;
  blobTracking = <span class="pl-k">new</span> BlobTracking;

  <span class="pl-c"><span class="pl-c">/*</span> Vehicle Counting Algorithm <span class="pl-c">*/</span></span>
  VehicleCouting* vehicleCouting;
  vehicleCouting = <span class="pl-k">new</span> VehicleCouting;

  std::cout &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span>Press 'q' to quit...<span class="pl-pds">"</span></span> &lt;&lt; std::endl;
  <span class="pl-k">int</span> key = <span class="pl-c1">0</span>;
  IplImage *frame;
  <span class="pl-k">while</span>(key != <span class="pl-s"><span class="pl-pds">'</span>q<span class="pl-pds">'</span></span>)
  {
    frame = <span class="pl-c1">cvQueryFrame</span>(capture);
    <span class="pl-k">if</span>(!frame) <span class="pl-k">break</span>;

    cv::Mat img_input = <span class="pl-c1">cv::cvarrToMat</span>(frame);
    <span class="pl-c1">cv::imshow</span>(<span class="pl-s"><span class="pl-pds">"</span>Input<span class="pl-pds">"</span></span>, img_input);

    <span class="pl-c"><span class="pl-c">//</span> bgs-&gt;process(...) internally process and show the foreground mask image</span>
    cv::Mat img_mask;
    bgs-&gt;<span class="pl-c1">process</span>(img_input, img_mask);

    <span class="pl-k">if</span>(!img_mask.<span class="pl-c1">empty</span>())
    {
      <span class="pl-c"><span class="pl-c">//</span> Perform blob tracking</span>
      blobTracking-&gt;<span class="pl-c1">process</span>(img_input, img_mask, img_blob);

      <span class="pl-c"><span class="pl-c">//</span> Perform vehicle counting</span>
      vehicleCouting-&gt;<span class="pl-c1">setInput</span>(img_blob);
      vehicleCouting-&gt;<span class="pl-c1">setTracks</span>(blobTracking-&gt;<span class="pl-c1">getTracks</span>());
      vehicleCouting-&gt;<span class="pl-c1">process</span>();
    }

    key = <span class="pl-c1">cvWaitKey</span>(<span class="pl-c1">1</span>);
  }

  <span class="pl-k">delete</span> vehicleCouting;
  <span class="pl-k">delete</span> blobTracking;
  <span class="pl-k">delete</span> bgs;

  <span class="pl-c1">cvDestroyAllWindows</span>();
  <span class="pl-c1">cvReleaseCapture</span>(&amp;capture);

  <span class="pl-k">return</span> <span class="pl-c1">0</span>;
}</pre><div class="zeroclipboard-container">
    
  </div></div>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Python API</font></font></h2><a id="user-content-python-api" class="anchor" aria-label="永久链接：Python API" href="#python-api"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="/andrewssobral/simple_vehicle_counting/blob/master/python/demo.py"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Python 演示</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">展示</font><font style="vertical-align: inherit;">了如何调用 Python API。</font></font><a href="/andrewssobral/simple_vehicle_counting/blob/master/Demo.cpp"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">它与C++ 演示</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">类似</font><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要使用Python API，您应该复制</font></font><a href="/andrewssobral/simple_vehicle_counting/blob/master/python"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">“python”目录</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">以覆盖生成的目录。</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>~/simple_vehicle_counting/cd build
~/simple_vehicle_counting/build/cmake ..
~/simple_vehicle_counting/build/make -j 8
~/simple_vehicle_counting/build/cp -r ../python/* python/
~/simple_vehicle_counting/build/../run_python_demo.sh
</code></pre><div class="zeroclipboard-container">
    
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="/andrewssobral/simple_vehicle_counting/blob/master/python"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您之前在项目根目录下构建过项目，请确保“python”目录</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中</font><font style="vertical-align: inherit;">没有之前生成的库</font></font><code>make clean</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">发行说明：</font></font></h2><a id="user-content-release-notes" class="anchor" aria-label="永久链接： 发行说明：" href="#release-notes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2017 年 12 月 4 日：添加了 OpenCV 3.x 支持。</font><font style="vertical-align: inherit;">删除了 vs2013 模板项目（使用 CMAKE 代替）。</font></font></p>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">07/04/2017：添加了 Python API，感谢</font></font><a href="https://github.com/kyu-sz"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">@kyu-sz</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">版本 1.0.0：第一个版本。</font></font></p>
</li>
</ul>
</article></div>
