# 浦发银行 技术栈分析

## 应用基本信息
- **目录名**: base(11)
- **应用类型**: 银行金融应用
- **签名**: SPDBCCC.RSA

---

## 1. 开发框架和技术平台

### 核心框架
- **原生 Android SDK** - 主框架
- **Kotlin** - 开发语言
- **Java** - 部分模块

---

## 2. 第三方库和依赖

### AndroidX 核心
- androidx.activity
- androidx.appcompat
- androidx.arch.core
- androidx.biometric (生物识别)
- androidx.cardview
- androidx.coordinatorlayout
- androidx.core
- androidx.fragment
- androidx.lifecycle
- androidx.loader
- androidx.media
- androidx.recyclerview
- androidx.transition
- androidx.viewpager2

### 数据存储
- **Realm** (realm-kotlin-extensions) - 移动数据库

### 网络
- **Retrofit** - HTTP客户端

### 异步处理
- **Kotlin Coroutines**
  - kotlinx_coroutines_android
  - kotlinx_coroutines_core

### UI组件
- **CornersLibrary** - 圆角组件
- **ColoredShadow** - 彩色阴影

### Material Design
- android.support.design_material - Material组件

---

## 3. 核心组件和架构模式

### 架构设计
- **MVVM** - ViewModel + LiveData
- **模块化架构** - 功能模块分离

### 安全特性
- **Biometric** - 指纹/面容识别
- 安全存储

### 核心组件
- **ViewModel** - 数据管理
- **LiveData** - 可观察数据
- **Realm** - 本地数据库

---

## 4. SDK和服务

### 安全服务
- 生物识别认证
- 加密存储

### UI服务
- Material Design组件
- 自定义UI组件

---

## 5. 技术亮点

1. **Realm数据库** - 高性能移动数据库
2. **生物识别** - 安全认证
3. **Kotlin Coroutines** - 现代异步处理
4. **Material Design** - 标准UI规范
5. **金融级安全** - 银行级安全保障

---

## 6. 总结

浦发银行采用稳定的原生技术栈：
- 原生Android开发确保稳定性
- Realm数据库提供高性能存储
- 生物识别保障安全认证
- Kotlin Coroutines现代化异步

适合作为金融银行类应用的技术参考。
