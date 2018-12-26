### 1. 接口抓包
找到要mock的接口
```
以掘金首页为例，找到下面的接口
https://gold-tag-ms.juejin.im/v1/categories
```

![](https://user-gold-cdn.xitu.io/2018/12/18/167c0fbaf55aae14?w=1829&h=1093&f=png&s=140048)

### 2. 复制接口数据到本地
在接口上进行右键点击，选择save -> …and Open as Local File -> 默认会保存至桌面，示例中的数据，保存到了桌面的88_.json

![](https://user-gold-cdn.xitu.io/2018/12/18/167c0fcaae5e5e10?w=1847&h=1120&f=jpeg&s=297337)

### 3. 修改数据
修改保存到本地的json文件，示例中仅修改了页面的标签数据。
![](https://user-gold-cdn.xitu.io/2018/12/18/167c0fd83380d046?w=1285&h=985&f=png&s=31573)

### 4. 增加监听规则
选择工具栏 AutoResponder -> Add Rule -> 选择
![](https://user-gold-cdn.xitu.io/2018/12/18/167c102e133b9cf4?w=1894&h=1081&f=png&s=63423)

### 5. 修改规则
如下图，习惯使用正则方式匹配接口

```
格式：regex:url  
regex代表通过正则匹配，url代表需要监听的接口地址
```
![](https://user-gold-cdn.xitu.io/2018/12/18/167c104db6fe15ba?w=1122&h=204&f=png&s=7482)

### 6. 匹配数据
Local file to return ... 选择下拉列表中的Find a file ...
![](https://user-gold-cdn.xitu.io/2018/12/18/167c10892e464906?w=1127&h=451&f=png&s=9714)

![](https://user-gold-cdn.xitu.io/2018/12/18/167c109d9b423b7b?w=1244&h=188&f=png&s=4017)

### 7. save，刷新页面