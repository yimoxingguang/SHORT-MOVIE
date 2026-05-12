# SHORT-MOVIE 项目

## 项目描述

SHORT-MOVIE 是一个全栈短视频平台项目，包括用户前端、管理后台前端和Java后端服务。用户可以通过前端观看和管理短视频，管理员可以通过后台管理系统进行视频审核、用户管理和数据分析。

## 技术栈

- **前端（用户端）**: Vue.js + Vite + Less + JavaScript
- **前端（管理端）**: Vue.js + Vite + Less + JavaScript
- **后端**: Java + Spring Boot + MyBatis Plus + MinIO + JWT
- **数据库**: MySQL (假设)
- **包管理**: pnpm (前端), Maven (后端)

## 项目结构

```
SHORT-MOVIE/
├── admin infront/          # 管理后台前端
│   ├── src/
│   │   ├── components/     # Vue组件
│   │   ├── layouts/        # 布局组件
│   │   ├── router/         # 路由配置
│   │   ├── views/          # 页面视图
│   │   └── ...
│   ├── package.json
│   ├── pnpm-lock.yaml
│   └── vite.config.js
├── user infront/           # 用户前端
│   ├── src/
│   │   ├── components/     # Vue组件
│   │   ├── router/         # 路由配置
│   │   ├── views/          # 页面视图
│   │   └── ...
│   ├── package.json
│   ├── pnpm-lock.yaml
│   └── vite.config.js
├── shortmovie/             # Java后端
│   ├── src/main/java/com/example/shortmovie/
│   │   ├── config/         # 配置类
│   │   ├── controller/     # 控制器
│   │   ├── service/        # 服务层
│   │   ├── entity/         # 实体类
│   │   ├── mapper/         # 数据映射
│   │   └── ...
│   ├── src/main/resources/
│   │   └── application.yml # 配置文件
│   └── pom.xml             # Maven配置
└── README.md               # 项目说明
```

## 安装和运行

### 前提条件

- Node.js (版本 16+)
- pnpm
- Java 17+
- Maven
- MySQL (或配置的数据库)

### 后端安装和运行

1. 进入后端目录：
   ```bash
   cd shortmovie
   ```

2. 配置数据库：在 `src/main/resources/application.yml` 中设置数据库连接信息。

3. 安装依赖并运行：
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

   后端服务将在 `http://localhost:8080` 启动。

### 用户前端安装和运行

1. 进入用户前端目录：
   ```bash
   cd "user infront"
   ```

2. 安装依赖：
   ```bash
   pnpm install
   ```

3. 运行开发服务器：
   ```bash
   pnpm run dev
   ```

   用户前端将在 `http://localhost:3000` (或Vite默认端口) 启动。

### 管理后台前端安装和运行

1. 进入管理后台目录：
   ```bash
   cd "admin infront"
   ```

2. 安装依赖：
   ```bash
   pnpm install
   ```

3. 运行开发服务器：
   ```bash
   pnpm run dev
   ```

   管理后台将在 `http://localhost:3001` (或Vite默认端口) 启动。

## 功能特性

- **用户端**:
  - 视频播放和浏览
  - 用户登录/注册
  - 视频推荐

- **管理端**:
  - 用户管理
  - 视频审核
  - 数据分析
  - 权限管理

- **后端**:
  - RESTful API
  - JWT认证
  - 文件上传 (MinIO)
  - 数据库操作

## 开发指南

- 前端使用Vue 3 Composition API
- 后端遵循Spring Boot最佳实践
- 代码风格：请保持一致，使用ESLint (前端) 和Checkstyle (后端)

## 贡献

欢迎提交Issue和Pull Request。请确保代码通过测试并遵循项目规范。

## 许可证

[MIT License](LICENSE)