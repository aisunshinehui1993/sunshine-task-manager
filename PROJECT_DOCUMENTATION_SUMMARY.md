# MCP Shrimp Task Manager - 项目文档总结

> 项目完整文档索引与概览 | 最后更新：2025年1月

---

## 📑 目录

1. [项目概述](#项目概述)
2. [核心文档](#核心文档)
3. [技术文档](#技术文档)
4. [用户指南](#用户指南)
5. [开发文档](#开发文档)
6. [版本历史](#版本历史)
7. [多语言支持](#多语言支持)

---

## 项目概述

**项目名称**: MCP Shrimp Task Manager  
**项目类型**: MCP (Model Context Protocol) 服务器 - AI驱动的智能任务管理系统  
**主要语言**: TypeScript  
**当前版本**: 1.0.21  
**开源许可**: MIT License  
**项目地址**: https://github.com/cjo4m06/mcp-shrimp-task-manager

### 核心价值

Shrimp Task Manager 是一个为 AI Agents 设计的任务管理工具，强调思维链、反思和风格一致性。它将自然语言转换为结构化的开发任务，并具有依赖追踪和迭代优化功能。

### 主要特性

- 🧠 **持久化内存**: 任务和进度跨会话持久化
- 📋 **结构化工作流**: 规划、执行和验证的引导流程
- 🔄 **智能分解**: 自动将复杂任务分解为可管理的子任务
- 🎯 **上下文保存**: 即使在 token 限制下也不会丢失进度
- 🔬 **研究模式**: 系统化的技术探索和解决方案比较
- 🤖 **代理系统**: 将专业化 AI 代理分配给特定任务
- 📏 **项目规则**: 定义和维护项目范围内的编码标准
- 🖥️ **Web界面**: React 和轻量级 GUI 两种可视化界面

---

## 核心文档

### 1. README.md - 项目主文档

**路径**: `README.md`  
**语言**: 英文（多语言版本见 docs 目录）  
**内容概览**:

#### 快速开始
- **先决条件**: Node.js 18+, npm/yarn, MCP 兼容的 AI 客户端
- **安装步骤**:
  ```bash
  git clone https://github.com/cjo4m06/mcp-shrimp-task-manager.git
  cd mcp-shrimp-task-manager
  npm install
  npm run build
  ```
- **配置示例**: 详细的 `.mcp.json` 配置说明
- **支持的 AI 客户端**: Claude Code, Cline, Claude Desktop

#### 核心功能说明
- 任务管理工作流程
- 高级功能（研究模式、代理系统、项目规则）
- Web 界面（Task Viewer 和 Web GUI）

#### 常见用例
- 功能开发
- Bug 修复
- 研究与学习

### 2. 开发守则 (shrimp-rules.md)

**路径**: `shrimp-rules.md`  
**语言**: 简体中文  
**最近更新**: 从繁体中文转换而来

**主要章节**:

#### 项目架构
- 源代码目录结构 (`src/`)
- 编译输出 (`dist/`)
- 配置文件管理
- 文档组织

#### 代码规范
- **命名规范**: camelCase, PascalCase, kebab-case 使用指南
- **格式要求**: 2空格缩进，分号使用，引号规范
- **TypeScript 规范**: 类型注解，接口定义，严格模式

#### 功能实现规范
- 单一职责原则 (SRP)
- 错误处理最佳实践
- 日志记录规范
- Zod 数据验证使用

#### 工作流程
- 开发流程（分支管理、测试、提交）
- 版本控制 (Git)
- CHANGELOG 更新要求

#### AI 决策规范
- 处理模糊请求的策略
- 错误/异常处理优先级
- 依赖选择标准

### 3. 系统说明 (system.md)

**路径**: `system.md`  
**语言**: 简体中文  
**最近更新**: 从繁体中文转换而来

**内容**:
- AI 编码助手角色定义
- 沟通风格规范
- 工具调用规则
- 代码更改说明
- 自定义用户指令（Laravel, PHP, Livewire 等技术栈）

---

## 技术文档

### 1. 可用工具文档 (docs/tools.md)

**分类**:

#### 任务管理工具
- **核心操作**: `plan_task`, `execute_task`, `list_tasks`, `delete_task`, `complete_task`, `update_task`
- **高级操作**: `split_tasks`, `analyze_task`, `verify_task`, `reflect_task`, `query_task`
- **内存与历史**: `get_task_detail`, `clear_all_tasks`

#### 项目管理工具
- `init_project_rules`: 初始化项目标准
- `research_mode`: 进入系统化研究模式

#### 思考处理工具
- `process_thought`: 处理和构建思维链

**最佳实践**:
- 任务规划流程
- 任务执行策略
- 内存管理技巧
- Token 优化建议

### 2. 代理管理系统 (docs/agents.md)

**功能**:

#### 代理类型
| 代理类型 | 适用场景 | 示例任务 |
|---------|----------|---------|
| Frontend Developer | UI/UX 实现 | React 组件, CSS 样式 |
| Backend Engineer | 服务器端逻辑 | API 端点, 数据库查询 |
| DevOps Specialist | 基础设施 | CI/CD, 部署, 监控 |
| Data Scientist | 数据分析 | ML 模型, 数据处理 |
| Security Expert | 安全审查 | 漏洞评估, 认证 |
| QA Engineer | 测试 | 测试用例, Bug 验证 |
| Technical Writer | 文档 | API 文档, 用户指南 |

#### 使用方法
- 基本用法：分配代理到任务
- 高级功能：代理指令、代理协作
- Task Viewer 中的代理管理

#### 配置
- 自定义代理创建
- 代理模板
- 与 Claude 的集成

### 3. API 参考 (docs/api.md)

**MCP 工具端点**:

#### 任务管理 API
- `plan_task`: 规划和分析任务
- `execute_task`: 执行特定任务
- `list_tasks`: 列出所有任务
- `split_tasks`: 将复杂任务分解
- `update_task`: 更新任务属性
- `verify_task`: 验证任务完成

#### 项目管理 API
- `init_project_rules`: 初始化项目规则
- `research_mode`: 进入研究模式

#### 数据模型
```typescript
interface Task {
  id: string;
  title: string;
  status: 'pending' | 'in_progress' | 'completed' | 'failed';
  priority: number;
  dependencies: string[];
  metadata?: TaskMetadata;
}
```

**Web API** (GUI 启用时):
- REST 端点: `/api/tasks`, `/api/tasks/:id`
- WebSocket 事件: `task:created`, `task:updated`, `task:deleted`

---

## 用户指南

### 1. 使用说明 (data/使用说明.md)

**完整工作流程**:

1. **初始化项目规则** (首次使用)
   ```
   初始化项目规则
   ```

2. **规划任务**
   ```
   规划任务：实现用户登录功能
   ```

3. **任务拆分** (生成 tasks.json)
   ```
   拆分任务
   ```

4. **查看任务列表**
   ```
   列出所有任务
   ```

5. **执行任务**
   ```
   执行任务 [任务ID或任务名称]
   ```

6. **验证任务**
   ```
   验证任务 [任务ID]
   ```

**常见问题**:
- 为什么没有生成 tasks.json？
- 任务文件存储在哪里？
- 可以手动编辑 tasks.json 吗？

### 2. Task Viewer 完整指南 (tools/task-viewer/README.md)

**页面功能**:

#### 📋 任务页面
- 任务表格：可排序列，状态徽章，代理分配
- 🤖 机器人表情符号：AI 任务执行
- AI 批量代理分配（使用 GPT-4）
- 任务详情视图：导航按钮，相关文件，依赖图

#### 📜 项目历史页面
- 时间线视图
- 内存文件管理
- 任务演变追踪
- 笔记系统

#### 🤖 子代理页面
- 代理库浏览
- AI 指令列
- 代理编辑器
- 颜色编码

#### 🎨 模板页面
- 模板编辑器
- 模板类型管理
- 实时预览
- 导出/导入

#### ⚙️ 全局设置
- Claude 文件夹路径配置
- API 密钥管理
- 语言首选项

**技术架构**:
- **前端**: React 19 + Vite
- **表格组件**: TanStack React Table
- **样式**: 自定义 CSS，暗色主题
- **后端**: Node.js HTTP 服务器
- **构建系统**: Vite

**部署选项**:
- 标准部署
- Systemd 服务（Linux）
- 开发模式（热重载）

---

## 开发文档

### 1. 贡献指南 (CONTRIBUTING.md)

**贡献方式**:
- 报告 Bug
- 建议增强功能
- 第一次代码贡献

**贡献工作流**:
1. Fork & Clone
2. 安装依赖
3. 创建分支 (`feat/` 或 `fix/`)
4. 进行更改
5. 提交 (遵循 Conventional Commits)
6. 推送和开启 Pull Request
7. 代码审查
8. 合并

**PR 要求**:
- 文档更新
- CHANGELOG.md 更新
- 版本号递增（遵循 SemVer）

**测试要求**:
- 正在迁移到 Vitest
- 新代码需包含 Vitest 测试

### 2. 子代理系统规范 (SUB_AGENTS_SPECIFICATION.md)

**执行摘要**:
- 为 MCP Task Manager 实现子代理系统
- 基于任务复杂度、领域专长和工作负载分配的智能任务委托

**系统设计**:

#### 代理类型
```typescript
enum SubAgentType {
  FRONTEND = 'frontend',
  BACKEND = 'backend',
  DEVOPS = 'devops',
  FULLSTACK = 'fullstack',
  RESEARCH = 'research',
  TESTING = 'testing',
  ARCHITECTURE = 'architecture'
}
```

#### 实施阶段
1. **阶段 1: 基础** (4-6 周) - 核心子代理基础设施
2. **阶段 2: 委托引擎** (3-4 周) - 智能任务路由
3. **阶段 3: UI 集成** (2-3 周) - 子代理管理界面
4. **阶段 4: 高级功能** (4-5 周) - 工作负载平衡和分析

**技术规范**:
- 数据库架构扩展
- API 端点
- 配置架构
- 性能优化

---

## 版本历史

### CHANGELOG.md - 完整变更记录

**最新版本**: 1.0.21 (2025-01-13)

#### 主要版本亮点

**v1.0.21** - Task Viewer 工具
- 完整的基于 React 的 Web 界面
- 现代标签界面，支持拖放
- 实时搜索和过滤
- 可配置的自动刷新
- 专业暗色主题

**v1.0.20** - 依赖图增强
- 重置按钮和缩略图视图
- 增强的依赖图交互

**v1.0.19** - 研究模式
- 添加系统化编程研究功能
- 研究模式提示和模板（中英文）

**v1.0.18** - Bug 修复
- 移除不必要的 console.log 输出
- 修复 WebGUI 国际化问题

**v1.0.12** - WebGUI 功能
- 添加基于 Web 的图形界面
- 由 `ENABLE_GUI` 环境变量控制

**v1.0.10** - 多语言支持
- 添加提示语言和自定义说明
- `TEMPLATES_USE` 配置选项
- 多语言任务模板（英文/中文）

### 版本演进趋势
- 从基础功能到高级 AI 集成
- 从命令行到全功能 Web 界面
- 从单语言到多语言支持
- 从简单任务管理到复杂代理系统

---

## 多语言支持

### 可用语言版本

项目文档支持以下语言：

#### 核心文档
- 🇺🇸 **English** (英文) - 主要文档语言
- 🇨🇳 **中文** (简体中文) - 完整翻译
- 🇩🇪 **Deutsch** (德语)
- 🇪🇸 **Español** (西班牙语)
- 🇫🇷 **Français** (法语)
- 🇮🇹 **Italiano** (意大利语)
- 🇰🇷 **한국어** (韩语)
- 🇧🇷 **Português** (葡萄牙语)
- 🇷🇺 **Русский** (俄语)
- 🇮🇳 **हिन्दी** (印地语)

#### 文档路径
- README: `docs/{语言代码}/README.md`
- CHANGELOG: `docs/{语言代码}/CHANGELOG.md`
- 提示自定义: `docs/{语言代码}/prompt-customization.md`

#### 提示模板语言
- 位置: `src/prompts/{语言代码}/`
- 配置: 通过 `TEMPLATES_USE` 环境变量设置
- 支持: en (英文), zh (中文)

---

## 文档组织结构

```
mcp-shrimp-task-manager/
├── README.md                          # 项目主文档（英文）
├── CHANGELOG.md                       # 版本变更记录（英文）
├── CONTRIBUTING.md                    # 贡献指南
├── LICENSE                            # MIT 许可证
├── shrimp-rules.md                    # 开发守则（简体中文）
├── system.md                          # 系统说明（简体中文）
├── SUB_AGENTS_SPECIFICATION.md        # 子代理规范（英文）
│
├── docs/                              # 文档目录
│   ├── README.md                      # 文档索引（英文）
│   ├── tools.md                       # 可用工具文档
│   ├── agents.md                      # 代理管理文档
│   ├── api.md                         # API 参考
│   │
│   ├── en/                            # 英文文档
│   │   └── prompt-customization.md
│   │
│   ├── zh/                            # 中文文档
│   │   ├── README.md
│   │   ├── CHANGELOG.md
│   │   └── prompt-customization.md
│   │
│   └── [其他语言目录]/
│
├── data/                              # 数据和使用说明
│   ├── 使用说明.md                     # 中文使用指南
│   ├── WebGUI.md                      # WebGUI 链接
│   └── tasks.json                     # 任务数据（由系统生成）
│
├── tools/                             # 工具目录
│   └── task-viewer/                   # Task Viewer 工具
│       ├── README.md                  # Task Viewer 完整文档
│       ├── releases/                  # 发布说明
│       └── [源代码文件]
│
└── src/                               # 源代码
    ├── prompts/                       # 提示模板
    │   ├── en/                        # 英文提示
    │   └── zh/                        # 中文提示
    └── [其他源代码目录]
```

---

## 快速导航

### 新用户
1. 📖 阅读 [README.md](README.md) 了解项目概况
2. 🚀 按照快速开始指南安装
3. 📝 查看 [使用说明](data/使用说明.md) 学习工作流程
4. 🖥️ 安装 [Task Viewer](tools/task-viewer/README.md) 获得可视化界面

### 开发者
1. 📋 阅读 [开发守则](shrimp-rules.md)
2. 🛠️ 查看 [可用工具文档](docs/tools.md)
3. 🤖 学习 [代理系统](docs/agents.md)
4. 🔌 参考 [API 文档](docs/api.md)
5. 🤝 遵循 [贡献指南](CONTRIBUTING.md)

### 高级用户
1. 🔬 探索研究模式功能
2. 🎨 自定义提示模板
3. 📊 使用 Task Viewer 的高级特性
4. 🤖 配置和管理子代理

---

## 文档维护

### 最近更新
- ✅ 2025年10月21日: 将 shrimp-rules.md 从繁体中文转换为简体中文
- ✅ 2025年10月21日: 将 system.md 从繁体中文转换为简体中文
- ✅ 2025年10月21日: 更新 data/WebGUI.md 语言代码（zh-TW → zh-CN）

### 待更新项目
- 📌 完善中文版本的技术文档
- 📌 添加更多代码示例
- 📌 创建视频教程链接
- 📌 补充故障排除指南

---

## 联系与支持

- **GitHub Issues**: [提交 Bug 或功能请求](https://github.com/cjo4m06/mcp-shrimp-task-manager/issues)
- **GitHub Discussions**: [社区讨论](https://github.com/cjo4m06/mcp-shrimp-task-manager/discussions)
- **发布说明**: [查看最新版本](https://github.com/cjo4m06/mcp-shrimp-task-manager/releases)

---

## 许可证

本项目基于 MIT 许可证开源。详见 [LICENSE](LICENSE) 文件。

---

<div align="center">
  <p>
    由 <a href="https://github.com/cjo4m06">cjo4m06</a> 创建 • 由社区维护
  </p>
  <p>
    <a href="https://github.com/cjo4m06/mcp-shrimp-task-manager">⭐ Star on GitHub</a> •
    <a href="https://github.com/cjo4m06/mcp-shrimp-task-manager/issues">🐛 Report Bug</a> •
    <a href="https://github.com/cjo4m06/mcp-shrimp-task-manager/discussions">💬 Discuss</a>
  </p>
</div>

---

*本文档总结生成于 2025年10月21日*  
*文档版本: 1.0.0*

