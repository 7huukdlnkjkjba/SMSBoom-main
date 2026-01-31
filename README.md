# SMSBoom - 终极短信测试神器

> **全球领先的短信接口测试工具**  
> **最强大的短信发送能力测试系统**-- English  
> **终极短信测试神器**-- Simplified Chinese  
> **無敵のSMSテストツール** -- Japanese

![test](img/test2.gif)

## 免责声明

1. 使用此程序请遵守当地的法律法规，禁止滥用、恶意使用，**触犯法律所造成的问题均由使用者承担**。  
2. 本程序仅供娱乐,源码全部开源,**禁止滥用** 和二次 **禁止用于商业用途**.

## Repair - TODO

1. 修改文档
2. 修缮主要功能
3. 修缮后端使用 FastAPI 前端使用 vue3 elementUI
4. GUI 使用 web 技术

## Feature

1. 通过自定义 `api.json` 的方式定义接口.  
2. 支持关键字替换. **时间戳** `[timestamp]` **手机号** `[phone]`  
3. 多线程/异步 请求.  
4. 通过 Flask 提供网页测试/添加接口.  
5. 友好的命令行参数支持.  
6. 采用方便的 pipenv 包管理.  
7. 通过代理调用短信接口, 支持 http, socks4, socks5代理.
8. 使用随机的 User-Agent.
9. 可指定轰炸次数, 轰炸间隔时间.

## Quick Start

### 适用于大神


## SMSBoom 简易使用指南

### 🚀 超简单三步上手

#### 1. 安装依赖
打开命令提示符（Win+R 输入 cmd），复制粘贴以下命令：
```bash
cd c:\Users\Administrator\Downloads\Compressed\SMSBoom-main && pip install -r requirements.txt
```

#### 2. 更新接口
```bash
python smsboom.py update
```

#### 3. 开始使用
**最简单的命令**（复制粘贴后修改手机号）：
```bash
python smsboom.py run -p 13812345678
```

### 🎯 常用命令速查

| 功能 | 命令 |
|------|------|
| 基础测试 | `python smsboom.py run -p 手机号` |
| 加强版 | `python smsboom.py run -t 64 -p 手机号 -f 10` |
| 终极版 | `python smsboom.py run -t 64 -p 手机号 -f 30 -i 20 -e` |

### 💡 命令解释

- `-t 64`：使用64个线程（速度更快）
- `-p 手机号`：要测试的手机号码
- `-f 30`：循环测试30次
- `-i 20`：每次间隔20秒
- `-e`：使用代理（更稳定）

## SMSBoom - 终极短信测试工具使用指南

### 🚀 项目简介

SMSBoom是一款功能强大的短信接口测试工具，采用最新的异步IO技术，支持百万级并发请求，能够快速测试短信接口的可靠性和稳定性。

### 📦 安装步骤

1. **下载项目**
   ```shell
   git clone https://github.com/AdminWhaleFall/SMSBoom.git/
   ```

2. **安装依赖**
   ```shell
   # 方法一：使用pipenv
   pip install pipenv
   pipenv install
   
   # 方法二：直接安装
   pip install -r requirements.txt
   ```

3. **更新接口**
   ```shell
   python smsboom.py update
   ```

### 💣 使用方法

#### 基本命令格式
```shell
python smsboom.py run -t <线程数> -p <手机号> -f <执行次数> -i <间隔时间> -e
```

#### 常用命令示例

1. **单波测试**：启动64个线程，测试一个手机号
   ```shell
   python smsboom.py run -t 64 -p 198xxxxxxxxx
   ```

2. **循环测试**：启动64个线程，循环测试60次
   ```shell
   python smsboom.py run -t 64 -p 198xxxxxxxxx -f 60
   ```

3. **定时循环**：启动64个线程，循环测试60次，每次间隔30秒
   ```shell
   python smsboom.py run -t 64 -p 198xxxxxxxxx -f 60 -i 30
   ```

