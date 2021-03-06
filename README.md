# <img src="src/docs/asciidoc/images/spring-framework.png" width="80" height="80"> Spring Framework


鉴于开始准备看spring源码时，出现下载了代码但对gradle不熟悉导致导入IDEA后无法通过编译的情况

特意增加**一点调试备注**


下面步骤的源文档：[Build from Source](https://github.com/spring-projects/spring-framework/wiki/Build-from-Source) 以及 [import-into-idea.md.](https://github.com/spring-projects/spring-framework/blob/master/import-into-idea.md)

源代码clone到本地后

编译

    cd spring-framework
    ./gradlew build
    #等待执行完成，如果网速不好会非常痛苦，因为要下载gradle还要下载很多jar

导入IDEA

    Within your locally cloned spring-framework working directory:
    
    * 使用 ./gradlew :spring-oxm:compileTestJava 命令预编译spring-oxm
    * 打开IDEA (File -> New -> Project from Existing Sources -> 进入指定目录 -> 选择 build.gradle 确定导入)
    * 基本上等导入完成就可以了
    
源码调试简单指引：

    到每个模块下的test目录，有非常健全的单元测试类

### Spring-beans(也就核心的IOC)
    
1. 从BeanFactoryUtilsTests开始调试一步步看，了解简单IOC容器
2. 看完再把ClassPathXmlApplicationContextTests大致看一下，了解上下文以及各种事件注册机制
3. 再稍微看看注解加载模式

### Spring-aop

1. 把ProxyFactoryTests稍微看一下，编程式AOP
2. 详细看一遍ProxyFactoryBeanTests，声明式AOP，IOC容器加载与FactoryBean结合的实现   


This is the home of the Spring Framework: the foundation for all [Spring projects](https://spring.io/projects). Collectively the Spring Framework and the family of Spring projects is often referred to simply as "Spring". 

Spring provides everything required beyond the Java programming language for creating enterprise applications for a wide range of scenarios and architectures. Please read the [Overview](https://docs.spring.io/spring/docs/current/spring-framework-reference/overview.html#spring-introduction) section as reference for a more complete introduction.

## Code of Conduct

This project is governed by the [Spring Code of Conduct](CODE_OF_CONDUCT.adoc). By participating, you are expected to uphold this code of conduct. Please report unacceptable behavior to spring-code-of-conduct@pivotal.io.

## Access to Binaries

For access to artifacts or a distribution zip, see the [Spring Framework Artifacts](https://github.com/spring-projects/spring-framework/wiki/Spring-Framework-Artifacts) wiki page.

## Documentation

The Spring Framework maintains reference documentation ([published](http://docs.spring.io/spring-framework/docs/current/spring-framework-reference/) and [source](src/docs/asciidoc)), Github [wiki pages](https://github.com/spring-projects/spring-framework/wiki), and an
[API reference](http://docs.spring.io/spring-framework/docs/current/javadoc-api/). There are also [guides and tutorials](https://spring.io/guides) across Spring projects.

## Build from Source

See the [Build from Source](https://github.com/spring-projects/spring-framework/wiki/Build-from-Source) Wikipedia page and the [CONTRIBUTING.md](CONTRIBUTING.md) file.

## Stay in Touch

Follow [@SpringCentral](https://twitter.com/springcentral), [@SpringFramework](https://twitter.com/springframework), and its [team members](https://twitter.com/springframework/lists/team/members) on Twitter. In-depth articles can be found at [The Spring Blog](http://spring.io/blog/), and releases are announced via our [news feed](http://spring.io/blog/category/news).

## License

The Spring Framework is released under version 2.0 of the [Apache License](http://www.apache.org/licenses/LICENSE-2.0).
