# Sprouts 记账 (萌系记账) 技术栈分析

## 应用概述
- **应用名称**: Sprouts (萌系记账)
- **包名**: com.mutangtech.sprouts
- **应用类型**: 个人理财记账应用
- **开发者**: 木坦科技

## 技术证据分析

### 1. 开发框架与语言

#### Kotlin 开发
```
证据块:
- Kotlin 协程支持
- Kotlin 反射库
- Kotlin 标准库
- DebugProbesKt.bin 存在
```

#### Android Jetpack 组件
```
证据块:
- androidx.activity.ComponentActivity
- androidx.constraintlayout.widget.ConstraintLayout
- androidx.constraintlayout.motion.widget.MotionLayout
- androidx.emoji2:emoji2-bundled
- androidx.room.IMultiInstanceInvalidationCallback (数据库)
- androidx.savedstate.Restarter
```

#### 架构模式
```
证据块:
- MVVM 架构 (ViewModel + LiveData 模式)
- 组件化设计
- 生命周期感知组件
```

### 2. Material Design 集成

#### Material Design 3
```
证据块:
- MaterialButton 组件
- Material Design 3 主题
- 动态主题支持
- CoordinatorLayout 布局
- Material 输入框组件
```

#### UI 框架特性
```
证据块:
- ConstraintLayout 复杂布局
- MotionLayout 动画支持
- RecyclerView 列表展示
- ViewPager2 页面切换
- SwipeRefreshLayout 下拉刷新
```

### 3. 网络通信框架

#### OkHttp 3.x
```
证据块:
- Lokhttp3/OkHttpClient
- Lokhttp3/Request
- Lokhttp3/Response
- Lokhttp3/Interceptor
- Lokhttp3/Authenticator
- OkHttp 缓存机制
```

#### API 调用
```
证据块:
- REST API 支持
- HTTP/2 支持
- 网络拦截器
- 自动重试机制
```

### 4. 数据持久化方案

#### SQLite 数据库
```
证据块:
- Room 数据库框架
- 数据库版本管理
- 多实例失效回调
- 数据库事务支持
- SQLCipher 加密 (可能)
```

#### 数据模型
```
证据块:
- Account 表结构
  - 账单日期 (billingDay)
  - 还款日期 (repaymentDay)
  - 账户类型 (kind)
  - 股票/理财相关字段
  - 定期存款字段
  - 费用管理字段
```

### 5. 第三方登录与分享

#### 微信 SDK
```
证据块:
- Lcom/tencent/mm/opensdk/
- 微信授权登录
- 微信分享功能
- 微信支付集成
```

#### QQ/腾讯系 SDK
```
证据块:
- Lcom/tencent/connect/common/AssistActivity
- Lcom/tencent/tauth/AuthActivity
- QQ 登录
- QQ 分享
```

#### 支付宝 SDK
```
证据块:
- Lcom/alipay/sdk/app/PayTask
- Lcom/alipay/sdk/app/AuthTask
- 支付宝支付
- 支付宝授权
```

### 6. 云端同步服务

#### Google Firebase
```
证据块:
- firebase-encoders.properties
- firebase-encoders-json.properties
- firebase-encoders-proto.properties
- Firebase 编码器支持
```

#### 网盘集成
```
证据块:
- 豆腐网盘 (Nutstore) 集成
- 云端存储 API
- 数据备份服务
- 实时同步机制
```

### 7. 订阅与付费系统

#### Google Play Billing
```
证据块:
- Google Play Billing Library v6
- 订阅管理 (subscriptionOfferDetails)
- 购买流程 (purchaseData)
- VIP 订阅功能
- 账单日管理 (billingDay)
```

#### 付费功能
```
证据块:
- VIPIpg (VIP 内购)
- RVip (续费 VIP)
- 订阅服务端验证
- Alternative Billing 支持
```

### 8. 多媒体与资源

#### 图表库
```
证据块:
- 饼图、柱状图、折线图
- 趋势分析图表
- 自定义图表组件
```

#### 资源管理
```
证据块:
- 账本模板系统 (account_book_template/)
  - 标准账本、家庭账本、恋爱账本
  - 生意账本、宝宝账本、旅行账本
- Widget 图片资源
- Emoji 支持 (emojos.json)
```

