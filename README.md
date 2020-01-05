#  :star2: Python期末项目之交互数据可视化网页

---
> 此项目为中大南方18级Python课程期末项目，与17级合作完成。<br>
项目内容为通过使用Python完成数据处理、可视化操作，并部署于PythonAnywhere上展示。
+ [ :v: 点击展示呀](http://womenpowerteam.pythonanywhere.com/)

##  :page_facing_up: HTML页面描述
---
**主页面主题为女性权利可视化地图与各主题柱状图跳转下拉框**

 :mega: 1. 用户可通过主页面的地图下拉框选择感兴趣的女性权利主题，按提交按钮显示不同可视化地图。<br>每个地图下方还有时间轴可供选择，既展示了横向维度也展示了纵向维度。
 
 :low_brightness: 2. 用户可选择页面下方感兴趣的主题选择下拉框观看数据图表。
 
 :bulb: 3. 下拉框下还有就业、教育、政治、计划生育叉表。

##  :white_medium_square: Python档描述
---
+ 主运行py文件为main.py 有且仅有一个py文件
- 导入多个数据可视化模块，如（plotly、pyecharts、cufflinks等）
+ 读取多个数据文件、py文件render数据可视化地图.html、py文件render数据可视化图表.html
- ' static ' 以及 ' templates ' 为网页样式以及模版
+ 其余为本项目引用的数据文档（csv）
