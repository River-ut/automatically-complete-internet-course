# 融优学堂自动刷课脚本-可切换多门课程版-适应列表中所有学校（USTB-RongYouXueTang-计2508 WuYu River-Automation-script）
> 仅供学习交流使用

## 前言
* 首先要感谢大佬UltramarineW的开源代码https://github.com/UltramarineW
* 以及学长study-233 Andy Tao的开源代码https://github.com/study-233/USTB-RongYouXueTang-Automation-Script
* 可以实现全自动刷课程内的视频与全、半自动切换用户页面内的自选的多门课程
* 本人在其基础上解决了对于选了多门课程，但先前代码只能自动刷完一门课程就结束的问题。
* 解决了网页跳出广告或加载较慢导致脚本超时崩溃的问题
* 如果要适配其他学校，可自行修改代码里的学校代码，代码中罗列了学校和对应的代码

## Feature (功能特点)
* **学号登录**：适配需要学号登录的用户。
* **验证码识别**：自动识别登录页面的验证码。
* **自动刷课**：自动识别未完成课程并开始学习。
* **跳过测试**：自动跳过单元测试和非视频章节。
* **切换课程**：自动尝试切换课程
* **代码健壮**：1，若自动切换课程失败，可以通过重新启动脚本，在脚本切回主页面后，30秒内点击右上角头像里的我的课程（该过程根据课程数偶尔需要在返回主页面后再点击一次头像下的”我的课程”,请记住，只要程序停留在主页面，就去点我的课程，终端上也会给是否成功进入我的课程页面的反馈，可自行比对），辅助代码找到下一门课。2，打开网页后，若存在广告或网页加载较慢等问题，代码可自动等待两分钟再运行。

## Usage (使用说明)

1. **安装环境**：
   因为使用了 selenium 库中的 Edge Driver，所以需要安装 Edge 浏览器，并从 [Microsoft 官网](https://developer.microsoft.com/zh-cn/microsoft-edge/tools/webdriver/) 下载对应版本的 WebDriver。下载完后解压，将 `msedgedriver.exe` 放到 Python 解释器的根目录下。

2. **安装依赖库**：
   在终端（Terminal）运行以下命令安装必要的 Python 扩展包：
   ```bash
   git clone https://github.com/River-ut/USTB-RongYouXueTang-2508-WuYu-River-Automation-script.git
   cd USTB-RongYouXueTang-2508-WuYu-River-Automation-script
   pip install tqdm selenium ddddocr
3.编辑main.py 更改其中的username、password、school_code
4.
*方案一
在terminal中运行脚本：输入命令：python main.py
*方案二
直接将main.py中的代码复制粘贴到VScode或者PyCharm上运行。
   
