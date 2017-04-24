# BookLibraryIntro
Java期中作业家庭图书馆说明



## 概述

### 小组构成及分工
### 设计内容
### 开发工具
### 应用平台

## 系统设计
### 功能模块设计
### 数据结构设计

#### 书籍存储结
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


#### 书架存储结构
<table>
<tr><th>字段名</th><th>变量</th><th>字段类型</th></tr>
<tr><td>书架索引（主键）</td><td>id</td><td>int</td></tr>
<tr><td>书架描述</td><td>desc</td><td>Text</td></tr>
</table>


### API设计
Api采用RESTFul 风格设计<br>
实现书籍信息的增删改查,返回格式为json

[获取书籍信息](https://github.com/PkuDarkCom/BookLibraryIntro/blob/master/Apis/%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF.md)<br>
[获取书籍详细信息](https://github.com/PkuDarkCom/BookLibraryIntro/blob/master/Apis/%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF.md)<br>
[增加图书](https://github.com/PkuDarkCom/BookLibraryIntro/blob/master/Apis/%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF.md)<br>
[修改图书](https://github.com/PkuDarkCom/BookLibraryIntro/blob/master/Apis/%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF.md)<br>
[删除图书](https://github.com/PkuDarkCom/BookLibraryIntro/blob/master/Apis/%E8%8E%B7%E5%8F%96%E4%B9%A6%E7%B1%8D%E4%BF%A1%E6%81%AF.md)<br>

## 实现与测试
### 关键技术实现
### 测试运行结果

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
