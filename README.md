### 📱 Redux Meituan（仿美团外卖移动端）

一个基于 React 与 Redux 构建的仿美团外卖移动端项目。项目完整实现了外卖点餐的核心业务流程，涵盖商品分类展示、购物车联动以及订单结算等功能，并通过 `json-server` 在本地模拟后端接口数据。

### ✨ 核心功能

- **商品分类与菜单联动**：左侧分类菜单与右侧商品列表动态切换高亮，数据由 Redux 统一管理。
- **购物车与数量增减**：支持商品加购、移除与数量调整，购物车状态与商品列表实时同步。
- **数据持久化**：基于 `json-server` 模拟 RESTful API，通过 `server/data.json` 提供接口数据。
- **多环境配置**：内置 `.env.development`、`.env.test`、`.env.production`，支持灵活切换请求地址。

### 🛠️ 技术栈

- **核心框架**：React
- **状态管理**：Redux Toolkit (`@reduxjs/toolkit`)、React-Redux
- **网络请求**：Axios
- **样式预处理器**：Sass / SCSS
- **Mock 服务**：json-server
- **辅助工具**：classnames、lodash

### 📂 项目结构

```text
redux-meituan/
├── public/                 # 静态资源
├── server/                 # Mock 数据服务
│   └── data.json           # 模拟后端数据
├── src/
│   ├── components/         # 组件目录
│   │   ├── Cart/           # 购物车组件
│   │   ├── Count/          # 数量控制组件
│   │   ├── FoodsCategory/  # 商品分类组件
│   │   ├── Menu/           # 左侧菜单
│   │   └── NavBar/         # 顶部导航栏
│   ├── store/              # Redux 状态管理
│   │   ├── modules/
│   │   │   └── takeaway.js # 外卖业务逻辑
│   │   └── index.js        # Store 配置
│   ├── App.js              # 根组件
│   ├── App.scss            # 全局样式
│   └── index.js            # 应用入口
├── .env.development        # 开发环境配置
├── .env.test               # 测试环境配置
├── .env.production         # 生产环境配置
└── package.json            # 项目配置
```

### 🚀 快速开始

```bash
# 1. 安装依赖
npm i

# 2. 启动 Mock 接口服务（默认端口 3004）
npm run serve

# 3. 启动前端项目
npm run start
```

### 🔗 相关链接

- **在线预览**：https://mark-1994.github.io/redux-meituan/
- **参考 UI**：[美团外卖 H5 端](https://h5.waimai.meituan.com/waimai/mindex/home)
- **接口部署**：https://dashboard.suga.app/
