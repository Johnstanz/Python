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

##  :large_blue_diamond: Python档描述
---
+ 主运行py文件为main.py 有且仅有一个py文件
- 导入多个数据可视化模块，如（plotly、pyecharts、cufflinks等）
+ 读取多个数据文件、py文件render数据可视化地图.html、py文件render数据可视化图表.html
- ' static ' 以及 ' templates ' 为网页样式以及模版
+ 其余为本项目引用的数据文档（csv）

##  :large_orange_diamond: HTML档描述
---
+ base.html为基模板，其实frist.html、historical_event.html、rencent_data.html、result2.html继承了基模板。
- 有多个html主要用于导入数据；生成可视化图表，最后render进py
+ 除了在hf.css中输入css样式，也可在各输出网页的html上增加一些css样式，还可以引入javascript制作好看的动态效果。

## :shipit: WEB动作描述
---
+ 地图区：用户选择不同主题可呈现不同地图、用户选择不同年份可呈现不同年份的地图、以及相应的故事
- 跳转数据图表区：用户选择不同主题后，跳转至不同主题页面呈现不同数据图表
- dash区：用户可选择dash按钮跳转仪表盘
- 交互：用户选择进行不同主题不同年份进行交互

## :white_flower: 自定义函数模块与功能拓展
---
+ 函数取名符合标准： 如map_world、update_graph等函数
- 模块符合标准： 如pandas、pyecharts、cufflinks等模块
+ 功能拓展：数据可视化的世界地图可放大缩小、不同国家的选取块不同、鼠标悬停后还有文字介绍。


