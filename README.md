# Design Language Compiler

Design Language Compiler is a Codex skill for analyzing a real website URL with browser automation plus LLM reasoning, then producing semantic design-language artifacts.

It helps an agent:

- inspect a live page through browser evidence
- separate observations into visual, structural, layout, and interaction layers
- synthesize a semantic design language summary
- write both machine-readable JSON and human-readable reports

## What It Outputs

- `report.md`
- `report.zh.md` when Chinese output is useful or requested
- `design_language.json`
- `scene_graph.json`
- `component_graph.json`
- `layout_graph.json`
- `interaction_graph.json`
- `manifest.json`

## Workflow

1. Confirm the URL, depth, output language, and target surfaces.
2. Open the page with the best available browser runtime.
3. Collect desktop and mobile first-meaningful states when feasible.
4. Split browser evidence into:
   - Visual Layer
   - DOM Structure
   - Layout Geometry
   - Interaction Signals
5. Use the LLM to synthesize the site’s design language.
6. Write the artifact set and validate it.

## Safety

The skill avoids destructive actions such as:

- submitting forms
- logging in
- purchasing
- uploading
- deleting
- publishing
- granting permissions

Public outputs stay semantic only and should not expose selectors, DOM trees, raw CSS, source IDs, exact nesting, or pixel-level layout details.

## Repository Structure

```text
design-language-compiler/
  README.md
  SKILL.md
  agents/
    openai.yaml
  references/
    agent-operating-contract.md
    browser-reading-workflow.md
    leakage-rules.md
    schemas.md
    semantic-vocabulary.md
```

## Trigger Examples

- “Analyze this URL as a design language system.”
- “Generate a Chinese report for this website.”
- “Extract the layout grammar and interaction semantics from this page.”

---

# 设计语言编译器

设计语言编译器是一个 Codex skill，用浏览器自动化结合大模型推理来分析真实网站 URL，并输出语义化的设计语言资产。

它帮助智能体完成这些事：

- 通过浏览器证据阅读真实页面
- 把观察拆成视觉、结构、布局、行为四层
- 归纳出语义化的设计语言总结
- 同时输出机器可读 JSON 和人类可读报告

## 输出内容

- `report.md`
- `report.zh.md`，当需要中文输出时生成
- `design_language.json`
- `scene_graph.json`
- `component_graph.json`
- `layout_graph.json`
- `interaction_graph.json`
- `manifest.json`

## 工作流

1. 确认 URL、深度、输出语言和目标页面范围。
2. 使用当前环境中可用的最佳浏览器运行时打开页面。
3. 尽可能采集桌面端和移动端的首屏状态。
4. 将浏览器证据拆成四层：
   - 视觉层
   - DOM 结构层
   - 布局几何层
   - 交互信号层
5. 交给大模型做设计语言归纳。
6. 写出产物并完成校验。

## 安全边界

此 skill 会避免这些动作：

- 提交表单
- 登录
- 购买
- 上传
- 删除
- 发布
- 授权

公开输出只保留语义，不暴露选择器、DOM 树、原始 CSS、源代码 ID、精确嵌套或像素级布局信息。

## 仓库结构

```text
design-language-compiler/
  README.md
  SKILL.md
  agents/
    openai.yaml
  references/
    agent-operating-contract.md
    browser-reading-workflow.md
    leakage-rules.md
    schemas.md
    semantic-vocabulary.md
```

## 触发示例

- “把这个 URL 按设计语言系统分析一下。”
- “给这个网站生成中文报告。”
- “提取这个页面的布局语法和交互语义。”
