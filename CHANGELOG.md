# 更新日志

本项目的所有重要变更都记录在此文件中。

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)，
版本号遵循[语义化版本](https://semver.org/lang/zh-CN/)。

## [未发布]

## [1.0.0] - 2026-09-09

### 新增

- 新增 `--ty-tooltip-bg-color`、`--meta-block-bg-color`、`--meta-block-color`、`--mathjax-midline-bg-color` 主题变量，tooltip、YAML 元信息块与数学公式的配色可独立适配浅色/深色模式
- README 补充 Windows、macOS、Linux 三个平台的 Typora 主题目录说明，编译命令改用「主题目录」占位符，不再包含机器特定路径

### 变更

- 编译产物 `light-and-dark-lb.css` 不再纳入版本库，改由 [GitHub Release](https://github.com/lb-fes/typora-theme/releases) 分发
- Sass 模块导入由弃用的 `@import` 迁移至 `@use`
- `.editorconfig` 的 `end_of_line` 由 `crlf` 修正为 `lf`；`vsc-scheme.scss` 缩进统一为空格，十六进制颜色统一为小写

### 修复

- 修复浅色模式下 tooltip 文字不可见的问题：`.ty-tooltip` 背景不再绑定 `--side-bar-bg-color`，改用新增的 `--ty-tooltip-bg-color`（#1）
- 修复深色模式下 YAML 元信息块与数学公式 `.md-mathjax-midline` 使用硬编码浅色背景导致的显示异常
- 修复任务列表复选框与文字垂直错位的问题：任务列表内段落行高恢复为 1.6，与内置 GitHub 主题一致

### 移除

- 移除永远不会匹配的失效 CodeMirror 规则（`.cm-s-inner` 下的 `.cm-atom` 与 `.cm-comment`）

[未发布]: https://github.com/lb-fes/typora-theme/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/lb-fes/typora-theme/releases/tag/v1.0.0
