# STATA基础理论学习

## 导入数据

利用命令查看当前的工作路径

```stata
pwd /*查看当前的工作路径*/
import excel "path"，sheet("汇总")
firstrow clear /*首行作为变量名*/
save "path"
cd "path"指定工作路径
use "path.dta",clear *调用dta数据
```

面板数据的定义

如果地点名称为英文，则需要进行重新编码

```stata
encode province, gen(provi) *变为1234等数字取代
xtset provi year *定义为面板数据
```

![image-20231201202929506](C:\Users\郑宇坤和柯菲\AppData\Roaming\Typora\typora-user-images\image-20231201202929506.png)

面板数据类型同上，可以按照省份排也可以按照年份排