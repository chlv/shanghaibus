#shanghaibus
修改记录


9/13/2018:
站点停靠信息界面已画好， 接下来要用storage存储信息，方便控件之间数据共享交互
设定加载界面的timeout时间， 超时返回到上一个界面

9/17/2018：
增加python虚拟环境

10/8/2018:
基本界面已经完成，停站信息修改，数据存储在JSON，kivy默认存储数据不同步
待修复问题：
1. 设定加载时的timeout返回
2. 出错时的返回，网络未连接的返回， 现在没有返回按钮
3. 停站信息没有修改完成，刚刚实现到站数修改
4. 监控部分逻辑功能未完成
5. 监控信息修改界面在大窗口时，上部分有黑屏

10/11/2018:
1. 上个版本中1，2，5已经修复
2. 上海发布网络接口发生变换
3. http --> https
4. 公交线路查询网址变换 https://shanghaicity.openservice.kankanews.com/public/bus/mes/sid/{sid}?stoptype=1
5. 首末班车 网页解析元素变化 //div[@class='upgoing cur ' or @class='upgoing ']/p/span/text()

10/12/2018：
1.监控站点，到站信息动态刷新
2.刷新间隔60s

10/24/2018:
界面配置和存储已经完成，准备完成监控告警逻辑

10/25/2018:
基本功能完成，Clock时序存在问题

10/27/2018:
PC端功能完成， 公交线路列表可以更新
1. 界面刷新间隔5s
2. 告警间隔30s
3. 查询间隔60s
告警列表中有满足条件的就告警，多个条件满足，告警一次