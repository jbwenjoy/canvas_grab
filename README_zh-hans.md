# canvas-grab

将Canvas课程系统上的所有文件抓取到本地目录！

## 入门指南

如果你希望享受直接运行源代码的快感，可以 [在这里](https://github.com/skyzh/canvas_grab/archive/master.zip) 下载最新版本源代码，并按照 “构建并从源代码运行” 章节进行。

或者，你也可以直接 [在这里](https://github.com/skyzh/canvas_grab/releases) 下载构建好的二进制包，有能双击打开的 `canvas_grab(.exe)` 文件哦！

本程序将会在首次启动时提示输入一个API密钥，API密钥可以通过Canvas的 “设置” 页面生成。通过修改 `config.toml` 文件还可以对程序进行自定义，想试试更多炫酷功能吗？去“配置”章节看看吧！

在下载过程中可以随时中断，程序在下次启动时会继续当前进度。

如果需要重新下载全部文件，可以删除检查点文件 `.checkpoint` 和文件下载目录 `files/`。

## 配置

`config.toml` 文件可以对canvas_grab程序进行配置，这是一个可以用任何一个文本编辑器打开的纯文本文件。
可以参考 `config.example.toml` 或 `config.example.zh-hans.toml`文件中的注释进行配置。

## 炫酷功能

- **支持所有使用Canvas系统的网站！** 只要配置正确的Canvas系统网址即可。
- **自动记录下载状态！** 只要资源没有发生更新，文件就不会被反复下载。
- **设置文件尺寸过滤和类型过滤！** 可以设置允许下载的最大文件尺寸，还能通过文件扩展名过滤不想要的文件。
- **自动重试！** 当网络连接出错时，程序会自动进行重试，它随时都会停下来！
- **自动归类！** 所有文件都会被自动保存至对应课程的目录。课程目录名还可以利用像 `{CANVAS_ID}-{NAME}` 这样的模板来自定义！

## 构建并从源代码运行

首先，请按照Python 3.7或更高版本。

对于 macOS 或 Linux 用户，运行：

```bash
pip3 install -r requirements.txt
./main.py
```

对于 Windows 用户，运行：
```powershell
pip install -r requirements.windows.txt
python main.py
```

## 常见问题

* **获取API密钥** 在Canvas系统中，依次找到“账户” - “设置” - “创建新访问许可证”.
* **交大人** 可直接通过[传送门](https://oc.sjtu.edu.cn/profile/settings#access_tokens_holder)生成访问令牌。
* **提示Ignored Course** 如果出现"Ignored Course"警告，表明canvas_grab无法访问此课程。可能是由于(1) 课程没有发布 (2) 课程在之前的学期。
* **提示An error occurred** 如果出现"An error occurred when processing this course"说明课程中没有任何文件。
* **提示File not available** 此文件可能位于未发布的章节，canvas_grab无法绕过平台的限制。
* **提示No module named 'canvasapi'** 请参考“构建并从源代码运行”章节进行构建或直接下载构建好的二进制包。

## 截图

![image](https://user-images.githubusercontent.com/4198311/76405828-b71b1780-63c3-11ea-9c9e-59d0fcaf1de1.png)

## [参与者](https://github.com/skyzh/canvas_grab/graphs/contributors)

[@skyzh](https://github.com/skyzh), 
[@danyang685](https://github.com/danyang685),
[@BugenZhao](https://github.com/BugenZhao)

## 许可证

MIT