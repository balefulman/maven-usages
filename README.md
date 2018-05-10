# maven-usages
maven使用

## mvn参数
1.  -v 版本
2.  compile 编译
3.  test 测试
4.  package 打包
5.  clean 清除 target
6.  install 安装jar包到本地仓库
## archetype 自动创建目录结构
 1. mvn archetype:generate 交互创建
 2. mvn archetype:generate -DgroupId=组织名,公司网址反写,项目名 -DartifactId=项目名-模块名 -Dversion=版本号 -Dpackage=代码所存放的包名.例子: `mvn archetype:generate -DgroupId="imooc-arthur" -DartifactId="spring-mvc-study" -DarchetypeArtifactId="maven-archetype-webapp"`
## 仓库
* 本地仓库
* 远程仓库
## 线上搜索库
* [https://repo.maven.apache.org/maven2](https://repo.maven.apache.org/maven2)
* [http://search.maven.org/](http://search.maven.org/)
## 镜像仓库
  conf目录下的 settings.xml 添加下代码
  
      <mirror>
        <id>maven.net.cn</id>
        <mirrorOf>central</mirrorOf> *
        <name>central mirror in china</name>
        <url>http://maven.net.cn/content/groups/public</url>
      </mirror>
   官方推荐
   
      <mirrors>
        <mirror>
          <id>UK</id>
          <name>UK Central</name>
          <url>http://uk.maven.org/maven2</url>
          <mirrorOf>central</mirrorOf>
        </mirror>
      </mirrors>
      
修改仓库默认路径
  conf目录下的 settings.xml
  
    <localRepository>C:/m2repo</localRepository>

## 完整的项目构建过程:
  清理 编译 测试 打包 集成测试 验证 部署

## maven 生命周期
* clean 清理项目
* dafault 构建项目
* site  生成项目站点

