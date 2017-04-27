# BookLibraryIntro
Java期中作业家庭图书馆说明



## 概述
家庭图书管理系统 [原型设计](https://pkudarkcom.github.io/BookLibraryIntro/start.html#g=1&p=index)

#### 小组构成
- 产品管理组：[**张旭**](https://github.com/orgs/PkuDarkCom/people/zhangxu273)<br>
- 前端设计小组：**禹单单**，[**于飞**](https://github.com/orgs/PkuDarkCom/people/mumuCode)<br>
- 后端设计小组：[**陈亨**](https://github.com/orgs/PkuDarkCom/people/adreamteama)，[任荣刚](https://github.com/orgs/PkuDarkCom/people/renrg)<br>
- 测试组：**赵孝锋**，刘艳波，武小强，蔡先慧<br>

#### 小组分工
- **产品管理组**<br>
负责全局进度把控，数据结构设计，功能模块设计，文档的编写与维护<br>

- **前端设计小组**<br>
负责把服务器传来的内容通过web页面展示出来，以及移动端的适配<br>
时间允许 可以 顺手做一个 微信小程序展示<br>

- **后端设计小组：**<br>
这次java作业的主力，负责业务逻辑的编写，以及提供接口给前端使用<br>

- **测试小组：**<br>
对产品进行验收测试 提出修改意见<br>

#### 设计内容
- **书架管理模块**

	书架是用于记录书籍存放的位置的容器，如果把书比作文件的话，书架就相当于文件夹。<br>
	书架管理模块需要实现<br>
	* 创建书架
	* 编辑书架
	* 删除书架
	* 按书架查询该书架上的所有图书
- **书籍管理模块**

	* 创建书籍数据
	* 编辑书籍数据
	* 删除书籍数据
	* 按ISBN查询书籍数据
	* 按标题查询书籍数据
	* 按作者查询书籍数据
	* 按译者查询书籍数据
	* 按出版社查询书籍数据
	* 按TAG查询书籍数据数据
	* 按阅读状态书籍查询数据
	* 按是否是电子书查询书籍数据
  * 按评分排序筛选书籍数据

- **豆瓣爬虫模块**
	* 根据isbn从豆瓣获取图书数据
  * 获取数据后入库

- **ISBN的图像识别**（选做）
	* 输入一张图片 输出isbn号

- **用户系统**（选做）
	* 增加用户
	* 删除用户
	* 修改用户
	* 用户登录登出
	* 用户的阅读状态分开记录
	* 用户操作日志

#### 开发工具
#### 应用平台

## 系统设计
#### 功能模块设计
#### 数据结构设计

###### 书籍存储结构
<table>
<tr><th>字段名</th><th>变量</th><th>字段类型</th></tr>
<tr><td>索引（主键）</td><td>id</td><td>int</td></tr>
<tr><td>ISBN</td><td>isbn13</td><td>int</td></tr>
<tr><td>存储书架</td><td>storage</td><td>int</td></tr>
<tr><td>电子书与否</td><td>is_ebook</td><td>bool</td></tr>
<tr><td>阅读与否</td><td>is_read</td><td>bool</td></tr>
<tr><td>标题</td><td>title</td><td>text</td></tr>
<tr><td>原文标题</td><td>origin_title</td><td>text</td></tr>
<tr><td>封面图</td><td>image</td><td>text</td></tr>
<tr><td>作者（可以多人）</td><td>author</td><td>text</td></tr>
<tr><td>译者（可以多人）</td><td>translator</td><td>text</td></tr>
<tr><td>出版社</td><td>publisher</td><td>text</td></tr>
<tr><td>出版日期</td><td>pubdate</td><td>text</td></tr>
<tr><td>豆瓣评分</td><td>rating</td><td>text</td></tr>
<tr><td>标签（可以多个）</td><td>tags</td><td>text</td></tr>
<tr><td>装帧</td><td>binding</td><td>text</td></tr>
<tr><td>价格</td><td>price</td><td>text</td></tr>
<tr><td>页数</td><td>pages</td><td>text</td></tr>
<tr><td>作者简介</td><td>author_intro</td><td>text</td></tr>
<tr><td>书籍简介</td><td>summary</td><td>text</td></tr>
<tr><td>目录</td><td>catalog</td><td>text</td></tr>
</table>


###### 书架存储结构
<table>
<tr><th>字段名</th><th>变量</th><th>字段类型</th></tr>
<tr><td>书架索引（主键）</td><td>id</td><td>int</td></tr>
<tr><td>书架描述</td><td>desc</td><td>Text</td></tr>
</table>


#### API设计
Api采用RESTFul 风格设计<br>
实现书籍信息的增删改查,返回格式为json

[获取书籍信息](https://github.com/PkuDarkCom/BookLibraryIntro/wiki/API%EF%BC%9A%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF)<br>
[图书查询](https://github.com/PkuDarkCom/BookLibraryIntro/wiki/API%EF%BC%9A%E5%9B%BE%E4%B9%A6%E6%9F%A5%E8%AF%A2)<br>
[增加图书](https://github.com/PkuDarkCom/BookLibraryIntro/blob/master/Apis/%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF.md)<br>
[修改图书](https://github.com/PkuDarkCom/BookLibraryIntro/blob/master/Apis/%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF.md)<br>
[删除图书](https://github.com/PkuDarkCom/BookLibraryIntro/blob/master/Apis/%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF.md)<br>

## 实现与测试
#### 关键技术实现
#### 测试运行结果

## 开发日志
<table>
    <tr>
        <td>2017.4.18</td>
		<td>立项</td>
    </tr>
    <tr>
        <td></td>
		<td>模块设计</td>
    </tr>
    <tr>
        <td></td>
		<td>服务器环境部署</td>
    </tr>
    <tr>
        <td></td>
		<td>人员分工确定</td>
    </tr>
    <tr>
        <td>2017.4.24</td>
		<td>设计数据表结构</td>
    </tr>
    <tr>
        <td></td>
		<td>设计api</td>
    </tr>
	    <tr>
        <td></td>
		<td>Github建立组织与仓库</td>
    </tr>
</table>

## 总结
## 参考文献
