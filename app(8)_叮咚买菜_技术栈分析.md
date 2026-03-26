# 叮咚买菜 (React Native电商应用) 技术栈分析

## 应用基本信息
- **目录名**: base(8)
- **应用类型**: 电商/生鲜配送应用
- **签名**: ZONE.RSA
- **原生库数量**: 102个 (arm64-v8a)

---

## 1. 开发框架和技术平台

### 核心框架
- **React Native** - 跨平台开发框架
- **Hermes** - Facebook高性能JS引擎
- **原生 Android SDK** - Native模块
- **Kotlin** - 原生开发语言

### React Native 核心组件
| 库名 | 用途 |
|------|------|
| libreactnativejni.so | RN核心JNI |
| libhermes.so | Hermes JS引擎 |
| libjsi.so | JS Interface |
| libreanimated.so | Reanimated动画 |
| libreact_render_*.so | Fabric渲染引擎 |
| librrc_*.so | RN核心组件 |

---

## 2. 第三方库和依赖

### React Native 生态
- **react-native-gesture-handler** - 手势处理
- **react-native-pager-view** - 分页视图
- **react-native-webview** - WebView组件
- **flash-list** - 高性能列表

### 音视频/多媒体
- **腾讯LiteAVSDK** (libliteavsdk.so 11MB) - 音视频SDK
- **百度语音SDK** (libBaiduSpeechSDK.so) - 语音识别
- **FFmpeg** (libtxffmpeg.so) - 音视频编解码
- **SoundTouch** (libtxsoundtouch.so) - 音频处理
- **SVGA** (com.opensource.svgaplayer) - 动画播放

### 图片处理
- **Fresco** (libimagepipeline.so) - Facebook图片库
- **Glide WebP** (libglide-webp.so) - WebP支持
- **GIF** (libgifimage.so, libpl_droidsonroids_gif.so) - GIF支持

### AI/ML
- **TensorFlow Lite** (libtensorflowlite_jni.so) - 机器学习
- **GPU Delegate** (libtensorflowlite_gpu_jni.so) - GPU加速
- **Task Vision** (libtask_vision_jni.so) - 视觉任务

### 网络与存储
- **OkHttp** - HTTP客户端
- **MMKV** (libmmkv.so) - 高性能KV存储
- **TQUIC** (libtquic_jni.so) - QUIC协议

### 监控与调试
- **Bugly** - 腾讯崩溃监控
  - libBugly.so
  - libBugly_Native.so
  - libbugly_dumper.so
  - libbuglybacktrace.so
- **Shark** - 内存泄漏检测 (LeakCanary)

### 推送服务 (全平台覆盖)
- push-core - 推送核心
- push-honor - 荣耀推送
- push-huawei - 华为推送
- push-oppo - OPPO推送
- push-vivo - vivo推送
- push-xiaomi - 小米推送

### AndroidX 核心
- androidx.activity
- androidx.camera (相机功能)
- androidx.databinding
- androidx.datastore
- androidx.lifecycle
- androidx.navigation
- androidx.paging
- androidx.room
- androidx.work

### 业务模块
| 模块 | 用途 |
|------|------|
| home | 首页 |
| cart | 购物车 |
| category | 分类 |
| order | 订单 |
| search | 搜索 |
| productdetail | 商品详情 |
| pay | 支付 |
| login | 登录 |
| settings | 设置 |
| aichat | AI聊天 |
| speech | 语音功能 |

---

## 3. 核心组件和架构模式

### 架构设计
- **React Native + Native混合** - 跨平台+原生
- **模块化架构** - 业务模块分离
- **路由系统** (ddlrouter) - 模块间导航

### 技术亮点
- **Hermes引擎** - 优化启动和运行性能
- **Fabric渲染器** - 新一代RN渲染架构
- **TurboModules** - 优化Native模块调用

### 安全相关
- libclient-encrypt.so - 客户端加密
- libmsaoaidauth.so - OAID认证
- libmsaoaidsec.so - OAID安全

---

## 4. SDK和服务

### 支付SDK
- **抖音支付** (dy-pay-sdk)
- 微信支付/支付宝 (通过Native模块)

### 视频直播
- **腾讯超级播放器** (superplayerkit)
- 短视频组件 (shortvideo)
- 直播组件 (topvideo)

### 数据服务
- **DataStore** - 数据存储
- **Room** - 数据库
- **MMKV** - 高性能KV

### 网络诊断
- netdiagnostics - 网络诊断工具

---

## 5. 技术亮点

1. **React Native新架构** - 使用Hermes+Fabric+TurboModules
2. **完整的推送覆盖** - 支持6大厂商推送
3. **AI集成** - TensorFlow Lite机器学习
4. **语音识别** - 百度语音SDK
5. **高性能视频** - 腾讯LiteAVSDK
6. **企业级监控** - Bugly崩溃监控

---

## 6. 原生库清单 (部分)

### React Native相关
```
libreactnativejni.so (814KB)
libhermes.so (2.4MB)
libreanimated.so (890KB)
libfabricjni.so (990KB)
```

### 多媒体相关
```
libliteavsdk.so (11MB) - 腾讯音视频
libBaiduSpeechSDK.so (1.1MB) - 百度语音
libtxffmpeg.so (2.5MB) - FFmpeg
```

### AI相关
```
libtensorflowlite_jni.so (3.2MB)
libtensorflowlite_gpu_jni.so (3.2MB)
libtask_vision_jni.so (6.7MB)
```

---

## 7. 总结

叮咚买菜采用React Native跨平台方案，具有以下特点：
- 采用RN新架构 (Hermes + Fabric)
- 丰富的原生能力扩展
- AI/ML功能集成
- 完整的推送服务覆盖
- 企业级音视频能力
- 高度模块化的业务架构

适合作为大型React Native电商应用的技术选型参考。