4. **使用代理**：启动64个线程，使用代理进行测试
   ```shell
   python smsboom.py run -t 64 -p 198xxxxxxxxx -f 60 -i 30 -e
   ```

5. **多目标测试**：同时测试多个手机号
   ```shell
   python smsboom.py run -t 64 -p 138xxxxxxxx -p 139xxxxxxxx -f 60 -i 30 -e
   ```

### 🔧 核心功能

1. **多线程/异步请求**：采用多线程和异步IO技术，支持高并发请求
2. **灵活的接口配置**：通过api.json配置接口，可根据需要添加和更新
3. **代理支持**：支持HTTP、SOCKS4、SOCKS5代理，提高测试稳定性
4. **多模式测试**：支持单线程、多线程、异步三种测试模式
5. **参数化配置**：可自定义线程数、执行次数、间隔时间等参数

### 📊 性能参数

- **并发能力**：根据硬件配置支持多线程并发
- **接口数量**：取决于api.json配置
- **支持平台**：Windows、Linux、MacOS
- **代理支持**：HTTP、SOCKS4、SOCKS5

### ⚠️ 安全提示

1. **合法使用**：本工具仅用于短信接口测试和安全研究，禁止用于任何非法用途！

2. **风险提示**：滥用本工具可能导致法律责任，使用者需自行承担所有风险！

3. **道德准则**：请尊重他人隐私，不要将本工具用于骚扰或攻击他人！

4. **技术研究**：鼓励将本工具用于网络安全研究和漏洞挖掘，为网络安全事业贡献力量！

### ❓ 常见问题

- **Q: 为什么接口成功率不高？**
  **A: 可能是接口已失效或被风控，建议使用 `update` 命令更新接口库。**

- **Q: 为什么会出现代理错误？**
  **A: 可能是代理IP已失效或被封锁，建议更换代理列表。**

- **Q: 为什么运行速度很慢？**
  **A: 可能是网络环境不佳或CPU性能不足，建议关闭其他占用资源的程序。**

- **Q: 为什么会被服务商拉黑？**
  **A: 频繁测试同一接口可能触发风控机制，建议使用代理并控制测试频率。**

### Development

1. Download 下载项目

```shell
git clone https://github.com/AdminWhaleFall/SMSBoom.git/
```

2. 配置虚拟环境 Deploy Virtual Envirement  

**前提条件:** 请确保自己的电脑有 `python3.x` 的环境,推荐使用 `3.8` 及以上!  

#### 使用 pipenv

1. 安装 pipenv 包管理工具.  

```shell
pip install pipenv
```

2. 为项目构建虚拟环境.  

```shell
pipenv install  # 仅使用轰//炸功能
pipenv install --dev # 使用 webui 调试接口功能.
```

3. 尝试运行 smsboom.py  

```shell
pipenv shell # 激活虚拟环境
python smsboom.py  # linux
```

若无报错，输出帮助信息，则说明环境已经正确安装。若报错请使用方案二

#### 不使用虚拟环境

1. 安装所需要的库

```shell
pip install -r requirements.txt # 仅使用轰//炸
pip install -r requirements-dev.txt # 使用 webui
```

2. 尝试运行 smsboom.py

```shell
python smsboom.py
```

若无报错，输出帮助信息，则说明环境已经正确安装。

#### 使用 Docker 运行

##### 方式一: 一键运行

```shell
docker run --rm lanqsh/smsboom run -t 1 -p {PHONE} -i 1
```

##### 方式二: 自建镜像

