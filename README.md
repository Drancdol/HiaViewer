# Herpy Image Viewer

Herpy Image Archive 的移动端浏览应用

## 开发环境

- Node.js 22.11 或更高版本
- Android Studio 或 Xcode，以及对应的 React Native 开发环境

## 运行

安装 JavaScript 依赖：

```sh
npm install
```

启动 Metro：

```sh
npm start
```

在 Android 设备或模拟器上运行：

```sh
npm run android
```

在 iOS 模拟器上运行：

```sh
bundle install
bundle exec pod install --project-directory=ios
npm run ios
```

## 常用命令

```sh
npm run lint
npm test
```

## 国内依赖下载慢/失败解决方案
```npm i 后 根目录运行
find node_modules/ -type f \( -name "*.kts" -o -name "*.gradle" \) -exec sed -i 's|mavenCentral()|maven { url = uri("https://maven.aliyun.com/repository/central") }\n    maven { url = uri("https://maven.aliyun.com/repository/public") }\n    maven { url = uri("https://maven.aliyun.com/repository/google") }\n    maven { url = uri("https://maven.aliyun.com/repository/gradle-plugin") }\n    maven { url = uri("https://maven.aliyun.com/repository/jcenter") }\n    mavenCentral()|g' {} +
```
```如果依旧有依赖下载失败，那就到对应的包里修改build.gradle，给repositories添加国内镜像为优先
```