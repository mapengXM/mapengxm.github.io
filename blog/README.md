## 脚手架

### springboot项目

#### 人人开源 / renren-fast

- renren-fast是一个**轻量级**的，`前后端分离`的Java快速开发平台，能快速开发项目并交付【接私活利器】
- 实现前后端分离，`通过token进行数据交互`，前端再也不用关注后端技术
- 使用Spring Boot、Shiro、MyBatis、Redis、Bootstrap、Vue2.x等框架，包含：管理员列表、角色管理、菜单管理、定时任务、参数管理、代码生成器、日志管理、云存储、API模块(APP接口开发利器)、前后端分离等。
- 灵活的`权限控制`，可控制到页面或按钮，满足绝大部分的权限需求
- 页面交互使用**Vue2.x**，极大的提高了开发效率
- 完善的代码生成机制，可在线生成entity、xml、dao、service、vue、sql代码，减少70%以上的开发任务
- 引入quartz定时任务，可动态完成任务的添加、修改、删除、暂停、恢复及日志查看等功能
- 引入API模板，根据token作为登录令牌，极大的方便了APP接口开发
- 引入Hibernate Validator校验框架，轻松实现后端校验
- 引入云存储服务，已支持：七牛云、阿里云、腾讯云等
- 引入swagger文档支持，方便编写API接口文档
- 核心框架：Spring Boot 2.0
- 安全框架：Apache Shiro 1.4
- 视图框架：Spring MVC 5.0
- 持久层框架：MyBatis 3.3
- 定时器：Quartz 2.3
- 数据库连接池：Druid 1.0
- 日志管理：SLF4J 1.7、Log4j
- 页面交互：Vue2.x

- 本项目是前后端分离的，还需要部署前端，才能运行起来**(无部门)**
- renren-fast-vue基于vue、element-ui构建开发，实现[renren-fast](https://gitee.com/renrenio/renren-fast)后台管理前端功能，提供一套更优的前端解决方案
- 前端下载地址：<https://gitee.com/renrenio/renren-fast-vue>
- 前端部署文档：<https://gitee.com/renrenio/renren-fast-vue/wikis/Home>
- 前端部署完毕，就可以访问项目了，账号：admin，密码：admin



- 数据交互

> - 一般情况下，web项目都是通过session进行认证，每次请求数据时，都会把jsessionid放在cookie中，以便与服务端保持会话
> - 本项目是前后端分离的，`通过token进行认证（登录时，生成唯一的token凭证），每次请求数据时，都会把token放在header中，服务端解析token，并确定用户身份及用户权限，数据通过json交互`

![img](https://cdn.renren.io/b6541201803082303391694.jpg)


#### 若依

- **1、系统环境**

  - Java EE 8
  - Servlet 3.0
  - Apache Maven 3

  **2、主框架**

  - Spring Boot 2.0
  - Spring Framework 5.0
  - Apache Shiro 1.4

  **3、持久层**

  - Apache MyBatis 3.4
  - Hibernate Validation 6.0
  - Alibaba Druid 1.1

  **4、视图层**

  - Bootstrap 3.3
  - Hplus 4.1
  - Thymeleaf 3.0

- 用户管理：用户是系统操作者，该功能主要完成系统用户配置。

- **部门管理**：配置系统组织机构（公司、部门、小组），树结构展现支持数据权限。

- **岗位管理**：配置系统用户所属担任职务。

- 菜单管理：配置系统菜单，操作权限，按钮权限标识等。

- 角色管理：角色菜单权限分配、设置角色按机构进行数据范围权限划分。

- **字典管理**：对系统中经常使用的一些较为固定的数据进行维护。

- **参数管理**：对系统动态配置常用参数。

- **通知公告**：系统通知公告信息发布维护。

- 操作日志：系统正常操作日志记录和查询；系统异常信息日志记录和查询。

- **登录日志**：系统登录日志记录查询包含登录异常。

- **在线用户**：当前系统中活跃用户状态监控。

- 定时任务：在线（添加、修改、删除)任务调度包含执行结果日志。

- 代码生成：前后端代码的生成（java、html、xml、sql)支持CRUD下载 。

- 系统接口：根据业务代码自动生成相关的api接口文档。

