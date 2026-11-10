# GenNova Box 公共制品

本仓库只分发公开二进制安装包、使用说明、校验值和历史版本记录。客户端与 GenNova 引擎源码均保存在组织私有仓库；这里没有源码发布。

- [产品与下载页面](https://gennova.sage.org.ai/download.html)
- [当前 PyPI 启动器 0.1.3a2](https://pypi.org/project/gennova-box/0.1.3a2/)
- [历史原生 AMD 桌面预览 0.2.1](https://github.com/GenNova-HUST/gennova-box-releases/releases/tag/v0.2.1)
- [历史 llama.cpp / GGUF 桌面预览 0.1.0](https://github.com/GenNova-HUST/gennova-box-releases/releases/tag/v0.1.0)

## 版本对应

| 组件 / 渠道 | 当前公开状态 | 说明 |
|---|---|---|
| `gennova-box` Python 启动器 | `0.1.3a2` | Linux ARM64 与 Windows x64 使用同一启动器版本，由 pip 按系统、架构和 Python ABI 选择二进制包。 |
| Windows 桌面客户端 | `0.3.0` 随 Windows `0.1.3a2` wheel 提供 | 仍处于私有验收阶段；本仓库暂不发布独立 0.3.0 MSI/EXE。 |
| 原生 AMD 独立桌面预览 | `0.2.1`，历史保留 | 需要维护者预先配置 WSL、ROCm、私有 GenNova 引擎和模型；不代表当前 PyPI 版本。 |
| llama.cpp / GGUF 桌面预览 | `0.1.0`，历史保留 | 早期 Windows 预览，与原生 GenNova AMD 路线不同。 |

既有 Release、标签、附件和 SHA-256 不会被覆盖。新版本使用新标签和新制品发布。

## 当前安装入口

需要 Python 启动器时，从 PyPI `gennova-box 0.1.3a2` 进入。Windows 包包含编译后的客户端和启动器，Linux 包包含编译后的 ARM64 启动器；公开制品均不包含客户端或引擎源码、模型权重和私有凭据。

独立 MSI/EXE 页面当前仅保留历史预览。0.3.0 在完成全新 Windows、长期稳定性、资源释放和其他适用验收前，不作为新的独立公开安装包发布。

本机 API 使用 `http://127.0.0.1:18181/v1`，只监听回环地址，并使用本机访问密钥。不同版本的模型、硬件、上下文与验证范围以对应 Release 和产品页为准，不跨版本拼接结论。

组织级整理与发布规则：[GN-PUBLISH-001](https://github.com/GenNova-HUST/gennova-knowledge/blob/main/governance/measurement-publication.md)。