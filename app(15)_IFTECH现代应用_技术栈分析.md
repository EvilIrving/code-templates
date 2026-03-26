# Compose+Hilt 现代应用 (IFTECH) 技术栈分析

## 应用基本信息
- **目录名**: base(15)
- **应用类型**: 现代化移动应用
- **签名**: IFTECH.RSA

---

## 1. 开发框架和技术平台

### 核心框架
- **原生 Android SDK** - 主框架
- **Kotlin** - 100%Kotlin开发
- **Jetpack Compose** - 声明式UI
- **Dagger Hilt** - 依赖注入

---

## 2. 第三方库和依赖

### Jetpack Compose全套
- androidx.compose.animation
- androidx.compose.foundation
- androidx.compose.material
- androidx.compose.material3
- androidx.compose.material-icons-core
- androidx.compose.runtime
- androidx.compose.ui

### Dagger Hilt依赖注入
- com.google.dagger_dagger
- com.google.dagger_hilt-android
- com.google.dagger_hilt-core
- androidx.hilt_hilt-navigation-compose
- androidx.hilt_hilt-navigation

### 图片加载 - Coil
- coil-core
- coil-compose
- coil-compose-core
- coil-network-core
- coil-network-okhttp

### 动画 - Lottie
- lottie-compose - Compose版Lottie

### 监控 - Sentry
- sentry-compose - 错误监控

### 网络
- **OkHttp** - HTTP客户端
- **Retrofit** - HTTP封装
- Logging Interceptor

### AndroidX 核心
- androidx.activity-compose
- androidx.fragment
- androidx.lifecycle
- androidx.navigation-compose
- androidx.room
- androidx.webkit

### 响应式
- **Kotlin Coroutines**
- **RxJava2** + RxKotlin
- **RxBinding** - UI绑定

### 自研模块
| 模块 | 用途 |
|------|------|
| app_backend | 后端交互 |
| conf | 配置管理 |
| database | 数据库 |
| defaultapi | 默认API |
| glide | 图片加载 |
| hybrid | H5混合 |
| image-conversion | 图片转换 |
| login_core | 登录核心 |
| model | 数据模型 |
| pay_core | 支付核心 |
| player | 播放器 |
| remote | 远程交互 |
| share_core | 分享核心 |
| share_weibo | 微博分享 |
| sso | 单点登录 |
| theme | 主题 |
| tracking | 埋点 |
| utils | 工具类 |
| widget | 组件 |

---

## 3. 核心组件和架构模式

### 架构设计
- **Clean Architecture** - 分层架构
- **MVVM** - ViewModel + Compose
- **依赖注入** - Hilt管理依赖

### 技术特点
- **声明式UI** - Jetpack Compose
- **导航** - Navigation Compose
- **协程** - 异步处理
- **Room** - 数据持久化

---

## 4. SDK和服务

### 登录/分享
- SSO单点登录
- 微博分享SDK

### 支付服务
- pay_core - 支付核心

### 媒体服务
- player - 视频播放
- image-conversion - 图片处理

### 监控服务
- Sentry错误监控
- tracking埋点

---

## 5. 技术亮点

1. **Jetpack Compose** - 全面采用声明式UI
2. **Dagger Hilt** - 标准依赖注入
3. **Coil** - Kotlin优先图片库
4. **Lottie Compose** - 声明式动画
5. **Navigation Compose** - 类型安全导航
6. **Sentry** - 企业级错误监控

---

## 6. 总结

该应用展示了最现代的Android技术栈：
- 100% Kotlin + Jetpack Compose
- Dagger Hilt依赖注入
- Coil图片加载
- Lottie动画
- Clean Architecture架构

是学习现代Android开发最佳实践的优秀参考。
