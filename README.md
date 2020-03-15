# 前言

Using IDL in Meteorology Version 5 Andy Heaps 的学习翻译版（仅供参考，侵权删），原著问题请联系：a.j.jeaps@reading.ac.uk，@NCAS 2010。翻译及相关问题请联系：erinsweet2016@gmail.com

这份指南的核心是一些小示例程序，使IDL用户可以快速。轻松地绘制气象学中常用的发表质量的图。

#### 文件及postscript操作

* NCREAD 读取netCDF文件
* NCWRITE 写入netCDF文件
* PSOPEN 打开一个postscript文件
* PSCLOSE 关闭一个postscript文件
* POS 在postcript页面中选择绘图位置
* SF 选择一幅等高线图或矢量图的一个域

#### 轮廓制图（contour plots）

* COLBAR 绘制一个彩色条
* CON 绘制等高线图
* LEVS 选择轮廓线
* MAP 选择一个地图投影
* STIPPLE 在一幅等高中画点
* GFILL 在等高线图上填充图案

#### 矢量图

* VECT 绘制矢量

#### 图的绘制

* EBAR 绘制错误条
* GPLOT 在图中绘制线，文本和符号
* GSYM 绘制符号的选择
* HIST 绘制直方图
* TEPHI 绘制熵温图

#### 常用

* AXES 标签轴
* CS 选择颜色比例
* GHELP 查看在线帮助文档
* GSET 建立制图区域
* LEGEND 新建制图的图例
* PCON 将压力换成以km为单位的高度，反之亦然
* REGRID 使用双线性插值重新格网化经纬度数据
* SCROP 将输入转化为一个字符的字符串

#### 旋转网格

* RGAXES 绘制旋转轴
* RGROT， RGUNROT 在旋转网格和原始坐标系之间移动点

#### shape 文件

* COUNTRY 从一个shape文件中选择国家进行绘图

#### 笔者添加

> 关系运算符
>
> * EQ 等于
> * NE 不等于
> * GE 大于等于
> * GT 大于
> * LE 小于等于
> * LT 小于
>
> 数组运算及其他符号
>
> * 数组乘 \#
> * 矩阵乘 \#\#
> * 条件表达式 ？：
> * 对象方法调用符 -&gt;
> * 指针引用符 \*
>
> 程序控制
>
> * 循环语句：FOR, WHILE, REPEAT, FOREACH
> * 条件语句：IF, CASE, SWITCH
> * 跳转语句：Break, Continue, GoTo



这个说明文档分为三部分：制图及代码样例，使用IDL的指导，和指导路线参考。

#### 访问指导流程的设置

指导见：http://ncas-cms.nerc.ac.uk/graphics/idl（节稿前，笔者未能打开该网站）

Unix，Mac和PC的安装简介见附录A。



#### 运行样例

在UNIX系统的命令行中打开IDL并且编译运行第一个样例：

```text
idl
ex1
```

输入q或者在图像化窗口点击escape，退出视图并且返回IDL命令行。



