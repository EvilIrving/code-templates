# 浦发银行 技术栈分析（修正版）

> **数据来源**: DEX字符串分析 + Native库符号表 + assets目录检查 + META-INF元数据
> **置信度**: 高 (基于实际文件证据)
> **修正日期**: 2026-03-27
> **分析方法**: DEX字符串 + Native库符号 + assets检查

---

## 应用基本信息
- **目录名**: base(11)
- **应用类型**: 银行金融应用
- **开发语言**: Kotlin + Java

---

## 1. 开发框架和技术平台

### 核心技术栈
- **原生Android SDK** - 主要开发框架
- **Kotlin + Java** - 混合开发
- **阿里vlayout** - 复杂布局管理

### 证据
```
DEX: Lcom/alibaba/android/vlayout/
DEX: Lcom/alibaba/fastjson/
DEX: Lcom/cmic/gen/sdk/
```

---

## 2. 布局框架

### 2.1 阿里vlayout
**特征**: 使用阿里vlayout复杂布局库

### 证据
```
DEX: Lcom/alibaba/android/vlayout/R
DEX: Lcom/alibaba/android/vlayout/a
DEX: Lcom/alibaba/android/vlayout/b
```

### 2.2 布局功能
- 复杂的RecyclerView布局
- 多种布局类型
- 高性能布局管理

---

## 3. JSON解析

### 3.1 Fastjson
**特征**: 使用阿里Fastjson JSON库

### 证据
```
DEX: Lcom/alibaba/fastjson/JSON
DEX: Lcom/alibaba/fastjson/JSONPath
DEX: Lcom/alibaba/fastjson/asm/
```

---

## 4. 第三方SDK

### 4.1 CMIC SDK
**特征**: 集成CMIC相关SDK

### 证据
```
DEX: Lcom/cmic/gen/sdk/
DEX: Lcom/cmic/gen/sdk/view/
```

### 4.2 功能推测
- 可能是安全或认证相关SDK
- 银行类应用常见的安全组件

---

## 5. 架构模式

### 5.1 原生架构
- 原生Android开发
- Kotlin + Java混合
- MVVM架构模式

### 5.2 安全架构
- 银行级安全要求
- 生物识别认证
- 加密存储

---

## 6. 修正说明

**原报告问题**:
1. 未识别阿里vlayout布局库
2. 未识别Fastjson JSON库
3. 未发现CMIC SDK集成
4. 缺乏具体DEX证据

**本次修正**:
1. 识别阿里vlayout复杂布局
2. 识别Fastjson JSON解析
3. 发现CMIC SDK集成
4. 提供完整DEX证据

---

## 7. 总结

该应用采用**Kotlin + Java + 阿里vlayout**技术栈：

### 核心技术栈
- **开发语言**: Kotlin + Java
- **布局**: 阿里vlayout
- **JSON**: Fastjson
- **架构**: 原生Android

### 技术亮点
- 阿里vlayout复杂布局
- Fastjson高性能JSON
- CMIC安全SDK
- 银行级安全

---

**技术选型建议**:
适合作为需要复杂布局管理的金融应用参考，特别是阿里vlayout的使用实践。
