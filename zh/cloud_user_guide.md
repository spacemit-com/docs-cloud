# 进迭云平台使用指南

```
最新版本：2025/12/05
```

## 1. 注册 & 登录

访问浏览器网址：[https://gdriscv.com](https://gdriscv.com)
点击 **“立刻注册”** 按钮进入注册页面。

### 手机号注册

（图片）

### 邮箱注册

（图片）

### 登录

注册成功后点击 **“立即登录”**，进入登录页面，支持 **短信登录** 与 **密码登录**。
（图片）

成功登录后进入系统主界面：
（图片）

## 2. 申请新实例

在系统主界面点击 **“申请实例”** 进入实例创建页面。
（图片）

### 2.1 实例类型

系统支持多种方式创建实例，包括不同的操作系统镜像、快应用模板以及 RISC-V 算力集群等。

#### 基于操作系统的镜像

包含：

* Bianbu
* Deepin
* OpenHarmony
* openKylin

（图片）

#### 基于快应用模板的实例

包含：

- 通义 Qwen 大模型
- Deepseek 大模型
- 在线 Python 开发环境 JupyterLab

（图片）

#### 基于 RISC-V 算力融合集群的实例

（图片）

### 2.2 实例名称

输入自定义实例名称，并勾选同意隐私协议。
（图片）

### 2.3 申请时长

（图片）

#### 非会员

可选：48 小时 / 7 天 / 1 个月

#### 会员与管理员

最长可选：3 个月

## 3. 远程实例

### 3.1 命令行访问

申请成功后，可在控制台查看当前账户拥有的实例：
（图片）

点击实例卡片查看实例详情及功能按钮。
（图片）

点击 **“开始远程”** 进入命令行界面：
（图片）

命令行界面支持：

- 多会话
- 分屏
  （图片）

点击右上角 **“退出”** 返回主界面。
（图片）

### 3.2 串口调试

在工作台点击 **“串口调试”** 按钮进入串口界面。
（图片）

### 3.3 文件操作

工作台左上角点击 **“文件”** 可打开文件树或文件管理器：
（图片）

在文件树中右键目录或文件，可执行：

- 上传
- 下载
- 刷新
- 新建文件/目录

（图片）

双击文件（例如 `.profile`）可在线编辑：
（图片）

修改完成后点击右上角 **“保存”**。
（图片）

### 3.4 远程桌面

在工作台顶部点击 **“远程桌面”** 开启或关闭远程桌面模式。
若按钮为禁用状态，请先切回 Terminal 或串口界面。
（图片）

远程桌面支持：

- 尺寸调整
- 全屏模式

### 3.5 实例重启

点击顶部控制按钮，可选择：

- 电源重启
- 系统重启
  （图片）

### 3.6 实例刷机

点击顶部 **“刷机”** 按钮，打开刷机面板，从镜像列表选择镜像并点击 **“烧写”**：
（图片）

### 3.7 Code Server 应用

工作台顶部点击 **应用 → code-server**：

- 打开：启动在线 IDE
- 关闭：停止 Code Server

（图片）

#### Python 插件安装

在左侧扩展中搜索 `python` 即可安装插件：
（图片）

安装完成后可进行 Python 开发：
（图片）

### 3.8 JupyterLab 应用

应用 → JupyterLab：

* 打开：进入 JupyterLab
* 关闭：退出 JupyterLab

此应用仅在快应用模板中的 JupyterLab 实例支持。
（图片）

### 3.9 通义 Qwen 大模型应用

应用 → qwen-ai：

* 打开：进入 Qwen 应用
* 关闭：退出 Qwen

也可使用右侧 AI 按钮操作。
（图片）

### 3.10 Deepseek 大模型应用

应用 → deepseek-ai：

* 打开：进入 Deepseek 应用
* 关闭：退出 Deepseek

同样支持右侧 AI 按钮。
（图片）

## 4. 账户管理

在系统页面右上角点击用户图标进入账户管理：
（图片）

### 4.1 修改个人信息

在账户设置页面点击 **“编辑个人信息”**：
（图片）

可修改：

* 用户名
* 密码
* 手机号
* 邮箱
  （图片）

保存后点击返回回到账户管理界面。

### 4.2 消息中心

查看系统消息。
（图片）

### 4.3 实例共享

可将个人实例共享给其他用户。
（图片）

### 4.4 API Key 管理

用于创建和管理 API Key，支持远程调用实例 API。
（图片）

### 4.5 告警信息

查看实例告警状态。
（图片）

## 5. 本地连接

### 5.1 SSH 直连

SSH 直连需启用 **TLS 隧道**，建议使用 Stunnel。

#### 客户端安装

* Windows: [https://www.stunnel.org/downloads/stunnel-latest-win64-installer.exe](https://www.stunnel.org/downloads/stunnel-latest-win64-installer.exe)
* Ubuntu/Debian:

  ```bash
  sudo apt install stunnel4
  ```
* CentOS/RHEL:

  ```bash
  sudo yum install stunnel
  ```

#### 获取 Stunnel 配置

进入实例卡片 → 本地连接
（图片）

将配置复制到 Stunnel 配置文件并启动：
（图片）

Linux 可直接通过命令启动：
（图片）

#### SSH 连接方式

命令行连接：

```bash
ssh -p 2222 root@localhost
```

（图片）

使用 MobaXterm：

* 协议需设置为 SSHv2
  （图片）

用户密码见连接信息页面末尾。
（图片）

### 5.2 VNC 直连

与 SSH 一样需配置 Stunnel。

在 MobaXterm 中新建 VNC Session：

* 地址：`localhost`
* 端口：`5901`
  （图片）

密码同 SSH 部分说明。

---

## 6. API 调用

### 6.1 Ollama 接口调用

仅支持：

* 通义 Qwen 大模型实例
* Deepseek 大模型实例

进入实例工作台 → 右侧点击 **API 调用**：
（图片）

设置请求头后，可通过给定 URL 调用 Ollama 接口：
（图片）

### 6.2 自定义接口调用

实例支持通过端口 `18080` 部署并访问自定义服务。

示例：运行 Python HTTP 服务：
（图片）

Postman 调用示例（deviceId 为实例设备 ID）：
（图片）

API Key 可从账户管理中获取：
（图片）

请求地址格式：

```
https://gdriscv.com/api/remote/{deviceId}
```

（图片）

## 7. 开发示例

### 7.1 RISC-V 汇编开发

#### RVV 编程

RVV（RISC-V Vector）扩展用于高性能向量计算，与 ARM NEON 存在差异：
（图片）

核心代码示例：
（图片）

在云实例中通过 Code Server 编辑代码：
（图片）

通过 gcc 编译与运行：
（图片）

#### RISC-V AI 指令编程

K1 为 8 核 RISC-V AI CPU，特点：

* 50 KDMIPS
* 2.0 TOPS AI 算力
* 支持 RVV 1.0，256-bit SIMD
  （图片）

核心代码示例：
（图片）

通过 Code Server 编辑并编译：
（图片）

运行结果：
（图片）

#### 卷积优化示例

说明卷积神经网络（CNN）的应用背景与优化方式，并给出 1×3 卷积核心代码示例：
（图片）

在云实例中编辑：
（图片）

运行结果：
（图片）

## 7.2 AI 开发

### YOLOv8 姿态识别

YOLOv8-pose 用于人体姿态估计，适用于动作识别、运动分析等场景。

#### 下载代码

```bash
git clone https://gitee.com/bianbu/spacemit-demo.git
```

#### 下载模型

```bash
cd spacemit-demo/examples/CV/yolov8-pose/model
sh download_model.sh
```

脚本会下载：

* FP32: `yolov8n-pose.onnx`
* INT8: `yolov8n-pose.q.onnx`

#### 创建环境并安装依赖

```bash
python3 -m venv <env>
source <env>/bin/activate
pip install -r requirements.txt --index-url https://git.spacemit.com/api/v4/projects/33/packages/pypi/simple
```

#### 编辑代码

（图片）

#### 运行

```bash
python test_yolov8_pose.py
```

（图片）


### YOLOv5-face 人脸检测

操作方式与 YOLOv8-pose 类似。

#### 下载示例代码与模型

```bash
git clone https://gitee.com/bianbu/spacemit-demo.git
cd spacemit-demo/examples/CV/yolov5-face/model
sh download_model.sh
```

#### 创建环境并安装依赖

（同上）

#### 编辑与运行

（图片）

### 7.3 OCR 识别

基于 K1 RISC-V 优化的 OpenCV OCR 示例。

#### 下载示例代码

```bash
git clone https://gitee.com/bianbu/spacemit-demo.git
```

#### 下载模型

```bash
cd spacemit-demo/examples/CV/ocr/model
sh download_model.sh
```

（内容后续同结构）


