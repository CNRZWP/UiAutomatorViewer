### 说明
Fork自项目：https://github.com/cmlanche/uiautomatorviewer-standalone

### 改动
1. 移除标题中的作者信息
2. 替换窗口中的图标，解决大小不一致问题
3. 修改默认窗口大小，避免图标不展示

### 问题 (注意)
<font color='red'>**树形图中无法展示 resource-id 信息**</font>

### 打包
```mvn clean package```<br><br>
![编译过程](https://raw.githubusercontent.com/CNRZWP/blog-media/image/2022/202210022232166.png)
生成的 jar 文件位于：target/UiAutomatorViewer-2.0-all.jar

### 启动 (MacOS)
```java -XstartOnFirstThread -jar UiAutomatorViewer-2.0-all.jar```

### 源码
[谷歌官方](https://android.googlesource.com/platform/tools/swt/+/refs/heads/android10-release/uiautomatorviewer/)

### 依赖库
1. swt：https://download.eclipse.org/eclipse/downloads/drops4/I20200830-1800/#SWT
2. jface: 下载 [RCP Runtime Binary](https://download.eclipse.org/eclipse/downloads/drops4/I20200830-1800/)，解压后查找org.eclipse.core.commands_{version}.jar、org.eclipse.equinox.common_{version}.jar、org.eclipse.jface_{version}.jar
3. 额外依赖：
```xml
<dependency>
    <groupId>commons-io</groupId>
    <artifactId>commons-io</artifactId>
    <version>2.7</version>
</dependency>
```

### 预览
Java8 预览图
![UIAutomatorViewer-Java8](https://raw.githubusercontent.com/CNRZWP/blog-media/image/2022/202210022210039.png)
![UIAutomatorViewer-Java8](https://raw.githubusercontent.com/CNRZWP/blog-media/image/2022/202210022215951.png)
Java11 预览图
![UIAutomatorViewer-Java11](https://raw.githubusercontent.com/CNRZWP/blog-media/image/2022/202210022209452.png)
