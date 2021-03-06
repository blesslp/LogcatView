# LogcatView [![](https://www.jitpack.io/v/huangdali/LogcatView.svg)](https://www.jitpack.io/#huangdali/LogcatView)

日志记录抓取

> 没有数据线的时候，就用这个输出日志吧

- 使用简单，一行代码搞定
- 点击链接可以用浏览器打开
- 可抓取大部分Android Studio中Logcat打印的内容
- 可以搜索内容
- 可按tag过滤
- 可根据日志等级筛选（提供隐藏方法）
    - **A**  所有内容
    - **O**  System.out 输出的内容
    - **W**  警告级别的内容
    - **E**  错误级别的内容

## 集成

### Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:

```java
allprojects {
    repositories {
        ...
        maven { url 'https://www.jitpack.io' }
    }
}
```

### Step 2. Add the dependency

```java
dependencies {
        compile 'com.github.huangdali:LogcatView:v1.1.2'
}
```

### 使用
```java
    new LogcatDialog(this).show();
```

## 效果图
![](https://github.com/huangdali/LogcatView/blob/master/all.png)


![](https://github.com/huangdali/LogcatView/blob/master/search.png)

## 版本记录

v1.1.2 ([2017.10.09]())

- 【优化】更精确的网页链接判断
- 【优化】链接颜色使用默认值

v1.0.9 ([2017.10.09]())

- 【新增】内容中有web链接的可点击用浏览器打开

v1.0.8 ([2017.10.09]())

- 【新增】重写有两个参数的构造方法

v1.0.5 ([2017.09.30]())

- 【新增】项目初始化

## 关于样式

【**如果你的activity继承至AppCompatActivity，请跳过此步骤**】如果你的Activity不是继承至AppCompatActivity，那么样式可能会很丑，可以通过下面的设置：


### 1、在style.xml中定义
```java
  <style name="Translucent_NoTitle" parent="android:style/Theme.Dialog">
        <item name="android:background">#00000000</item> <!-- 设置自定义布局的背景透明 -->
        <item name="android:windowBackground">@android:color/transparent</item>  <!-- 设置window背景透明，也就是去边框 -->
  </style>
```

### 2、设置主题

```java
  LogcatDialog logcatDialog = new LogcatDialog(mContext,R.style.Translucent_NoTitle);
  logcatDialog.show();
```

