# timetask - 定时任务系统
一款支持自定义定时任务的chatgpt-on-wechat插件，支持自定义时间、轮询周期、自定义时间，包含动态添加任务、取消任务、查看任务列表等功能，一款定时任务系统的插件。


## **【插件安装方法】**
1、clone本仓库 或 下载源代码
2、将本插件放进 chatgpt-on-wechat 的 plugins 文件夹中（chatgpt-on-wechat启动后，会自动加载本插件）
3、安装插件依赖库，使用命令：pip3 install -r requirements.txt
4、至此，插件安转完毕，启动chatgpt-on-wechat，使用 timetask 插件


## **【插件使用方法】**
1、启动chatgpt-on-wechat
2、与机器人对话，告诉机器人想要的定时任务，需要使用定时任务的指令(指令在下面会详解)
3、机器人将在你设定的时间，执行目标任务。

## **【定时任务-指令详解】**

### **一、添加定时任务**

【指令格式】：**$time 周期 时间 事件**
**①、$time**：指令前缀，当聊天内容以$time开头时，则会被当做为定时指令
**②、周期**：今天、明天、后天、每天、工作日、每周X（如：每周三）、YYYY-MM-DD的日期
**③、时间**：X点X分（如：十点十分）、HH:mm:ss的时间
**④、事件**：想要做的事情

示例：
```
a、指令： $time 明天 十点十分 提醒我健身
b、指令执行成功（机器人会回复 任务ID 及 任务信息）如下 ：
	 恭喜你，定时任务已创建成功🎉~
	【任务ID】：urwOi0he
	【任务详情】：$time 今天 十三点40 提醒我健身
```
	
	
### **二、取消定时任务**

##### **方法一、直接通过任务ID，取消定时任务**

【指令格式】：**$time 取消任务 任务ID**
**①、$time 取消任务**：指令前缀，以此前缀，会取消定时任务
**②、任务ID**：机器人回复的任务ID（添加任务成功时，机器人回复中有）

示例：
```
a、指令：$time 取消任务 urwOi0he
b、指令执行成功（机器人会回复 任务ID 及 任务信息）如下 ：
	 取消成功，定时任务已被取消~
	【任务ID】：urwOi0he
	【任务详情】：$time 今天 十三点40 提醒我健身
```
	
	

##### **方法二、先查询任务ID列表，然后选择要取消的任务ID，取消定时任务**

1、【指令格式】：$time 任务列表
指令执行成后，机器人会将所有 待执行的任务列表，回复出来。

2、根据1中的任务列表，选择要取消的任务ID，执行上面的方法一（直接通过任务ID，取消定时任务）
