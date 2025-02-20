# Free-riding_on_DeepSeek
白嫖满血deepSeek
https://github.com/yuning029/Free-riding_on_DeepSeek


# 远程服务器配置（白嫖不用看）
## 在 Chatbox 中连接远程 Ollama 服务

除了可以轻松连接本地 Ollama 服务，Chatbox 也支持连接到运行在其他机器上的远程 Ollama 服务。

例如，你可以在家中的电脑上运行 Ollama 服务，并在手机或其他电脑上使用 Chatbox 客户端连接到这个服务。

你需要确保远程 Ollama 服务正确配置并暴露在当前网络中，以便 Chatbox 可以访问。**默认情况下，需要对远程 Ollama 服务进行简单的配置**。

### 如何配置远程 Ollama 服务？

默认情况下，Ollama 服务仅在本地运行，不对外提供服务。要使 Ollama 服务能够对外提供服务，你需要设置以下两个环境变量：

```bash
OLLAMA_HOST=0.0.0.0
OLLAMA_ORIGINS=*
```

### 在 MacOS 上配置

1. 打开命令行终端，输入以下命令：

   ```bash
   launchctl setenv OLLAMA_HOST "0.0.0.0"
   launchctl setenv OLLAMA_ORIGINS "*"
   ```

2. 重启 Ollama 应用，使配置生效。

### 在 Windows 上配置

在 Windows 上，Ollama 会继承你的用户和系统环境变量。

1. 通过任务栏退出 Ollama。

2. 打开设置（Windows 11）或控制面板（Windows 10），并搜索“环境变量”。

3. 点击编辑你账户的环境变量。

   为你的用户账户编辑或创建新的变量 **OLLAMA_HOST**，值为 **0.0.0.0**； 为你的用户账户编辑或创建新的变量 **OLLAMA_ORIGINS**，值为 *****。

4. 点击确定/应用以保存设置。

5. 从 Windows 开始菜单启动 Ollama 应用程序。

### 在 Linux 上配置

如果 Ollama 作为 systemd 服务运行，应使用 systemctl 设置环境变量：

1. 调用 `systemctl edit ollama.service` 编辑 systemd 服务配置。这将打开一个编辑器。

2. 在 [Service] 部分下为每个环境变量添加一行 Environment：

   ```
   [Service]
   Environment="OLLAMA_HOST=0.0.0.0"
   Environment="OLLAMA_ORIGINS=*"
   ```

3. 保存并退出。

4. 重新加载 systemd 并重启 Ollama：

   ```
   systemctl daemon-reload
   systemctl restart ollama
   ```

# 白嫖从此处看
### 服务 IP 地址

配置后，Ollama 服务将能在当前网络（如家庭 Wifi）中提供服务。你可以使用其他设备上的 Chatbox 客户端连接到此服务。

Ollama 服务的 IP 地址是你电脑在当前网络中的地址，通常形式如下：

```
192.168.XX.XX
```

在 Chatbox 中，将 API Host 设置为：

```
http://192.168.XX.XX:11434
```

![image](https://github.com/user-attachments/assets/f7ac4420-b641-4b54-8fa2-beb67f525a91)


然后就可以提问了

![image](https://github.com/user-attachments/assets/f3c71419-d372-47cf-829c-051adcc8d698)

### chatbox

```
https://github.com/Bin-Huang/chatbox/releases
```

### ollama

```
https://ollama.com/
```

### 白嫖网站（模型网站）

```
实时更新大模型
https://freeollama.oneplus1.top/
http://23.95.20.225:8000/
```
![image](https://github.com/user-attachments/assets/2c16d200-bb69-4cb7-9a40-2588ed4e7b93)
![image](https://github.com/user-attachments/assets/d690bd63-b3ae-4469-9f8f-beb0593090f8)

### 感谢边亮老师的推荐

```
【[建议收藏]我找到了白嫖满血版的“好”办法-哔哩哔哩】 https://b23.tv/58GUCdL
```

