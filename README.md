# eamisAutoClicker
NKU EAMIS选课脚本
## LOG
- 2019.06.13 2019-2020学年度第一学期预选
- 2019.02.27 profileId改为18-19第二学期第二次补退选
- 2019.02.22 现在可以一次抢多个课的多个不同分组了
- 2019.02.19 现在可以一次抢两个课了；profileId改为18-19第二学期补退选；sleeptime现在由随机数决定，此功能由 lost222 的 pull request 实现
- 2019.01.19 First Editon，只支持抢一个课的单一分组
## 如何使用
- 打开浏览器console粘贴进去运行。会运行到所有要抢的课都成功后才会结束
- inputid是储存要抢的课号的数组，手动修改添加即可
- 每次尝试抢哪个课的哪个分组由随机数确定，如果此课无分组输出时会显示undefined，是正常的
- sleeptime现在由随机数确定，如果需要固定间隔请把第12行`true`改为`false`
- 若选课系统不同请将ajax函数中url末的profileId改为对应选课系统的ID，现在的ID是18-19第二学期第二次补退选ID
## 注意
- 请不要抢与现有课程冲突的课，因为选课系统里时间冲突的判断逻辑是在浏览器前端完成的，会带来未知后果
- 抢已选上的课或者已修过的课会直接浏览器报错，我没做脚本内的报错逻辑
- 所有课程均抢到后才有窗口提示。抢到其中某一门课只会在console输出一条成功的log
- 抢到课后不会在课表中立即显示出来，需要刷新选课页面