- 在线构建器：拖动表单元素生成相应的HTML代码。

- 连接池监视：监视当期系统数据库连接池状态，可进行分析SQL找出系统性能瓶颈。

#### eladmin

1. 适合

2. 项目基于 Spring Boot 2.1.0 、 Spring boot Jpa、 Spring Security、redis、Vue的前后端分离的权限管理系统，项目采用分模块开发方式， 权限控制采用 RBAC（Role-Based Access Control，基于角色的访问控制），支持数据字典、数据权限管理、前端菜单支持动态路由

   ```
   - 系统管理
       - 用户管理 提供用户的相关配置
       - 角色管理 对权限与菜单进行分配
       - 权限管理 权限细化到接口
       - 菜单管理 已实现菜单动态路由，后端可配置化，支持多级菜单
       - 部门管理与岗位管理
       - 字典管理 应广大码友的要求加入字典管理
   - 系统监控
       - 操作日志 使用apo记录用户操作日志
       - 异常日志 记录操作过程中的异常，并且提供查看异常的堆栈信息
       - 系统缓存 使用jedis将缓存操作可视化，并提供对redis的基本操作，可根据需求自行扩展
       - 实时控制台 实时打印logback日志，来自微强迫症患者的精心配色，更好的监控系统的运行状态
       - SQL监控 采用druid 监控数据库访问性能，默认用户名admin，密码123456
   - 系统工具
    - 定时任务 整合Quartz做定时任务，加入任务日志，任务运行情况一目了然
       - 代码生成 高灵活度一键生成前后端代码，减少百分之80左右的工作任务
       - 接口文档 使用的是 swagger-ui 
       - 邮件工具 配合富文本，发送html格式的邮件
       - SM.MS免费图床 挺好用的一个图床，作为公共图片上传使用
       - 七牛云存储 这个就不多说了
       - 支付宝支付 提供了测试账号，可自行测试
   - 组件管理
       - 图标库 系统图标来自 https://www.iconfont.cn/
       - 富文本 集成wangEditor富文本
       - Markdown编辑器与Yaml编辑器
   ```

   - 基础框架：Spring Boot 2.1.0.RELEASE
   - 持久层框架：Spring boot Jpa
   - 安全框架：Spring Security
   - 缓存框架：Redis
   - 日志打印：logback+log4jdbc
   - 接口文档 swagger2
   - 其他：fastjson、aop、MapStruct等

3. 前端

   - node
   - vue
   - vue-router
   - axios
   - element ui

4. 初始模板基于`vue-admin-template`

#### **FEBS-Shiro**  2.0  

FEBS-Shiro是一款简单高效的后台权限管理系统，使用Spring Boot，Shiro和Layui构建。FEBS意指：**F**ast，**E**asy use，**B**eautiful和**S**afe。相信无论作为企业级应用，私活开发脚手架或者权限系统构建学习，FEBS-Shiro都会是一个不错的选择。2091

| 名称           | 描述                                                         | 地址                                                    |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------- |
| FEBS-Shiro 1.x | Spring Boot 2.0.4 & Shiro1.4.0 权限管理系统（单页）。        | <https://github.com/wuyouzhuguli/FEBS-Shiro/tree/mysql> |
| FEBS-Security  | Spring Boot 2.0.4 & Spring Security 5.0.7 权限管理系统（单页）。 | <https://github.com/wuyouzhuguli/FEBS-Security>         |
| FEBS-Vue       | FEBS-Shiro前后端分离版本，前端架构采用Vue全家桶。            | <https://github.com/wuyouzhuguli/FEBS-Vue>              |

系统功能模块组成如下所示：

```
├─系统管理
│  ├─用户管理
│  ├─角色管理
│  ├─菜单管理
│  └─部门管理
├─系统监控
│  ├─在线用户
│  ├─系统日志
│  ├─登录日志
│  ├─Redis监控
│  ├─Redis终端
│  ├─请求追踪
│  ├─系统信息
│  │  ├─JVM信息
│  │  ├─TOMCAT信息
│  │  └─服务器信息
├─任务调度
│  ├─定时任务
│  └─调度日志
├─代码生成
│  ├─生成配置
│  ├─代码生成
└─其他模块
   ├─FEBS组件
   │  ├─表单组件
   │  ├─表单组合
   │  ├─FEBS工具
   │  ├─系统图标
   │  └─其他组件
   ├─APEX图表
   ├─高德地图
   └─导入导出

```



