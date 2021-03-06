# node 电影网站

## 导航

- [项目前期准备](#项目前期准备)
- [需求分析](#需求分析)
- [Node入口文件分析和目录初始化](#Node入口文件分析和目录初始化)

## 项目前期准备

- 后端使用技术

    - node(express)
    - mongodb(mongoose)
    - jade
    - moment.js
    - npm

- 前端使用技术

    - jQuery
    - Bootstrap
    - Bower

- 实战步骤

    1. 需求分析

        需要几个页面，每个页面有什么样的功能；

    2. 项目依赖初始化

        创建目录并安装依赖；

    3. 入口文件编码

        编写入口文件代码；

    4. 创建视图

        创建几个页面的模板；

    5. 测试前端流程

        跑通前后端流程；

    6. 样式开发，伪造模板数据；

    7. 设计数据库模型

        根据页面内容设计数据库模型；

    8. 开发后端逻辑

    9. 配置依赖文件，网站开发结束

## 需求分析

总共需要4个页面:

1. 电影展示页面

    这里展示了一系列的电影，包括电影的海报、名字、播放按钮，并且点击海报或者播放按钮就可以调到电影的详情页；

2. 电影详情页

    这个页面包含一些电影的详细信息以及电影的播放；

3. 后台录入页面

    通过表单提交数据，然后提交到后台；

4. 后台电影列表管理页面

    每一部存入到数据库中的电影都可以在这里进行管理；

## Node入口文件分析和目录初始化

测试路由如下:

```
localhost:3000/
localhost:3000/movie/1
localhost:3000/admin/movie
localhost:3000/admin/list
```

目录初始化

```
.
├── app.js
├── package.json
├── README.md
└── views
    ├── admin.pug
    ├── detail.pug
    ├── index.pug
    └── list.pug

```

## 创建四个pug视图及入口文件中处理

## 伪造模板数据跑通前后端交互流程

### 目录层调整

目录层调整——多个文件代码相似，如果一个文件一个文件修改，显然是极不可取的，所以利用 pug 的 include & inheritance。

```
.
└── views
    ├── includes
    ├── layout.pug
    └── pages
        ├── admin.pug
        ├── detail.pug
        ├── index.pug
        └── list.pug
```

```pug
doctype html
html
    head
        meta(charset='utf-8')
        title #{title}
        include ./includes/head
    body
        include ./includes/header
        block content
        h1 #{title}
```

### 编写样式

- 安装 Bootstrap（注意后面的`@3`，如果不加的话会提示不存在）

    ```
    bower install bootstrap@3
    ```
- 编写 header.pug

- 编写 head.pug

- 编写 index.pug

- 编写 detail.pug

- 编写 admin.pug

- 编写 list.pug

### 伪造数据

## mongodb模式模型设计及编码

## 编写数据库交互代码

## 删除功能及项目生成配置文件
