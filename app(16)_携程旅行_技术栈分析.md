# 携程旅行 技术栈分析

## 应用基本信息
- **目录名**: base(16)
- **应用类型**: OTA旅游服务应用
- **签名**: CTRIP.RSA

---

## 1. 开发框架和技术平台

### 多框架混合架构
- **原生 Android SDK** - 主框架
- **React Native** - 跨平台模块
- **Flutter** (ctflutter) - 新业务模块
- **Kotlin Multiplatform (KMP)** - 跨平台业务逻辑

### KMP 模块
| 模块 | 用途 |
|------|------|
| KMPFoundation | 基础能力 |
| KMPNetwork | 网络层 |
| KMPService | 服务层 |
| KMPFlightBusiness | 机票业务 |
| KMPFlightCity | 机票城市 |
| KMPFlightCore | 机票核心 |

---

## 2. 第三方库和依赖

### 业务模块
| 模块 | 用途 |
|------|------|
| CTFlight | 机票 |
| CTHotel | 酒店 |
| CTTrain | 火车票 |
| CTTour | 跟团游 |
| CTSchedule | 行程 |
| CTDestinationMain | 目的地 |
| CTDestinationStory | 游记 |
| CTDestVideoEdit | 视频编辑 |
| CTLiveStream | 直播 |
| CTPublicContent | 公共内容 |
| CTPublicProduct | 公共产品 |
| CTWenDao | 问答 |
| CTMarket | 营销 |
| CTMyCtrip | 我的携程 |
| CTLogin | 登录 |
| CTHybrid | H5混合 |
| CTService | 服务 |

### 支付模块
| 模块 | 用途 |
|------|------|
| CTPayBase | 支付基础 |
| CTPayBusiness | 支付业务 |
| CTPayFoundation | 支付底层 |
| CTPayVerify | 支付验证 |
| CTPayFacekit | 人脸支付 |
| trippay | 携程支付SDK |

### 技术基础设施
| 模块 | 用途 |
|------|------|
| CTAD | 广告 |
| CTAI | AI能力 |
| CTAutoEventCollect | 自动埋点 |
| CTBaseBusinessUI | 基础业务UI |
| CTDynamicLoad | 动态加载 |

### 数据序列化
- **Kotlinx Serialization** - Kotlin序列化
  - serialization-core
  - serialization-json
  - serialization-protobuf
- **Wire Runtime** - Protocol Buffers

### 存储
- **MMKV** (mmkv-kotlin) - 高性能KV存储
- **SQLlin** - Kotlin SQL DSL
  - sqllin-driver
  - sqllin-dsl

### 监控
- **KOOM** (koom-monitor-base) - 内存监控
- **Shark** - LeakCanary内存泄漏检测
- **DataReport** - 数据上报

### 图片加载
- **Fresco** - Facebook图片库
  - fbcore
  - animated-drawable
  - middleware

### 广告/营销
- **adlibc** - 广告库
- **market-oaid** - OAID获取
- **market-referrer** - 渠道归因

### AndroidX 核心
- androidx.activity
- androidx.camera
- androidx.lifecycle
- androidx.profileinstaller
- androidx.recyclerview
- androidx.sqlite
- androidx.startup
- androidx.webkit
- androidx.window

### 异步处理
- **Kotlin Coroutines**
  - kotlinx_coroutines_android
  - kotlinx_coroutines_core

---

## 3. 核心组件和架构模式

### 架构设计
- **三端混合架构** - Native + React Native + Flutter
- **KMP跨平台** - 共享业务逻辑
- **模块化架构** - 业务模块独立
- **动态加载** - CTDynamicLoad支持

### 技术组件
- **Lite State Store** - 轻量状态管理
- **Logcat** - 日志系统
- **Renderer** - 渲染层

---

## 4. SDK和服务

### 相机服务
- androidx.camera_camera-camera2
- androidx.camera_camera-core
- androidx.camera_camera-lifecycle
- androidx.camera_camera-view

### 多媒体
- 直播组件 (CTLiveStream)
- 视频编辑 (CTDestVideoEdit)
- 媒体工具 (CTMediaToolsLib)

### 城市选择
- CTCitySelectorLib - 城市选择器

---

## 5. 技术亮点

1. **三端混合架构** - Native + RN + Flutter共存
2. **Kotlin Multiplatform** - 跨平台业务逻辑共享
3. **完整的OTA业务覆盖** - 机酒火车跟团等全业务线
4. **动态化能力** - 支持动态加载
5. **企业级监控** - KOOM内存监控
6. **人脸支付** - CTPayFacekit

---

## 6. 总结

携程旅行采用了复杂的多框架混合架构：
- Native + React Native + Flutter三端并存
- Kotlin Multiplatform实现跨平台业务逻辑
- 完整的OTA业务模块化设计
- 强大的支付和AI能力
- 企业级性能监控体系

适合作为大型复杂业务应用的架构参考，展示了如何在同一应用中整合多种技术栈。
