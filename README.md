# GenNova Box

Windows 本地推理客户端。安装后管理本地模型、进行私有聊天，并为本机应用提供 OpenAI 兼容 API。

- [产品与下载页面](https://gennova.sage.org.ai/download.html)
- [v0.1.0 预览版安装包](https://github.com/GenNova-HUST/gennova-box-releases/releases/download/v0.1.0/GenNova-Box-0.1.0-x64.msi)
- [版本记录与 SHA256](https://github.com/GenNova-HUST/gennova-box-releases/releases/tag/v0.1.0)

双击 MSI 安装。首次启动会下载 Qwen3 4B（约 2.50 GB），随后可离线使用。客户端也支持 Qwen3 0.6B 和导入 GGUF。下载会依次尝试 Hugging Face、hf-mirror.com，并校验固定 SHA-256。

关闭主窗口后驻留系统托盘，本机 API 保持运行。双击托盘图标或桌面快捷方式重新打开；右键托盘图标可停止服务或彻底退出。不会默认设置开机自启动。

要求：Windows 10/11 x64、.NET Framework 4.8 和 [Microsoft Visual C++ v14 x64 运行库](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)。Vulkan GPU 优先，支持 CPU 模式。已在 Windows 11 / Radeon 8060S 上进行实机验证；其他设备的兼容性尚在完善。本预览版未进行代码签名。

API 地址 `http://127.0.0.1:18181/v1`，模型别名 `gennova-local`。在客户端复制包含本机访问密钥的 API 配置。服务只监听回环地址，不向局域网开放。

当前本地后端为 llama.cpp b12110，MIT；Qwen3 权重采用 Apache 2.0，并在首次使用时下载。第三方许可证随客户端安装到本地数据目录。客户端程序与其安装包不代表对 GenNova 研究引擎的性能承诺。

在 Windows“已安装的应用”中卸载。程序与快捷方式会移除，模型和日志保留在 `%LOCALAPPDATA%\GenNova\Box`。

本仓库仅分发公开安装包、使用说明与版本记录。客户端源码保存在组织私有仓库。

组织级整理与发布规则：[GN-PUBLISH-001](https://github.com/GenNova-HUST/gennova-knowledge/blob/main/governance/measurement-publication.md)（产品入口、实测口径、历史维护与公开边界）。
