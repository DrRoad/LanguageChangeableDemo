# LanguageChangeableDemo
### 多语言国际化支持库，暂只支持中英文切换，简单易用，无额外其他库依赖，修改可本地存储固化，无需重启

## 集成方式

[![](https://jitpack.io/v/feisher/LanguageChangeableDemo.svg)](https://jitpack.io/#feisher/LanguageChangeableDemo)

#### 1.在你的项目根目录 build.gradle 结尾添加(Add it in your root build.gradle at the end of repositories):
```groovy
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
#### 2. 在modle的gradle中添加依赖
```groovy
dependencies {
	        implementation 'com.github.feisher:LanguageChangeableDemo:1.0.0'
    		//注意上面jitpack版本号，
	}
```

默认实现了`Textview`和`Button`,直接使用`TextView2`或`Button2`即可， 其他控件需要实现`LangChangableView` 接口，

内部方法实现拷贝`TextView2`中的即可 使用前必须在`Application`中初始化
```java
CLang.init(this);
```
亦可指定语言环境使用 
```java
CLang.init(this, Locale.CHINA); 
```
初始化 需要修改语言的时候
```java
CLang.swithLang(context);
```
即可，语言环境会使用`SharedPreferences`存储到本地

![演示图](https://github.com/feisher/LanguageChangeableDemo/blob/master/device-2019-03-05-105142.gif?raw=true)

## PS:注意事项

#### 为了简化流程默认 以 values/strings.xml 文件作为英文文件  以   values-zh/strings.xml 作为中文文件，，具体操作可参考demo





#### 问题

发现bug或好的建议欢迎 [issues](https://github.com/feisher/LanguageChangeableDemo/issues) or Email 458079442@qq.com

#### 微信交流

![微信](https://github.com/feisher/LanguageChangeableDemo/blob/master/97af74c179108dc703cf3535de8b73b3.png?raw=true)
