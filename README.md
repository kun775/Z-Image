# Z-Image-UI

高性能 AI 图像生成应用，基于 Streamlit 构建。

## 🚀 快速开始

### 1. 启动应用

```bash
# 使用 Docker Compose 启动
docker-compose up -d
```

### 2. 访问应用

```
http://localhost:8501
```

## 📁 项目结构

```
z-image-ui/
├── app.py                 # Streamlit 应用主文件
├── Dockerfile            # Docker 构建文件
├── requirements.txt      # Python 依赖
├── docker-compose.yml    # Docker Compose 配置
└── README.md            # 项目说明
```

## 🛠️ 配置说明

### Streamlit 应用特性
- **现代化界面**：美观的响应式设计
- **实时生成**：高性能 AI 图像生成
- **历史记录**：保存生成的图片
- **API 集成**：支持外部 AI 服务

### Docker 部署
- **端口映射**：8501:8501
- **自动重启**：服务高可用性
- **时区设置**：Asia/Shanghai

## 🔧 常用命令

```bash
# 查看服务状态
docker-compose ps

# 查看日志
docker-compose logs -f

# 重启服务
docker-compose restart

# 停止服务
docker-compose down

# 重新构建镜像
docker-compose up -d --build
```

## 🎯 功能特性

- ✅ **高性能 AI 生成**：快速生成高质量图像
- ✅ **现代化 UI**：美观的用户界面
- ✅ **历史管理**：自动保存生成记录
- ✅ **Docker 容器化**：简化部署流程
- ✅ **实时预览**：即时查看生成效果

---

**🎨 开始你的 AI 图像创作之旅！**