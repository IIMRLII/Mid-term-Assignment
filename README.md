### 主要功能1：增加日期显示

#### 效果图：

<img src="README.assets/image-20211122225644180.png" alt="image-20211122225644180" style="zoom:50%;" />

#### 实现方法：

修改布局文件，预留时间显示空间

![image-20211122225933905](README.assets/image-20211122225933905.png)

在 SimpleCursorAdapter 的显示条目中增加日期栏

![image-20211122225839933](README.assets/image-20211122225839933.png)

并在 SimpleCursorAdapter 实现前对其进行 viewBinder 的绑定，使便签项中显示的时间格式化

![image-20211122225628594](README.assets/image-20211122225628594.png)

------

### 主要功能2：增加搜索显示（动态演示见附加功能）

#### 效果图：

##### 搜索前

<img src="README.assets/image-20211122230056708.png" alt="image-20211122230056708" style="zoom:50%;" />

##### 搜索后

<img src="README.assets/image-20211122230127331.png" alt="image-20211122230127331" style="zoom:50%;" />

#### 实现方法：

修改主视图，创建搜索框

![image-20211122230331539](README.assets/image-20211122230331539.png)

监听搜索框内容变化时修改 query_string 并触发数据库检索，同时根据框中内容决定是否显示清空按钮

![image-20211122230723560](README.assets/image-20211122230723560.png)

根据 query_string 进行模糊查询并刷新页面

![image-20211122231123822](README.assets/image-20211122231123822.png)

------

### 附加功能1：UI美化

#### 效果图：

<img src="README.assets/image-20211122231724606.png" alt="image-20211122231724606" style="zoom:50%;" />

#### 实现方法：

修改 styles.xml ，修改主题颜色（Action Bar颜色）

![image-20211122231900268](README.assets/image-20211122231900268.png)

在 drawable 文件夹下创建新 shape ，作为便签项的背景

![image-20211122232152295](README.assets/image-20211122232152295.png)

将 shape 应用于背景，并设置标签项阴影、间距等属性完成简单界面美化

![image-20211122232403231](README.assets/image-20211122232403231.png)

------

### 附加功能2：添加动画效果

#### 进入app动画效果：

<img src="README.assets/enterapp.gif" alt="enterapp" style="zoom:50%;" />

#### 搜索动画效果：

<img src="README.assets/serach.gif" alt="serach" style="zoom:50%;" />

#### 实现方法：

博客链接：https://blog.csdn.net/qq_40517035/article/details/121473836

首先我们在 res 文件夹下新建 anim 文件夹，并在 anim 文件夹中新建 list_anim_layout.xml 文件作为我们的主动画文件。在 list_anim_layout.xml 文件中写入下图代码

![3c7acc75cd9c47a491d73d6e7a4c7885](README.assets/3c7acc75cd9c47a491d73d6e7a4c7885.png)

然后在 anim 文件夹中新建 list_first_move.xml 文件作为我们的具体动画文件，写入代码

![3d18ffdbf78f4c25bfc909744015652a](README.assets/3d18ffdbf78f4c25bfc909744015652a.png)

最后在布局文件中找到我们要设置动画的对象，然后设置其 android:layoutAnimation 属性为刚才设置的主动画文件即可

![32fa7802bbfc4644b15c42e815156af5](README.assets/32fa7802bbfc4644b15c42e815156af5.png)

------

### 附加功能3：背景颜色修改

#### 效果图：

<img src="README.assets/changebackground.gif" alt="changebackground" style="zoom:50%;" />

#### 实现方法：

创建弹窗布局文件，包含 seekbar

![image-20211122233609980](README.assets/image-20211122233609980.png)

修改菜单文件，增加背景修改图标

![image-20211122233802791](README.assets/image-20211122233802791.png)

设置单击图标触发弹窗事件

![image-20211122234002572](README.assets/image-20211122234002572.png)

对每个进度条设置拖动事件

![image-20211122234135284](README.assets/image-20211122234135284.png)

数据存储使用 SharedPreference

![image-20211122234250134](README.assets/image-20211122234250134.png)

------

报告结束，感谢收看:)

