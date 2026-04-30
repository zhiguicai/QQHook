## 如何同步QQHook

android studio 2025.3.1

1：删除gradle-daemon-jvm.properties 文件
2：重启android stdio
3: File -> Settings -> Build, Execution, Deployment -> Build Tools -> Gradle，在 “Gradle JDK” 下拉框中选择你本地安装的 JDK 21。
4: 同步项目
5：打开项目根目录下的 gradle/libs.versions.toml 或根目录下的 build.gradle.kts
//AGP 9.1.0 版本，则需要将 IDE 升级到 Panda 4 (2025.3.4) 或更新版本，因为这些版本的 AGP 支持上限已提升至 9.2
agp = "9.0.0"   // 将 `9.1.0` 修改为 `9.0.0`

6:打开终端（命令行），进入项目根目录 D:\czg\czgAsFwgs\Swkj\QQHook，运行：
~~~
# qqstub 目录实际上是一个 Git Submodule（子模块），目前没有被拉取下来，所以里面是空的，导致 Gradle 找不到构建文件
git submodule update --init --recursive

~~~