1. 前后端请求参数校验
2. 支持Excel导入导出
3. 前端页面布局多样化，主题多样化
4. 支持多数据源，代码生成
5. 多Tab页面，适合企业应用
6. 用户权限动态刷新
7. 浏览器兼容性好，页面支持PC，Pad和移动端。
8. 代码简单，结构清晰

后端

- [Spring Boot 2.1.3](http://spring.io/projects/spring-boot/)
- [Mybatis-Plus](https://mp.baomidou.com/guide/)
- [MySQL 5.7.x](https://dev.mysql.com/downloads/mysql/5.7.html#downloads),[Hikari](https://brettwooldridge.github.io/HikariCP/),[Redis](https://redis.io/)
- [Shiro](http://shiro.apache.org/)

前端

- [Layui 2.5.4](https://www.layui.com/)
- [Nepadmin](https://gitee.com/june000/nep-admin)
- [formSelects 4.x 多选框](https://hnzzmsf.github.io/example/example_v4.html)
- [eleTree 树组件](https://layuiextend.hsianglee.cn/eletree/)
- [formSelect.js树形下拉](https://wujiawei0926.gitee.io/treeselect/docs/doc.html)
- [Apexcharts图表](https://apexcharts.com/)

#### Vhr 微人事

- 4293

微人事是一个前后端分离的人力资源管理系统，项目采用SpringBoot+Vue开发。

后端技术栈

1.SpringBoot
2.SpringSecurity
3.MyBatis
4.MySQL

前端技术栈

1.Vue
2.ElementUI
3.axios
4.vue-router

还有其他一些琐碎的技术就不一一列举了。

#### jeecg-boot

1. Github上面，非常强大
2. Jeecg-boot 是一款基于代码生成器的智能开发平台！采用前后端分离技术:SpringBoot，Mybatis，Shiro，JWT，Vue & Ant Design。提供强大的代码生成器， 前端页面和后台代码一键生成，不需要写任何代码，保持jeecg一贯的强大，绝对是全栈开发者福音！！ JeecgBoot的宗旨是降低前后端分离的开发成本，提高UI能力的同时提高开发效率，追求更高的能力，No代码概念，一系列智能化在线开发。
3. 后端
   - 基础框架：Spring Boot 2.0.3.RELEASE
   - 持久层框架：Mybatis-plus_3.0.6
   - 安全框架：Apache Shiro 1.4.0-RC2，Jwt_3.4.1
   - 数据库连接池：阿里巴巴Druid 1.1.10
   - 缓存框架：redis
   - 日志打印：logback
   - 其他：fastjson，poi，Swagger-ui，quartz, lombok（简化代码）等。
4. 前端
   - [Vue 2.5.22](https://cn.vuejs.org/),[Vuex](https://vuex.vuejs.org/zh/),[Vue Router](https://router.vuejs.org/zh/)
   - [Axios](https://github.com/axios/axios)
   - [ant-design-vue](https://vuecomponent.github.io/ant-design-vue/docs/vue/introduce-cn/)
   - [webpack](https://www.webpackjs.com/),[yarn](https://yarnpkg.com/zh-Hans/)
   - [vue-cropper](https://github.com/xyxiao001/vue-cropper) - 头像裁剪组件
   - [@antv/g2](https://antv.alipay.com/zh-cn/index.html) - Alipay AntV 数据可视化图表
   - [Viser-vue](https://viserjs.github.io/docs.html#/viser/guide/installation) - antv/g2 封装实现
   - eslint，[@vue/cli 3.2.1](https://cli.vuejs.org/zh/guide)
   - vue-print-nb - 打印
5. 开发环境
   - 语言：Java 8
   - IDE(JAVA)： Eclipse安装lombok插件 或者 IDEA
   - IDE(前端)： WebStorm 或者 IDEA
   - 依赖管理：Maven
   - 数据库：MySQL5.0 & Oracle 11g
   - 缓存：Redis

6. 技术文档

- 官方文档 ： [http://jeecg-boot.mydoc.io](http://jeecg-boot.mydoc.io/)
- 零基础入门： <http://jeecg-boot.mydoc.io/?t=344845>
- 常见问题 ： [新手入门常见问题汇总](http://www.jeecg.org/forum.php?mod=viewthread&tid=7816&page=1&extra=#pid21237)
- 在线演示 ： [http://boot.jeecg.org](http://boot.jeecg.org/)
- QQ交流群 ： 284271917
- 视频教程（视频可能有点老，以1.1文档为准） ： [![YPSuperKey Unlocked](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAYAAABXAvmHAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAADYgAAA2IByzwVFAAAABx0RVh0U29mdHdhcmUAQWRvYmUgRmlyZXdvcmtzIENTNui8sowAAAb7SURBVGiB7ZlrbFTHFcd/M/fu2uvXetcG24ChvIt4mHcIaUlaNVJRH6nUV1K1kapKkSqlVdu0pUqrSG1p+yFIUZt8SdqqrdKWUIkIpZQgEgKYQIAkxhTiAPHbXvxk117vrr17H6cf1jaFALtr8PpL/tKV7p2dc+b855w5c2ZWiQgzBaXUJuAbQB2wGvACl4GzwB4ROZxRiYjk/QHuBV4GegEBpMxfLoFgUAzDkPG2MHAE+CZg3EqXmgEPmKvXrj8c6urctuUT2/js5x9iwaLFlJX60YYmHo/R1dFB/eFDvPbqfgb6+wDeBR4TkYYPacvjrG8FGp781e+aLoYi8mbjJWkdjMuVmCtXYiKhmCuhEWf825WuqCVvnW+Wx3+0Q7xerwBx4Osz4gGl1DrgjUKfr/wvL+1j4z1bMDweUmNJzp9roOHt03S2t+I6LnNr51O3YRNr12/EXx5Aa039kdd54rvfoedKCOALIrI/bx4ASoD2wsJC+dM/90rrYELaBhPy0r8PydZtD0zEuwBJYHTiu279Rnn+xT3SOpiQjqGUHKg/I4FghQBRYPmk/jwQ2AXIU795WrpHbGm7mpBf7/q9mKYpgAX8EXgQWAosAj45LjMMyONP/Eya+0ekM5KUF/7+rwmy+/NCAFgIWOs33SMXQxFpvzoqf3jhbxNGXAY2ZpA9CciOp3ZK29WEdESS8rkvfXlCfms+CPwUkGf//KJ0R205ce6SBCsqhXT6nJ+FfCnQZBimvPLGCekcSsnLh46J1lqA56aVAKCAU7OqquTUe63SHbXlBzt+MTF7385Bz/2A+5VHviXtkTFp6hqUlWvWCnABKNN3mmFuAz+weOXqOqqqa4hGhzn6+kGAHmB3tkpE5BjQcKL+CP29vZSVl7Nh8xaAOcC66SRQDpRXz5mL1pro8BCd7e0AZ0VkLEddpwb6eunv7UFrg6qaOQA+YP50EggAZrCiEm0YjI2OMppIAFydgq5B27ZJJBIgQiAQBCgEqqaTgAZQWqNgIp4hvQZyRVpmQoeaNFtPJwGuG/Qa1BS03CBzTef0E5hmfERgpvERgZnGdBKIA3i8XopLDIqKiifarakq9Pl8lBQrCgoKJttMAKXUUtIbjztlc6+HACsAQl2dnKw/TVdHO67rAlQppTaMjx0Ske4s9GmAC/9txPR4aGn+4Lr2rwEJrh0s8vl0A4EsCrqf30L++yawDPA9sryWDdUBHOduOYHJHVjG35VSCGCaJnve7+BMX2Q2ac9HMqh6gfRJrIh0lBjAFWCfCaQAHl42jy+uXwJjUw7R7FFUSGs4ypm+iEUWYSsiA8CzN/vNnHiJWTaMpiCZAwGtAJUuFz5cMtwaSpG8S56eWhYyNBR6cR2XkbFUOj4KvaCmUubcGczMXf4PAnhNhhJJdh5t5D8tIfoTYywqL+XRVYv43rolgIK7uI4yITcCXpO2cJQH9x6nZTgOvjIK/UHeCQ/yzpFGDrb3su+h+/BoBW5+bvyyJ6AUtuvy6KtnaBmOM3/Nfcxa8HGUNnCsJN1Nb3OgrYlfnrjAzk+tg2RqGs2+huzXgMekvq2XN3vCVCxYQc3SOlzXwbGSKMNg/pqteEuDPNNwmUg0ll4neUD2oxia98JRAAJVtTi2NZl5xHEwDBP/7LkkHKF1OJ6XsxLklIWEMq8HANtKom80UIGVSgKM98vPGsiegOWwbd4sFNDb2oRtpdCmB0QwC3zEIwMMhdpYGShhUbA0b5koewK2w8JZfp7ctJyx4QEunzzA6HAYw1NAJNTCpbcOgmvx9LY6DI+ZtyyUW6CmbHbeX8dPNiwjFu7jygdnQSlaG4+jx+Ls3r6Z7ctrc9vN7xC5ERABj8G9NUEASoPVmB4vxcFq0IoH5laCm79NDNIEvABWVgMrsF2eP9cMKMqra3Edm9nzFpNyhb++3wGmMa0G3wgNHJtX4rtcV+nPvPBMTSgc5Uj3IEWVcygo9mNbSUora8D0sudiJ6SsvNZEWkSOd/34q8+trakAy759b4/JK609pARqPrYcw/SilKawxE9w7mIar45wvi+SVy9opdSWJc/sfexCXwQ8t6kslMK1bP5xsRPQKMNkeKCbWKSf6GAPRSVlAOy+1AVm/u4KTOAzLcPxVe/2D7FqTgXYzs17asVQbJQTPWEAmk8fumm317oG+K3tpsMolzPCFDF5IvPoDHHruvh9XnZv38zF8MhNJ9kR+HTt7HQmyoPxkEs1KumD6MOrF6YLtZvZpwDLgZQ9tSvcKWCSgKlV2rBMRZjlpJ/bIVMlamj0XcpUJuNzNZKyiY0mcZMZMtFdgKEg6WSYhCyhgB8CuwIFHl3sMXHzELtaKcJjKRK2EwNWZHm5dUvUAc3MzMXWUcBzJ/+G/g/y7+AhkzE2IwAAAABJRU5ErkJggg==)https://pan.baidu.com/s/1Il0TS50I70vH1AG1y40wtw](https://pan.baidu.com/s/1Il0TS50I70vH1AG1y40wtw) 提取码：hok5
- Angular版本 ：[如果你更熟悉Angular，请点击这里找到jeecg-boot的对应版本](https://gitee.com/dangzhenghui/jeecg-boot)

7. 功能模块

```
├─系统管理
│  ├─用户管理
│  ├─角色管理
│  ├─菜单管理
│  ├─权限设置（支持按钮权限、数据权限）
│  ├─部门管理
│  └─字典管理
├─智能化功能
│  ├─代码生成器功能（一键生成前后端代码，生成后无需修改直接用，绝对是后端开发福音）
│  ├─代码生成器模板（提供4套模板，分别支持单表和一对多模型，不同风格选择）
│  ├─代码生成器模板（生成代码，自带excel导入导出）
│  ├─查询过滤器（查询逻辑无需编码，系统根据页面配置自动生成）
│  ├─高级查询器（弹窗自动组合查询条件）
│  ├─Excel导入导出工具集成（支持单表，一对多 导入导出）
│  ├─平台移动自适应支持
├─Online在线开发
│  ├─Online在线表单(暂未开源)
│  ├─Online在线图表(暂未开源)
│  ├─Online在线报表
│  ├─消息中心（支持短信、邮件、微信推送等等）
├─系统监控
│  ├─性能扫描监控
│  │  ├─监控 Redis
│  │  ├─Tomcat
│  │  ├─jvm
│  │  ├─服务器信息
│  │  ├─请求追踪
│  ├─定时任务
│  ├─系统日志
│  ├─数据日志（记录数据变更情况，可进行版本对比查看数据变更记录）
│  ├─系统通知
│  ├─SQL监控
│  ├─swagger-ui(在线接口文档)
│─报表示例
│  ├─曲线图
│  └─饼状图
│  └─柱状图
│  └─折线图
│  └─面积图
│  └─雷达图
│  └─仪表图
│  └─进度条
│  └─排名列表
│  └─等等
│─常用示例
│  ├─单表模型例子
│  └─一对多模型例子
│  └─打印例子
│  └─一对多TAB例子
│  └─内嵌table例子
│  └─常用选择组件
│  └─一对多JEditable
│  └─接口模拟测试
│  └─一对多JEditable
│─封装通用组件	
│  ├─行编辑表格JEditableTable
│  └─省略显示组件
│  └─时间控件
│  └─高级查询
│  └─通用选择用户组件
│  └─通过组织机构选择用户组件
│  └─报表组件封装
│  └─等等组件
│─更多页面模板
│  ├─各种高级表单
│  ├─各种列表效果
│  └─结果页面
│  └─异常页面
│  └─个人页面
│─流程模块功能 (暂未开源)
│  ├─在线流程设计
│  ├─在线表单设计
│  └─我的任务
│  └─历史流程
│  └─历史流程
│  └─流程实例管理
│  └─流程监听管理
│  └─流程表达式
│  └─我发起的流程
│  └─我的抄送
│  └─流程委派、抄送、跳转
│  └─。。。
└─其他模块
   └─更多功能开发中。。
   
```

#### hdw-dubbo

- hdw-dubbo微服务化开发平台，具有统一授权、认证后台管理系统，其中包含具备用户管理、资源权限管理等多个模块，支持多业务系统并行开发，可以作为后端服务的开发脚手架。代码简洁，架构清晰，适合学习和直接项目中使用。
- 核心技术采用SpringBoot、Dubbo、Mybatis、Mybatis-plus、Druid、Redis、ActiveMQ、Quartz、JWT Token等主要框架和中间件。前端采用vue-element-ui组件。
- 前后端分离，通过token进行数据交互，可独立部署
- 灵活的权限控制，可控制到页面或按钮，满足绝大部分的权限需求
- 页面交互使用Vue2.x，极大的提高了开发效率
- 完善的代码生成机制，可在线生成entity、xml、dao、service、vue、sql代码，减少70%以上的开发任务
- 引入dubbo服务治理
- 引入quartz定时任务，可动态完成任务的添加、修改、删除、暂停、恢复及日志查看等功能
- 引入API模板，根据token作为登录令牌，极大的方便了APP接口开发
- 引入Hibernate Validator校验框架，轻松实现后端校验
- 引入swagger文档支持，方便编写API接口文档
- 前端地址：<https://github.com/tumao2/hdw-dubbo-vue>
- 演示地址：[http://locahost:8004](http://locahost:8004/) (账号密码：admin/123456)

运行项目

- 1.安装Redis、zookeeper 、ActiveMQ
- 2.启动Redis 、zookeeper、ActiveMQ
- 3.启动MonitorApplication
- 4.启动UpmsServiceApplication
- 5.等待UpmsServiceApplication完全启动后，启动UpmsWebApplication
- 6.默认用户 用户名：admin 密码：123456
- 7.启动前端

### springcloud项目

#### 冷冷 / pig

- 基于Spring Cloud、**OAuth2.0、Vue**的前后端分离的权限管理系统
- 完善登录：账号密码模式、短信验证码模式、社交账号模式均整合Spring security oAuth
- 单点登录：基于Srping security oAuth 提供单点登录接口，方便其他系统对接
- 用户管理：用户是系统操作者，该功能主要完成系统用户配置。
- 机构管理：配置系统组织机构，树结构展现，可随意调整上下级。
- 菜单管理：配置系统菜单，操作权限，按钮权限标识等。
- 角色管理：角色菜单权限分配、设置角色按机构进行数据范围权限划分。
- 动态路由：基于zuul实现动态路由，后端可配置化。
- 灰度发布：自定义ribbon路由规则匹配多版本请求。
- 终端管理：动态配置oauth终端，后端可配置化。
- 字典管理：对系统中经常使用的一些较为固定的数据进行维护，如：是否等。
- 操作日志：系统正常操作日志记录和查询；系统异常信息日志记录和查询。
- 服务限流：多种维度的流量控制（服务、IP、用户等）
- 消息总线：配置动态实时刷新
- 分库分表：shardingdbc分库分表策略
- 数据权限: 使用mybatis对原查询做增强，业务代码不用控制，即可实现。
- 文件系统: 支持FastDFS、七牛云，扩展API几行代码实现上传下载
- 消息中心：短信、邮件模板发送，几行代码实现发送
- 聚合文档：基于zuul实现 swagger各个模块的实现
- 代码生成：前后端代码的生成，支持Vue
- 缓存管理：基于Cache Cloud 保证Redis 的高可用
- 服务监控: Spring Boot Admin
- 分布式任务调度： 基于elastic-job的分布式任务，zookeeper做调度中心
- zipkin链路追踪： 数据保存ELK，图形化展示
- pinpoint链路追踪： 数据保存hbase，图形化展示

#### 老干爹 / Cloud-Admin（复杂）

- Cloud-Admin是国内首个基于**Spring Cloud**微服务化开发平台，核心技术采用Spring Boot2以及Spring Cloud Gateway相关核心组件，前端采用**vue-element-admin**组件。具有统一授权、认证后台管理系统，其中包含具备用户管理、资源权限管理、网关API 管理等多个模块，支持多业务系统并行开发，可以作为后端服务的开发脚手架。代码简洁，架构清晰，适合学习和直接项目中使用。 核心技术采用`Spring Boot 2.0.1`以及`Spring Cloud (Finchley.RELEASE)`相关核心组件，采用`Consul注册中心`，前端采用`vue-element-admin`组件。

- QQ群号：169824183

  访问地址: [http://118.126.104.133:81](http://118.126.104.133:81/)

  账号/密码：admin/admin、

- 前端：

  - https://gitee.com/minull/AG-Admin-v2.0
  - vue

#### fisher

1. github上面

2. 基于Spring Cloud Alibaba,Oauth2,基于VUE的后台权限管理框架,集成了基于MQ的可靠消息的分布式事务解决方案，集成Caffeine和redis分布式多级缓存，集成了Skywalking的APM监控。

3. 技术栈

   此项目是 Spring cloud Oauth2 构建的后台管理系统，计划采用以下技术

   - 注册中心：Nacos
   - 服务网关：Spring cloud-Gateway
   - 配置中心：Nacos
   - 服务调用：Spring-cloud-open-Feign
   - 负载均衡：Spring-cloud-loadbalancer
   - 熔断降级：Sentinel
   - 链路追踪：Skywalking
   - 消息队列：RabbitMQ
   - 权限认证：Spring secruity Oauth2
   - 项目部署：Docker+Rancher+K8S

4. 项目结构说明 

   - fisher-center Eureka服务注册中心,该工程已经删除 注册中心已替换成Nacos
   - fisher-common 公共模块
   - fisher-auth Oauth2 认证服务器 提供token
   - fisher-back 后台管理模块
   - fisher-transcation 基于mq最终一致性实现可靠消息的分布式事务方案
     - fisher-transaction-message 独立消息服务微服务
     - fisher-transaction-sample 基于支付宝转账的演示
     - fisher-transaction-web消息补偿管理后台
   - fisher-monitor Spring boot admin监控以及Skywalking监控
   - fisher-log 日志中心模块
   - fisher-file 文件上传服务,这个服务可以暂时不起，因为前端还没有对接
   - fisher-gen 代码生成模块
   - fisher-starter 自定义封装各种starer 目前封装了日志处理
   - fisher-gateway 后端统一入口，提供动态路由，oauth2的资源服务器

5. 项目运行

   ```
   git clone https://github.com/fanxinglong/fisher
   先配置数据库，然后reids，需要启动rabbitmq,启动nacos,启动sentinel
   启动顺序：最好按顺序启动，不按顺序启动，至少要把网关放到最后启动
   注意：Nacos先修改配置连自己本地数据库，并把nacos的配置数据库导入到自己本地数据库
   导入之后，检查nacos各个微服务相关配置的mysql，redis,rabbitmq配置是否正确
   fisher-auth
   fisher-back
   fisher-log
   fisher-gen
   fisher-monitor
   fisher-transcation
   fisher-file 
   fisher-gateway
   
   前端启动参照前端项目
   
   ```

   ### 

## 博客