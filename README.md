# xby-mermaid-doc

DeepSeek Harness (DSH) 的插件：Mermaid文档生成服务

Mermaid Doc MCP Server是一个用于生成Mermaid文档的服务器，提供列出可用图表和检索特定图表文档的功能。

## 功能

- **set_xby_apikey** — 在聊天中设置 API 密钥（自动持久化，重启有效）
- **get_diagram_doc** — 
Retrieve the documentation content for a specific Mermaid diagram.

Args:
    diagram_name (DiagramType): The name of the diagram. Possible values are: 'architecture', 'block', 'c4', 'classDiagram', 'entityRelationshipDiagram', 'examples', 'flowchart', 'gantt', 'gitgraph', 'kanban', 'mindmap', 'packet', 'pie', 'quadrantChart', 'radar', 'requirementDiagram', 'sankey', 'sequenceDiagram', 'stateDiagram', 'timeline', 'userJourney', 'xyChart', 'zenuml'. These are case sensitive strings.

Returns:
    str: The documentation content as a string, or an empty string if the diagram is not found.


## 安装

### 方式一：从 GitHub 直接安装（推荐）

```bash
# 格式: dsh plugin --profile <profile> add github:<owner>/<repo>
dsh plugin --profile web add github:xby_skill/xby-mermaid-doc
```

### 方式二：从本地目录安装（开发模式）

```bash
# 仅用于本地开发调试
dsh plugin --profile web add /absolute/path/to/xby-mermaid-doc
```

### 方式三：通过 cordis.patch.yml 开发调试

```bash
dsh web --profile web --patch /absolute/path/to/dsh-ocr-plugin/cordis.patch.yml
```



## 配置

### 获取 API 密钥

前往 [小笨羊官网](https://xiaobenyang.com) 注册并获取 API 密钥。
