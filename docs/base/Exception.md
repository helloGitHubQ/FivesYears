系统运行,风云不测,睹始知终,秋去冬来,一落叶而知秋.
						     --Easy Coding
# 异常&日志 #
## 异常分类 ##
 Throwable 是所有异常的父类，分为 Error 和 Exception两种。

废话不多说直接上图

![](https://i.imgur.com/CHvYvaN.png)

## 捕获异常 ##
try - catch - finally

finally 代码块的任务是清理资源、释放连接、关闭管道流等等操作。

finally 代码块中使用 return 语句，使返回值的判断变得复杂。所以为了避免返回值不可控。我们不要在 finally 代码块中使用 return 语句。（此处应该有例子 lueluelue）

当涉及到 break 和 continue 的时候，finally也会执行。
## 异常丢失 ##
+ 前一个异常还没处理就抛出下一个异常
+ finally 中使用 return 
## 其他 ##
- 异常限制
- 异常匹配
- 构造器
- 创建自定义异常
- 异常链
- 重新抛出异常
- 栈轨迹
- 常见异常
## 日志 ##
规范自己的日志命名，推荐日志命名方式: appName _logType _
logName.log

日志级别分类：

+ DEBUG 级别日志，记录对调试有帮助的信息。
+ INFO 级别日志，用于记录程序运行现场，虽然此处并未发生错误，但是对排除错误有重要意义。
+ WARN 级别日志，也是用来记录程序运行现场，更偏向于表明此处可能发生错误。
+ ERROR 级别日志，当前程序发生错误，需要被关注。但是当前错误没有影响系统的正常运行
+ FATAL 级别日志，当前程序发生严重错误，程序中断。

 
### 5/27/2019 9:50:50 PM 

java虚拟机栈中可能会出现两种异常：StarkOverFlowError & OutOfMemoryError

### 6/15/2019 9:12:28 AM 

Math.pow 求某数的任意次方, 抛出ArithmeticException处理溢出异常
### 6/21/2019 9:52:20 AM 
UnsupportedOperationException（不支持方法异常）

### 6/28/2019 2:52:07 PM 

    String[] str=new String[?];

如果 ? 处写的是负数的话就会抛 NegativeArraySizeException。