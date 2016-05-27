# Gradle Tutorial
## What Gradle
Gradle 是一个自动化和支持多语言的构建工具，你可以构建测试、发布、部署到一个平台。Gradle 支持的语言Java, Scala, Android, C/C++, and Groovy。和目前的开发工具也有很好的集成 Eclipse, IntelliJ, and Jenkins。也支持plugin功能。
## Using Gradle
* Gradle 构建项目基于build.gradle文件,如下所示

```
// 引入java插件
apply plugin: 'java'
// 配置全局属性，下面表示不要导入spring-boot-starter-tomcat模块
configurations {
    compile.exclude module: "spring-boot-starter-tomcat"
}
// 引入依赖的jar包
dependencies {
	compile("jar-group:jar-name:jar-version")
}
// 自定义的task
task myTask(type: xxx){
}
```
* 执行构建

```
gradle clean - Deletes the build directory.
gradle build - Assembles and tests this project.
gradle check - Runs all checks.
gradle test - Runs the unit tests.
```
## Gradle Command
* gradle \<task\>
* gradle tasks
* gradle --help
* gradle help --task <task>


