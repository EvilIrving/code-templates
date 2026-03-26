# 美团点评 技术栈分析

## 应用基本信息
- **目录名**: base(14)
- **应用类型**: 本地生活服务应用
- **签名**: DIANPING.RSA

---

## 1. 开发框架和技术平台

### 核心框架
- **原生 Android SDK** - 主框架
- **Litho** - Facebook声明式UI框架 (重点采用)
- **mmPaaS** - 美团移动平台

### Litho 组件
目录: META-INF/litho/
| 组件 | 用途 |
|------|------|
| litho-core | 核心框架 |
| litho-widget | 基础组件 |
| litho-sections | 列表分区 |
| litho-annotations | 注解处理 |

---

## 2. 第三方库和依赖

### Android Arch Components (旧版)
| 库名 | 用途 |
|------|------|
| android.arch.core_runtime | 架构组件运行时 |
| android.arch.lifecycle_extensions | 生命周期扩展 |
| android.arch.lifecycle_livedata-core | LiveData核心 |
| android.arch.lifecycle_livedata | LiveData |
| android.arch.lifecycle_runtime | 生命周期运行时 |
| android.arch.lifecycle_viewmodel | ViewModel |

### 美团自研组件 (mmPaaS)
META-INF/mmPaaS/ - 美团移动平台SDK

---

## 3. 核心组件和架构模式

### 架构设计
- **Litho声明式UI** - 高性能列表渲染
- **mmPaaS平台** - 企业级移动开发平台
- **模块化架构** - 业务解耦

### Litho技术优势
- **异步布局** - 后台线程计算布局
- **增量渲染** - 仅更新变化部分
- **扁平化视图** - 减少视图层级
- **组件复用** - 高效内存利用

---

## 4. SDK和服务

### 服务层
META-INF/services/ - 服务注册

### 美团平台服务
- 移动开发平台 (mmPaaS)
- 企业级监控
- 动态化能力

---

## 5. 技术亮点

1. **Litho框架** - 高性能声明式UI
2. **异步布局计算** - 流畅的用户体验
3. **增量式渲染** - 高效的UI更新
4. **mmPaaS平台** - 企业级移动开发基础设施
5. **旧版Arch Components** - 保持兼容性

---

## 6. 总结

美团点评采用了Facebook的Litho框架：
- Litho声明式UI实现高性能列表
- mmPaaS企业级移动平台
- 异步布局计算优化性能
- 使用旧版Android Arch Components保持兼容

适合作为高性能列表应用和Litho框架使用的技术参考。
