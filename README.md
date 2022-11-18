 **BurpSuite汉化发布, 翻译更新到 22.11.1 版本**



## 运行

### 一键启动(需要勾选自动启动auto start)

```
java -jar burpsuitloader-x.xx-all.jar
```

### keygen页面

```
java -jar burpsuitloader-x.xx-all.jar -r
```



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

  
