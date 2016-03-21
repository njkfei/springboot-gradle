# springboot-gradle
本人的第一个gradle工程，抄自springboot官网，从今天开始，将转向基于gradle构建项目。
因此，这个项目虽然简单，但确是本人的一个里程碑。

## 关键配置
```
buildscript {
  repositories {
    maven { url "https://repo.spring.io/libs-release" }
    mavenLocal()
    mavenCentral()
  }
  dependencies {
    classpath("org.springframework.boot:spring-boot-gradle-plugin:1.1.10.RELEASE")
  }
}
apply plugin: 'java'
apply plugin: 'eclipse'
apply plugin: 'idea'
apply plugin: 'spring-boot'
jar {
  baseName = 'springbootgradle'
  version =  '0.1.0'
}
repositories {
  mavenLocal()
  mavenCentral()
  maven { url "https://repo.spring.io/libs-release" }
}
dependencies {
  compile("org.springframework.boot:spring-boot-starter-web")
  testCompile("junit:junit")
}
task wrapper(type: Wrapper) {
  gradleVersion = '2.2.1'
}
```
