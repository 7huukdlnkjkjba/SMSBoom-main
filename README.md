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
| 基础呼死你 | `python smsboom.py callrun -p 手机号` |
| 加强版呼死你 | `python smsboom.py callrun -t 64 -p 手机号 -f 10` |

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
6. **呼死你功能**：支持语音验证码轰炸，通过voice_api.json配置语音接口

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