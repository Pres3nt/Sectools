# Xray_1.9.11高级版+Xray批量主动扫描

## 简述

1. 在pppXray大佬实现Xray批量主动扫描的基础上修改脚本实现扫描时是否开启爬虫功能
2. Xray_1.9.11社区版的高级版（破解版）



## 1.配置环境

```python
pip install -r requirements.txt
```



## 2.批量扫描时是否开启爬虫

在对站点进行批量扫描时，修改pppXray.py脚本中红框部分命令，实现爬虫功能的开启/关闭

```py
#扫描URL，不使用爬虫
xray.exe webscan {} --url {} --html-output {}\\{}.html

#扫描URL，使用爬虫，并且对爬虫爬取的页面进行扫描
xray.exe webscan {} --basic-crawler {} --html-output {}\\{}.html
```

![9e1891ed-e4a6-4ca9-83f2-e5f3ba067ab8](D:\Tools\Xray\xray_1.9.11\images\9e1891ed-e4a6-4ca9-83f2-e5f3ba067ab8.png)

## 3.批量扫描执行

将URL放入target.txt中，执行下面命令即可实现批量扫描

```
python .\pppXray.py -r target.txt
```



## 4.其他用法参考

[Cl0udG0d/pppXray: Xray批量化自动扫描 (github.com)](https://github.com/Cl0udG0d/pppXray)

[chaitin/xray: 一款完善的安全评估工具，支持常见 web 安全问题扫描和自定义 poc | 使用之前务必先阅读文档 (github.com)](https://github.com/chaitin/xray)