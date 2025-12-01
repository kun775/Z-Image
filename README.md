<div align="center">

# ShowImageWeb

</div>

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.29.0-red.svg)
![Docker](https://img.shields.io/badge/Docker-20.10+-blue.svg)

</div>

AI图像生成网页交互平台 - 基于Streamlit构建的Web应用，提供简洁的用户界面和实用的图像生成功能 - **对手机UI界面进行了优化**
## 应用预览

![ShowImageWeb Demo](assets/showimage-web-demo.png)
![ShowImageWeb Demo](assets/showimage-web-demo1.png)
## 项目结构

```
showimageweb/
├── app.py                    # 主应用文件（Streamlit界面）
├── Dockerfile               # Docker构建配置
├── requirements.txt         # Python依赖包
├── docker-compose.yml       # Docker Compose配置
├── LICENSE                  # MIT许可证
├── README.md                # 项目文档
└── assets/
    └── showimage-web-demo.png # 应用预览图
```

## Key（可蹬）

    sk-zKTGcw8llBFZLpXAAsxTmMSmCfY8DNfe

## 技术栈

- **前端框架**: Streamlit 1.29.0+
- **后端语言**: Python 3.9+
- **容器化**: Docker & Docker Compose
- **核心依赖**: requests, streamlit, base64

## 特性

- **高性能**: 基于Streamlit的快速响应界面
- **美观UI**: 现代化的卡片式设计，支持自定义画廊列数
- **响应式**: 自适应不同屏幕尺寸，适配移动端
- **历史记录**: 自动保存生成记录，支持无限数量存储
- **配置选项**: 支持随机/固定种子，自定义API配置
- **实时状态**: 生成进度实时显示，带有时间统计
- **一键下载**: PNG图片直接下载，自动命名
- **通用API**: 兼容多种AI图像生成服务
- **内存管理**: 智能存储管理，自动base64优化

## 快速开始

## 使用方式

### 方式一：Docker 部署（灵活）

```bash
# 克隆项目
git clone https://github.com/kaima2022/showimageweb.git
cd ShowImageWeb

# 使用 Docker Compose 启动
docker compose up -d
```

### 方式二：非容器化直接运行（快速）

```bash
# 克隆项目
git clone https://github.com/kaima2022/showimageweb.git
cd ShowImageWeb

# 安装依赖
pip install -r requirements.txt
# 启动
streamlit run app.py --server.address=0.0.0.0 --server.port=8501
```

### 访问应用

```
http://localhost:8501
```

## 如何更新？
### 拉取最新代码并重建启动服务

```
  git pull origin main && docker compose up -d --build
```

## API配置

应用支持任意兼容的AI图像生成API：

### 支持的API格式
- **请求方式**: POST
- **认证方式**: Bearer Token
- **请求格式**: `{"prompt": "...", "seed": ...}`
- **响应格式**: `{"base64": "..."}`

### 配置说明

#### 方式一：通过环境变量配置（推荐）

1. 复制 `env.example` 文件为 `.env`：
```bash
cp env.example .env
```

2. 编辑 `.env` 文件，填入您的API配置：
```bash
API_KEY=sk-your-api-key-here
API_BASE_URL=https://z-api.aioec.tech/proxy/generate
```

3. 应用启动时会自动从 `.env` 文件加载配置，侧边栏会显示"✅ API Key已从环境变量加载"

#### 方式二：通过界面配置

1. **API URL**: 在侧边栏输入完整的API接口地址（如：`https://api.example.com/v1/generate`）
2. **API Key**: 在侧边栏输入您的API密钥
3. **种子设置**: 支持随机种子或固定种子复现结果

> 💡 **提示**: 优先使用 `.env` 文件配置，更安全且方便管理

### 兼容的服务
- OpenAI DALL-E API
- Stable Diffusion API
- 自建AI图像服务
- 任何支持标准格式的图像生成API

## 配置选项

### 环境变量（可选）
```bash
# Streamlit配置
STREAMLIT_SERVER_ADDRESS=0.0.0.0
STREAMLIT_SERVER_PORT=8501
STREAMLIT_SERVER_HEADLESS=true

# 时区设置
TZ=Asia/Shanghai
```

### 自定义配置
- **画廊列数**: 1-4列可调
- **API超时**: 默认60秒
- **图片格式**: PNG格式输出
- **文件命名**: 时间戳自动命名

## 贡献指南

1. Fork 本项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

---
