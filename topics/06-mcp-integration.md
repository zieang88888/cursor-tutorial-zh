# 06 MCP 集成

> 让 Cursor 连接外部工具：读数据库、操作 Figma、查浏览器——MCP 把 AI 的"手"伸到你的工具链里。

## MCP 是什么

- **全称**：Model Context Protocol，模型上下文协议
- **定位**：AI 与外部工具/数据源之间的标准接口协议
- **通俗理解**：给 AI 装"外挂能力"——原本 AI 只能读文件，通过 MCP 可以查数据库、操作浏览器、调用设计工具
- **适用场景**：需要 AI 直接接触项目外部数据或工具时

## 配置 MCP 服务

- **操作路径**：项目根目录创建 `.cursor/mcp.json` → 填入服务配置 → 重启/刷新 Cursor
- **配置示例**：
  ```json
  {
    "mcpServers": {
      "my-db": {
        "command": "npx",
        "args": ["-y", "@modelcontextprotocol/server-postgres", "postgresql://user:pass@localhost:5432/db"]
      }
    }
  }
  ```
- **管理入口**：Settings → MCP → 查看连接状态、启用/停用

## 常用 MCP 服务

| MCP 服务 | 能力 | 适用场景 |
| --- | --- | --- |
| PostgreSQL / MySQL | 查表、执行 SQL | 数据库操作 |
| Figma Context | 读取设计稿信息 | 设计稿转代码 |
| Browser / Playwright | 打开网页、读取页面 | 网页抓取、自动化测试 |
| GitHub | 仓库、Issue、PR 操作 | 开发协作 |
| Fetch | 抓取 URL 内容 | 文档阅读、API 调试 |

## 怎么找到需要的 MCP

- 官方市场：https://mcp.cursor.com/ 与 registry
- 社区聚合：awesome-mcp-servers 等列表
- **避坑**：MCP 服务来源五花八门，优先用官方/知名维护者的包，避免安装来源不明的服务器

## 自带 MCP：@ 连接器

- **操作路径**：Chat/Composer 输入 `@` → 选择 `Connectors` → 选择已配置的 MCP
- **用法**：提问时 @ 对应连接器，AI 自动调用该工具
- **示例**："@figma 看下这个设计的间距规范" → AI 读取 Figma 节点信息回答

## MCP 授权与安全

- **权限控制**：Settings → MCP 可对每个服务设置允许/拒绝的工具调用
- **风险提醒**：数据库类 MCP 有写权限时，AI 可能执行破坏性 SQL——重要环境只给只读权限
- **避坑**：token/密码写在 mcp.json 会被提交到仓库，敏感配置用环境变量或 .cursor/mcp.local.json（需自行 gitignore）

## 自建 MCP 服务

- **适用场景**：公司内部系统、私有数据源没有现成 MCP 时
- **快速上手**：官方 SDK（TypeScript/Python）写一个 server，几十行即可暴露一个工具
- **小技巧**：先做只读工具（查询），验证稳定后再加写操作

## 本地 MCP vs 远程 MCP

- **本地（stdio）**：`command + args` 启动子进程，简单直接，适合本机工具
- **远程（SSE/HTTP）**：`url` 指向远端服务，适合共享服务、公司内部部署
- **避坑**：远程 MCP 注意鉴权；本地 MCP 注意 `npx` 首次下载耗时

## 一句话原则

> **MCP 是"按需装的手"——别一次性装一堆，装你真正要 AI 碰的工具，并管好权限。**
