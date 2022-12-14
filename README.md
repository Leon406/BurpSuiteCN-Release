 **BurpSuite汉化发布, 翻译更新到 22.12.3 版本**



## 运行

### 一键启动(需要勾选自动启动auto start)

```
java -jar burpsuitloader-x.xx-all.jar
```

### keygen页面

```
java -jar burpsuitloader-x.xx-all.jar -r
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


## 文件日志及问题反馈

根目录下会生成log文件,未翻译的内容会写入日志, 如需翻译,请提issue 附上日志文件
任何翻译有问题,或者不准确的,请提issue反馈

debug版本同时会生成已翻译的日志



## 已知问题

翻译原理实现基于[BurpSuiteCn 汉化](https://github.com/funkyoummp/BurpSuiteCn) , 部分页面无法翻译,个人能力有限,未找到文本注入点,如果有师傅知道也请提issue告知。

以下是原作者找到的注入点

- java/awt/Frame#setTitle

- java/awt/Dialog#setTitle

- javax/swing/JLabel#setText

- javax/swing/AbstractButton#setText

- javax/swing/text/JTextComponent#setText

- javax/swing/text/PlainDocument#setTitle

- javax/swing/JComponent#setToolTipText

- javax/swing/text/PlainDocument#setTitle

- javax/swing/JComboBox#addItem

- javax/swing/JOptionPane#addTab

- javax/swing/JOptionPane#insertTab

- javax/swing/JDialog#JDialog

  