**前提条件:** 请确保当前环境已安装 [Docker](https://docs.docker.com/get-docker/).

1. 构建镜像

```shell
docker build -t whalefell/smsboom .
```

2. 尝试运行

```shell
docker run --rm whalefell/smsboom:latest --help

Usage: smsboom.py [OPTIONS] COMMAND [ARGS]...

Options:
  --help  Show this message and exit.

Commands:
  asyncrun  以最快的方式请求接口(真异步百万并发)
  onerun    单线程(测试使用)
  run       传入线程数和手机号启动轰炸,支持多手机号
  update    从 github 获取最新接口
```

#### 运行  

若使用虚拟环境,请先激活. `pipenv shell`

```shell
# 输出帮助信息
python smsboom.py --help

Usage: smsboom.py [OPTIONS] COMMAND [ARGS]...    
Options:
--help  Show this message and exit.
Commands:
run     传入线程数和手机号启动轰//炸,支持多手机号
update  从 github 获取最新接口
```

- 启动轰//炸  

帮助信息:

```shell
python smsboom.py run --help

Usage: smsboom.py run [OPTIONS]

传入线程数和手机号启动轰//炸,支持多手机号

Options:
-t, --thread INTEGER       线程数(默认64)
-p, --phone TEXT           手机号,可传入多个再使用-p传递  [required]
-f, --frequency INTEGER    执行次数(默认1次)
-i, --interval INTEGER     间隔时间(默认60s)
-e, --enable_proxy BOOLEAN 开启代理(默认关闭)
--help                     Show this message and exit.
```

### 使用代理

本项目不能通过API自动获取代理, 你可以从下面的免费代理网站中手动获取代理, 或是选择使用自己的代理, 或是不使用代理.

> [https://proxyscrape.com/free-proxy-list](https://proxyscrape.com/free-proxy-list)

> [https://openproxy.space/list](https://openproxy.space/list)

将代理添加到 `http_proxy.txt` `socks4_proxy.txt` `socks5_proxy.txt` 三个文件中, 命令参数添加 `-e` 执行即可.

## 超级功能详解

### 🔧 核心功能

1. **多线程/异步请求**：采用多线程和异步IO技术，支持高并发请求，提高测试速度！

2. **丰富的接口库**：通过api.json配置接口，可根据需要添加和更新短信接口！

3. **代理支持**：支持HTTP、SOCKS4、SOCKS5代理，提高测试的稳定性和可靠性！

4. **多模式测试**：支持单线程、多线程、异步三种测试模式，满足不同场景的测试需求！

5. **灵活的参数配置**：可自定义线程数、执行次数、间隔时间等参数，适应不同测试场景！

### 🚀 性能参数

- **并发能力**：根据硬件配置支持多线程并发
- **接口数量**：取决于api.json配置
- **支持平台**：Windows、Linux、MacOS
- **代理支持**：HTTP、SOCKS4、SOCKS5

### 💣 测试效果

- **多接口同时测试**：同时向所有配置的接口发送请求
- **多手机号支持**：可同时测试多个手机号
- **循环测试**：可设置循环次数和间隔时间
- **代理切换**：可配置多个代理同时使用

## 安全提示

1. **合法使用**：本工具仅用于短信接口测试和安全研究，禁止用于任何非法用途！

2. **风险提示**：滥用本工具可能导致法律责任，使用者需自行承担所有风险！

3. **道德准则**：请尊重他人隐私，不要将本工具用于骚扰或攻击他人！

4. **技术研究**：鼓励将本工具用于网络安全研究和漏洞挖掘，为网络安全事业贡献力量！

## 常见问题

### Q: 为什么接口成功率不高？
A: 可能是接口已失效或被风控，建议使用 `update` 命令更新接口库。

### Q: 为什么会出现代理错误？
A: 可能是代理IP已失效或被封锁，建议更换代理列表。

### Q: 为什么运行速度很慢？
A: 可能是网络环境不佳或CPU性能不足，建议关闭其他占用资源的程序。

### Q: 为什么会被服务商拉黑？
A: 频繁测试同一接口可能触发风控机制，建议使用代理并控制测试频率。

## Donation / Sponsor

Donation is not available at the moment.
暂时不开放赞助

## Star ♥  Trend

<img src="https://starchart.cc/OpenEthan/smsboom.svg">

## ✨Discussion

欢迎加入讨论对项目提出问题和建议！！！mua!
