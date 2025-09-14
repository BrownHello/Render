# Node.js API Demo for Render

这是一个为 Render 平台设计的 Node.js 示例项目，包含完整的 RESTful API 和简单的前端界面。

## 🚀 功能特性

- **RESTful API**: 完整的用户管理 CRUD 操作
- **响应式前端**: 美观的用户界面，支持移动端
- **健康检查**: 提供服务状态监控接口
- **错误处理**: 完善的错误处理机制
- **CORS 支持**: 跨域资源共享配置
- **环境配置**: 支持环境变量配置

## 📋 API 接口

### 用户管理
- `GET /api/users` - 获取所有用户
- `GET /api/users/:id` - 根据ID获取用户
- `POST /api/users` - 创建新用户
- `PUT /api/users/:id` - 更新用户信息
- `DELETE /api/users/:id` - 删除用户

### 系统接口
- `GET /health` - 健康检查
- `GET /` - 前端页面

## 🛠️ 本地开发

### 安装依赖
```bash
npm install
```

### 启动开发服务器
```bash
npm run dev
```

### 启动生产服务器
```bash
npm start
```

服务器将在 http://localhost:3000 启动

## 🌐 Render 部署

### 自动部署
1. 将代码推送到 GitHub 仓库
2. 在 Render 控制台创建新的 Web Service
3. 连接你的 GitHub 仓库
4. Render 将自动检测并部署你的应用

### 手动配置
如果需要手动配置，请使用以下设置：
- **Build Command**: `npm install`
- **Start Command**: `npm start`
- **Environment**: Node.js
- **Node Version**: 18.x 或更高

## 📁 项目结构

```
.
├── server.js          # 主服务器文件
├── package.json       # 项目配置和依赖
├── .env               # 环境变量配置
├── render.yaml        # Render 部署配置
├── public/            # 静态文件目录
│   └── index.html     # 前端页面
└── README.md          # 项目说明
```

## 🧪 测试 API

### 使用 curl 测试

```bash
# 获取所有用户
curl http://localhost:3000/api/users

# 创建新用户
curl -X POST http://localhost:3000/api/users \
  -H "Content-Type: application/json" \
  -d '{"name":"测试用户","email":"test@example.com","age":30}'

# 健康检查
curl http://localhost:3000/health
```

### 响应格式

所有 API 响应都遵循统一格式：

```json
{
  "success": true,
  "data": {},
  "message": "操作成功"
}
```

## 🔧 环境变量

| 变量名 | 说明 | 默认值 |
|--------|------|--------|
| PORT | 服务器端口 | 3000 |
| NODE_ENV | 运行环境 | development |

## 📝 版本历史

- **v1.0.0** - 初始版本
  - 基础 CRUD API
  - 响应式前端界面
  - Render 部署支持

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交 Issues 和 Pull Requests！

## 📞 支持

如果您在使用过程中遇到问题，请创建 Issue 或联系开发者。