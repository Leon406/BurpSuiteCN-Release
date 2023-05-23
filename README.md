 


<p align="center">
<a href="https://github.com/Leon406/BurpSuiteCN-Release/releases/latest"><img src="https://img.shields.io/github/release/Leon406/BurpSuiteCN-Release.svg"/></a>
<img src="https://img.shields.io/github/downloads/Leon406/BurpSuiteCN-Release/total"/>
</p>

<h4 align="center">Visitors :eyes:</h4>

<p align="center"><img src="https://profile-counter.glitch.me/Leon406_BurpSuiteCN-Release/count.svg" alt="BurpSuiteCN-Release :: Visitor's Count" />
 <img width=0 height=0 src="https://profile-counter.glitch.me/Leon406/count.svg" alt="Leon406:: Visitor's Count" />

</p>
BurpSuite汉化发布   如果有用请star,这是支持我更新的最大的动力.

**3.5.20 翻译更新到 2023.5.1 版本**
 支持外置多个cn*.txt文件翻译,优化不翻译白名单,兼容插件
 
**3.3.23 翻译更新到 2023.3.2 版本**
 修复翻译错误,及Target过滤显示问题
 
 **3.1.16 翻译更新到 2023.1 版本**
 此版本修改较多,新增368个翻译,3个白名单规则.



## 如何使用 (选择一种即可)

### 一键启动(需要勾选自动启动auto start)

```
java -jar burpsuitloader-x.xx-all.jar
```

### keygen页面 (按需勾选loader,汉化,一键启动)

```
java -jar burpsuitloader-x.xx-all.jar -r
```


### java agent配置方式(如果一键启用有问题的,建议采用这种方式)


```
// loader + 汉化
%JAVA_HOME%/bin/java -javaagent:burpsuitloader-x.xx-all.jar=loader,han   -jar burpsuite_pro_v20xx.jar

// 仅汉化,loader失效
%JAVA_HOME%/bin/java -javaagent:burpsuitloader-x.xx-all.jar=han   -jar burpsuite_pro_v20xx.jar

```

### 版本命名

[A]A.BB.CC[.DD]

- AA  年份减去2020, 2022为 2
- BB 月份
- CC 修改日期
- DD 可选,小版本号,如有从1开始



如 2.11.19 为2022-11-19 构建发布的第一个版本



### 外置文件(按需手动创建)

- debug文件或者文件夹  

  打开调试日志,写入已翻译文本到log目录

- white.txt   不翻译白名单,支持正则, 注释行以#开头

- cn.txt   翻译内容 ,支持正则,可覆盖默认内容,分隔符为Tab键, 注释行以#开头
- cn*.txt  支持多个文件,插件翻译内容 ,支持正则,可覆盖默认内容,分隔符为Tab键, 注释行以#开头


## 文件日志及问题反馈

根目录下会生成log文件,未翻译的内容会写入日志, 如需翻译,请提issue 附上日志文件
任何翻译有问题,或者不准确的,请提issue反馈

debug版本同时会生成已翻译的日志



## 已知问题

翻译原理实现基于[BurpSuiteCn 汉化](https://github.com/funkyoummp/BurpSuiteCn) , 部分页面无法翻译,个人能力有限,未找到文本注入点,如果有师傅知道也请提issue告知。

目前发现新版本设置树状菜单内容无法翻译


以下是原作者找到的注入点

- java/awt/Frame#setTitle

- java/awt/Dialog#setTitle

- javax/swing/JLabel#setText

- javax/swing/AbstractButton#setText

- javax/swing/text/JTextComponent#setText

- javax/swing/text/PlainDocument#insertString  ==> javax/swing/text/AbstractDocument#insertString  参考 [Belle](https://github.com/ankokuty/Belle)

- javax/swing/JComponent#setToolTipText

- javax/swing/text/PlainDocument#setTitle

- javax/swing/JComboBox#addItem

- javax/swing/JOptionPane#addTab

- javax/swing/JOptionPane#insertTab

- javax/swing/JDialog#JDialog

  
