#  :star2: Python期末项目之交互数据可视化网页

---
> 此项目为中大南方18级Python课程期末项目，与17级合作完成。<br>
项目内容为通过使用Python完成数据处理、可视化操作，并部署于PythonAnywhere上展示。
+ [ :v: Pythonanywhere页面展示呀](http://womenpowerteam.pythonanywhere.com/)

##  :page_facing_up: HTML页面描述
---
**主页面主题为女性权利可视化地图与各主题柱状图跳转下拉框**

 :mega: 1. 用户可通过主页面的地图下拉框选择感兴趣的女性权利主题，按提交按钮显示不同可视化地图。<br>每个地图下方还有时间轴可供选择，既展示了横向维度也展示了纵向维度。
 
 :low_brightness: 2. 用户可选择页面下方感兴趣的主题选择下拉框观看数据图表。
 
 :bulb: 3. 下拉框下还有就业、教育、政治、计划生育叉表。
 
 :bulb: 4. 共有五个url，第一个为总页面，第二个为地图互后缀为query，第三个为国家议会女性人数占国家议会女性人数占比页面后缀为meeting，第四个为中小学女生与男生的入学比例页面后缀为female，第五个为dash，后缀为dash。
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

## :vhs: 数据传递描述
---
  :sailboat: **数据结构循环 ：** >  for i in range(2006, 2018):  【详情见main.py line 36】<br>
  :tram: **数据嵌套 ：**  > list(zip(list(df3['CountryName']),list(df3["{}".format(i)])))  【详情见main.py line 40】<br>
  :aerial_tramway: **使用推导式：**  > the_region = request.form["the_region_selected1"] ## 取得用户交互输入<br>
 :suspension_railway: **使用条件判断：** <br>

>     if the_region =="中小学女生与男生的入学比例（%）":
        with open("1.html", encoding="utf8", mode="r") as f:                  
            plot_all3 = "".join(f.readlines())  
            text = '同一教育阶段的女生正越来越获得与男生一样平等的教育机会。'
    elif the_region=="国家议会中妇女席位的比例（%）":
        with open("2.html", encoding="utf8", mode="r") as f:                  
            plot_all3 = "".join(f.readlines())
            text = '政治领域性别比例改善，从政女性数量的大幅增加。'
    elif the_region=="孕产妇死亡率（每10万例活产中所占比例）":
        with open("3.html", encoding="utf8", mode="r") as f:                  
            plot_all3 = "".join(f.readlines())
            text = """1. 北非，南亚和中亚五国中的土库曼斯坦、阿富汗斯坦与大洋洲岛国、东南亚地区除新马泰以外的国家孕妇死亡率较高。
					  \n2. 欧洲澳洲北美地区和东亚地区的孕妇死亡率较低。

 :train2:  **Python文档与HTML文档数据交互**
> import dash_html_components as html<br>
map_world().render('1.html')<br>
with open("3.html", encoding="utf8", mode="r") as f: <br>
return render_template('First.html'

