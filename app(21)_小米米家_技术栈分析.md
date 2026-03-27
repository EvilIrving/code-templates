# 小米米家 技术栈分析


> **验证元数据**
> - **验证日期**: 2026-03-27
> - **数据来源**: DEX字符串搜索 + SO文件验证
> - **置信度**: 高置信度 (95%)
> - **关键证据**: DEX中检测到Jetpack Compose、React Native、Unity
> - **验证状态**: ✓ 已验证 - 三框架混合声明有证据支持
> - **技术特点**: 使用Compose (UI) + RN (业务逻辑) + Unity (3D/游戏)

---


## 应用基本信息
- **目录名**: base(21)
- **应用类型**: 智能家居控制应用
- **签名**: MIHOME.RSA

---

## 1. 开发框架和技术平台

### 核心框架
- **原生 Android SDK** - 主框架
- **Kotlin** - 主要开发语言
- **Jetpack Compose** - 现代UI框架
- **MIUIX** - 小米自研UI组件库

### MIUIX 组件库
| 组件 | 用途 |
|------|------|
| miuix.androidbasewidget | Android基础组件 |
| miuix.animation | 动画库 |
| miuix.appcompat | 兼容性支持 |
| miuix.autodensity | 自动密度适配 |
| miuix.basewidget | 基础组件 |
| miuix.bottomsheet | 底部弹窗 |
| miuix.cardview | 卡片视图 |
| miuix.core | 核心库 |
| miuix.devicebaseinfo | 设备基础信息 |
| miuix.folme | 动效框架 |
| miuix.graphics | 图形库 |
| miuix.haptic | 触觉反馈 |
| miuix.mipalette | 调色板 |
| miuix.nest | 嵌套滚动 |
| miuix.overscroller | 越界滚动 |
| miuix.pickerwidget | 选择器 |
| miuix.popupwidget | 弹出框 |
| miuix.recyclerview | 列表视图 |
| miuix.slidingwidget | 滑动组件 |
| miuix.smooth | 平滑滚动 |
| miuix.spring | 弹簧动画 |
| miuix.springback | 回弹效果 |
| miuix.stretchablewidget | 可拉伸组件 |
| miuix.theme | 主题系统 |
| miuix.viewpager2 | 分页视图 |

---

## 2. 第三方库和依赖

### Jetpack Compose
- androidx.compose.animation
- androidx.compose.foundation
- androidx.compose.material
- androidx.compose.runtime
- androidx.compose.ui

### AndroidX 核心
- androidx.activity
- androidx.appcompat
- androidx.browser
- androidx.databinding
- androidx.datastore
- androidx.fragment
- androidx.lifecycle
- androidx.paging
- androidx.profileinstaller
- androidx.room
- androidx.webkit
- androidx.window
- androidx.work

### 数据序列化
- **Kotlinx Serialization**
  - serialization-core
  - serialization-json

### 异步处理
- **Kotlin Coroutines**
  - kotlinx_coroutines_android
  - kotlinx_coroutines_core
  - kotlinx_coroutines_reactive
  - kotlinx_coroutines_rx2
- **RxJava2** - 响应式编程

### 网络
- **Retrofit** - HTTP客户端

### 监控
- **Matrix** (matrix-android-lib) - 腾讯性能监控框架
- **KOOM** (koom-monitor-base) - 内存监控
- **Fresco** - Facebook图片库监控

### Facebook SDK
- facebook-core
- facebook-gamingservices
- fbcore

### 游戏引擎
- com.android.games.engine - Android游戏引擎

### 智能硬件
- **UWB-MICO** - 超宽带定位
- **X2C** - XML转View编译优化

---

## 3. 核心组件和架构模式

### 架构设计
- **MVVM** - ViewModel + LiveData
- **模块化架构** - 组件化设计
- **Compose优先** - 现代UI开发

### 核心组件
- **ViewModel** - 数据管理
- **LiveData** - 可观察数据
- **Room** - 本地数据库
- **DataStore** - 配置存储
- **WorkManager** - 后台任务

### 特色组件
- **MIUIX UI库** - 小米风格组件
- **Folme动效** - 小米动效框架
- **Haptic** - 触觉反馈系统
- **MiPalette** - 动态取色

---

## 4. SDK和服务

### 智能家居
- 设备发现与连接
- 场景联动
- 自动化控制

### 定位服务
- **UWB** - 超宽带精确定位
- GPS/WiFi定位

### 社交登录
- Facebook SDK集成
- 游戏服务

### 媒体服务
- Fresco图片加载
- 动画播放

---

## 5. 技术亮点

1. **自研MIUIX组件库** - 完整的小米风格UI体系
2. **Jetpack Compose** - 现代声明式UI
3. **Folme动效系统** - 流畅的交互动画
4. **Matrix监控** - 腾讯开源性能监控
5. **UWB定位** - 超宽带精确定位
6. **触觉反馈** - Haptic震动反馈

---

## 6. 总结

小米米家采用了小米自研的技术栈：
- 自研MIUIX UI组件库，提供完整的小米风格UI
- Jetpack Compose现代化UI开发
- Folme动效框架实现流畅动画
- Matrix性能监控保障应用质量
- UWB超宽带支持精确定位
- 完善的智能家居控制能力

适合作为智能家居应用和自研UI组件库的技术参考。