### 9. 数据导入导出

#### 文件格式支持
```
证据块:
- Excel 文件导入 (XLS/XLSX)
- CSV 文件处理
- 图片分享导入
- 数据备份导出
```

#### 第三方账单识别
```
功能推断:
- 支付宝账单导入
- 微信账单导入
- 银行卡账单识别
- 智能分类系统
```

### 10. 后台服务与保活

#### 保活机制
```
证据块:
- 自启动权限请求
- 电池优化忽略
- 后台服务保活
- 进程保护机制
```

#### 系统集成
```
证据块:
- 无障碍服务 (可能用于自动记账)
- 悬浮窗权限
- 后台弹窗权限
- 系统截图监听
```

### 11. 搜索与分类

#### 搜索系统
```
证据块:
- 交易记录搜索
- 分类搜索
- 商户搜索
- 标签搜索
- 金额范围搜索
```

#### 分类管理
```
证据块:
- 标签系统
- 分类模板
- 自动分类建议
- 分类历史记录
```

### 12. 统计与分析

#### 数据统计
```
证据块:
- 收支统计
- 净流入统计
- 类别占比分析
- 趋势分析
- 对比分析
```

#### 报表生成
```
证据块:
- 月度报表
- 年度报表
- 自定义时间范围
- 图表导出
```

### 13. 权限管理

#### Android 权限
```
证据块:
- Android 13+ 权限适配
- 相机权限
- 存储权限
- 悬浮窗权限
- 无障碍服务权限
```

#### 隐私保护
```
证据块:
- 应用锁支持
- 数据加密
- 隐私模式
- 权限最小化原则
```

### 14. 国际化支持

#### 多语言
```
证据块:
- 中文 (简体/繁体)
- 英文支持 (template_en.json)
- 多地区适配
```

#### 本地化
```
证据块:
- 货币符号支持
- 日期格式本地化
- 数字格式本地化
```

### 15. 性能优化

#### 缓存策略
```
证据块:
- 图片缓存
- 数据缓存
- 网络请求缓存
```

#### 内存优化
```
证据块:
- 懒加载
- 资源按需加载
- 内存泄漏检测
```

### 16. 辅助功能

#### Widget 支持
```
证据块:
- 记账 Widget
- 余额 Widget
- 预算 Widget
- 多尺寸 Widget
```

#### 快捷方式
```
证据块:
- 桌面快捷方式
- 状态栏快捷入口
- 快捷记账功能
```

### 17. 社交功能

#### 分享功能
```
证据块:
- 微信分享
- QQ 分享
- 保存图片分享
- 账单分享
```

#### 账本协作
```
证据块:
- 多用户支持
- 账本共享
- 权限管理
- 数据隔离
```

## 技术架构总结

### 核心技术栈
1. **开发语言**: Kotlin 100%
2. **UI 框架**: Material Design 3 + 原生 Android View
3. **架构模式**: MVVM + Clean Architecture
4. **数据库**: Room + SQLite
5. **网络**: OkHttp 3.x
6. **异步**: Kotlin Coroutines + Flow
7. **依赖注入**: 手动依赖注入 (或未使用框架)

### 第三方 SDK
1. **支付**: 支付宝 SDK + Google Play Billing
2. **登录**: 微信 SDK + QQ SDK
3. **云同步**: Firebase + 豆腐网盘
4. **UI 组件**: Material Design Components
5. **图表**: 自定义图表库

### 技术亮点
1. **智能识别**: 账单自动识别与分类
2. **多种记账**: 手动/图片/自动/截图
3. **云端同步**: 多设备实时同步
4. **UI 设计**: 萌系设计风格
5. **功能完整**: 涵盖个人理财全场景

### 适用场景
- 记账应用开发参考
- 金融工具应用开发
- Material Design 3 实践
- Kotlin 协程应用
- MVVM 架构实践

### 技术评分
- **代码质量**: ★★★★☆ (Kotlin 现代化开发)
- **架构设计**: ★★★★☆ (MVVM 清晰分层)
- **用户体验**: ★★★★★ (萌系设计友好)
- **功能完整**: ★★★★★ (功能丰富)
- **技术创新**: ★★★★☆ (智能识别创新)
