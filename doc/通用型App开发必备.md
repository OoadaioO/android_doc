# 通用型App开发必备
#### 1.	框架搭建：
1. 整体框架，使用MVP或MVVM架构实现App整体骨架搭建。
2. UI部分，使用FrammentTabHost实现整体UI框架，使用ActionBar实现各个页面导航栏，使用DrawerLayout实现侧边栏，使用RecyclerView和ultra-ptr实现下拉刷新列表。

#### 2.	分包策略：
按照组件类型来分包，而不是按业务模块来分包，对于稍微大一点的项目，可以先按模块分包，在子模块中再按照组件类型分包。

#### 3.	引入必备开源项目：
1. ButterKnife、Dagger2（View注入框架，依赖注入框架）
2. Realm（数据库框架，比传统SQLite性能好很多，不过目前还有不少限制）
3. RxJava + Retrofit + OkHttp（网络请求相关框架）
4. Fresco（网络图片加载，内存优化的比较好）
5. RecyclerView + ultra-ptr （下拉刷新列表，可以完全替代ListView和GridView）
6. LeekCanary、BlockCanary（内存泄露检测，UI卡顿检测）
7. Stetho（调试工具，用来查看网络请求数据包和数据库）
8. RocooFix（热修复技术）