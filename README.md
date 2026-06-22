# 硅基流动 SiliconFlow 快速上手指南

> 国内可直接访问的大模型 API 平台，支持 DeepSeek、GLM、Kimi、Qwen 等主流模型。

## 为什么选硅基流动

- 🚀 **高速推理**：自研推理引擎，DeepSeek-V4-Flash 延迟低
- 💰 **价格透明**：按 token 计费，新用户有免费额度
- 🌏 **国内直连**：无需科学上网，延迟 < 50ms
- 🎯 **模型齐全**：一个 API 调通所有国产大模型

## 5 分钟接入

### 1. 注册 & 拿 API Key

访问 https://cloud.siliconflow.cn/ 注册账号，进入「API Keys」创建密钥。

### 2. Python 示例

```python
from openai import OpenAI

client = OpenAI(
    api_key="YOUR_SILICONFLOW_KEY",
    base_url="https://api.siliconflow.cn/v1",
)

resp = client.chat.completions.create(
    model="deepseek-ai/DeepSeek-V4-Flash",
    messages=[{"role": "user", "content": "你好，硅基流动！"}],
)
print(resp.choices[0].message.content)
```

### 3. 主流模型对照

| 模型 | 输入价格 | 输出价格 | 场景 |
|------|---------|---------|------|
| DeepSeek-V4-Flash | ¥1.00/M | ¥2.00/M | 日常对话 |
| GLM-5.2 | ¥8.00/M | ¥28.00/M | 复杂推理 |
| Qwen3-Coder | ¥4.00/M | ¥12.00/M | 代码生成 |
| Kimi-K2.7-Code | ¥6.50/M | ¥27.00/M | 长文本 |

## 下一步

- 🛠 接入 LangChain / Dify
- 📊 用 New-API 统一管理多模型
- 💼 企业级私有化部署

---

*本文首发于 Gitee / GitHub，更多内容持续更新。*
