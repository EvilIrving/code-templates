# Code Templates

Flutter 开发模板与 Claude Skills 集合，提供标准化的项目初始化、开发规范和工作流工具。

## 项目结构

```
.
├── .claude/skills/          # Claude Skills 技能库
│   ├── flutter-create-app/   # 创建 Flutter 应用
│   ├── flutter-create-package/ # 创建 Flutter/Dart 包
│   ├── flutter-rules/        # Flutter 开发规范
│   ├── flutter-modify/       # Flutter 代码修改
│   ├── flutter-debug/        # Flutter 调试工具
│   ├── flutter-release/      # Flutter 发布流程
│   ├── flutter-commit/       # Git 提交规范
│   ├── flutter-animation-guide/ # 动画开发指南
│   ├── icon-generate/        # 图标生成工具
│   ├── pre-commit/           # 提交前检查
│   ├── sessionlog/           # 会话日志记录
│   └── summarize-session/    # 会话总结
├── CLAUDE.md                 # Claude 使用规范
├── sessionlog.md             # 开发日志示例
└── README.md                 # 本文件
```

## Skills 说明

### 开发创建
- **flutter-create-app**: 创建带有规范结构的 Flutter 应用
- **flutter-create-package**: 创建 Dart/Flutter 包

### 开发规范
- **flutter-rules**: Flutter 和 Dart 开发规则、最佳实践、代码风格指南

### 开发辅助
- **flutter-modify**: Flutter 代码修改辅助
- **flutter-debug**: Flutter 调试工具和方法
- **flutter-release**: Flutter 应用发布流程
- **flutter-animation-guide**: 动画系统架构和手势交互设计

### 工作流工具
- **flutter-commit**: Git 提交规范
- **pre-commit**: 提交前代码检查
- **icon-generate**: 项目 SVG Logo 生成
- **sessionlog**: 开发会话日志记录
- **summarize-session**: 会话内容总结

## 使用方式

这些 Skills 位于 `.claude/skills/` 目录下，可与 Claude Code 配合使用，提供标准化的 Flutter 开发工作流。

## 规范文档

- [CLAUDE.md](CLAUDE.md) - Claude 使用规范和行为准则
- [flutter-rules](.claude/skills/flutter-rules/SKILL.md) - 完整的 Flutter/Dart 开发规范

## 日志示例

[sessionlog.md](sessionlog.md) 包含一个 Android 应用启动失败问题的排查和修复记录，展示了多因素问题的诊断方法。
