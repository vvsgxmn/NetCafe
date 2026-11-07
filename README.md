# 基于SpringBoot+Vue的网咖管理系统

![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![Vue3](https://img.shields.io/badge/-Vue3-grey?style=flat-square) ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![MyBatis](https://img.shields.io/badge/-MyBatis-000000?style=flat-square&logo=mybatis&logoColor=white) 

## 项目介绍

本系统是一款面向网咖门店的综合运营管理平台，针对机位状态不同步、送餐找错座位、会员余额与上机/点餐台账割裂、赛事报名难追溯等痛点，将专区机位、即时开机与预约、吧台点餐配送、余额充值、电竞赛事报名以及呼叫网管工单整合到同一会员账户体系下，支撑从前台消费到后台经营查询的完整闭环。

系统采用 SpringBoot + Vue 前后端分离架构，区分普通会员与系统管理员：会员端完成选座上机、预约取消、吧台下单、赛事报名、资讯阅读与服务呼叫；管理员在数据看板维护区域机位、商品订单、赛事报名、充值工单与公告资讯，并通过 ECharts 观察营收、机位占用与畅销排行。适合作为毕设、课设与门店数字化运营学习参考。

## 主要功能模块

- **用户认证与双角色分流**：会员与管理员统一登录注册，JWT 鉴权；登录后按角色进入会员门户或管理后台，/admin 路由与接口双重隔离
- **会员首页大厅**：展示专区配置、当前上机状态、吧台热销、电竞赛事与网咖资讯入口
- **机位选座与即时开机**：按专区查看硬件配置与实时矩阵，空闲机位现场开机并预扣基础网费
- **预约订座与结账下机**：选择开始时间与时长预估费用；上机结束后结账释放机位，支持取消待上机预约并回滚余额
- **吧台点餐与余额支付**：分类检索饮品零食，购物车下单并填写送餐机位，使用会员余额结算并跟踪配送状态
- **余额充值与流水查询**：选择充值面额核对赠送，个人中心查看充值、上机与点餐明细
- **电竞赛事与战队报名**：浏览赛事详情与名额，提交战队信息报名，支持查看审核状态与退出报名
- **呼叫网管工单**：按机位提交报修/加水/网络等问题，跟踪处理状态与网管回复
- **经营数据看板**：营收 KPI、近七日走势、机位分布与吧台畅销排行，ECharts 辅助门店决策
- **区域机位中台**：维护专区硬件单价与图片、机位矩阵坐标与状态，查询上机记录并支持代客结账
- **吧台与会员账务**：商品分类上下架、点餐订单履约推进、充值明细核对、会员调账与启停
- **赛事资讯运营**：发布电竞赛事与公告资讯，审核报名队伍，处理服务呼叫工单

## 技术架构

- **后端**：Spring Boot + MyBatis-Plus + JWT + Lombok
- **前端**：Vue 3 + TypeScript + Vue Router + Pinia + Element Plus + Vite + ECharts
- **数据库**：MySQL

<!-- screenshots-start -->
## 系统截图

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E7%99%BB%E5%BD%95%E9%A1%B5%E9%9D%A2.png" alt="登录页面" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E7%94%A8%E6%88%B7%E9%A6%96%E9%A1%B5.png" alt="用户首页" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E6%9C%BA%E4%BD%8D%E9%80%89%E5%BA%A7.png" alt="机位选座" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E5%90%A7%E5%8F%B0%E7%82%B9%E9%A4%90.png" alt="吧台点餐" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E7%94%B5%E7%AB%9E%E8%B5%9B%E4%BA%8B.png" alt="电竞赛事" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E7%AE%A1%E7%90%86%E5%91%98%E6%95%B0%E6%8D%AE%E7%9C%8B%E6%9D%BF.png" alt="管理员数据看板" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E5%90%8E%E5%8F%B0%E6%9C%BA%E4%BD%8D%E7%AE%A1%E7%90%86.png" alt="后台机位管理" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E5%90%8E%E5%8F%B0%E7%82%B9%E9%A4%90%E8%AE%A2%E5%8D%95.png" alt="后台点餐订单" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E8%AE%BA%E6%96%87%E5%9B%BE1.png" alt="论文图1" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/%E8%AE%BA%E6%96%87%E5%9B%BE2.png" alt="论文图2" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/netcafe/UML%E5%9B%BE%E5%88%97%E8%A1%A8.png" alt="UML图列表" width="600" />

<!-- screenshots-end -->

---

## 接毕业设计和论文

### 作者微信：vvsgxmn  (支持修改、 部署调试、 支持代做毕设)

### 接网站建设、小程序

### 选题+开题报告+任务书+程序定制+安装调试+论文+答辩ppt 都可以做

### 购买地址：[https://www.vvxx.love](https://www.vvxx.love)（vv毕设网）

### 支持 **一键生成 UML 图**：上传项目压缩包即可自动产出功能模块图、用例图、流程图、E-R 图、时序图等全套毕设图表。

### 提供 **免费配套软件下载 + 安装说明 + 部署教程**

![vv毕设网 - 一键画图](https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/uml-draw.png)

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/image-20260825133349317.png" alt="image-20260825133349317" />

⚠️ Bug添加微信**免费修复**，免费修复。其他平台的私信一律不管（微信方便发送文件）
