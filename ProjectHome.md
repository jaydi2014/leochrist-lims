# 背景 #
> 随着实验室的开放和实践教学体系改革的深入以及数字化校园建设的快速发展，数字化和网络化管理成为实验室管理的发展趋势。B/S结构的实验室信息管理系统以其时效性强，资源共享性高等特点倍受青睐。

> 实验室是实践教学的主要阵地，有大量的信息需要搜集、整理、汇总、发布、上报，例如实验室基本情况(面积、地点、功能等)、人员、实验项目、仪器设备、实验室规划等等。目前还有很多高校仍然在使用单机版实验室管理系统，对信息的管理存在诸多无法克服的缺点。（1）共享性弱，数据资源难以共享和统一管理，信息封闭。（2）时效性差，数据信息过时，不能及时更新。（3）维护困难，大量的信息需要实验室管理人员录入，工作量非常巨大。

> 网络版的实验室信息管理系统完全克服了上述的弊端，在网络环境下实现数据的录入、修改、删除、查询、统计、更新、打印等功能。具有如下特点：（1）共享性强，信息资源采用统一的数据管理模式，通过网络就可以实现数据资源的共享，随时随地的对资源库内的信息查询和浏览。（2）时效性好，信息数据能够实时更新，只要具有一台能够上网的计算机，就可以随时随地的维护实验室信息，实现实验室信息的实时性。（3）维护容易，大量的实验室信息可以由相关人员通过网络录入维护。极大的减轻了学校实验室管理人员的工作量，同时提高了实验室信息系统的维护性。在实验室信息量迅速膨胀和管理手段落后的窘境下，网络版实验室信息管理系统的开发应用将成为解决问题矛盾的有效途径。

> 基于网络的管理系统有C/S和B/S两种模式。C/S模式需要专门的客户端安装程序，分布功能弱，针对点多面广且不具备网络条件的用户群体，不能够实现快速部署安装和配置；兼容性差，对于不同的开发工具，具有较大的局限性；若采用不同工具，需要重新改写程序；开发成本较高，需要有一定专业技术水准的技术人员才能够完成。B/S模式具有分布性特点，可以随时随地进行查询、浏览等业务处理；业务扩展简单方便，通过增加网页即可增加服务器功能；维护简单方便，只需要改变网页，即可实现所有用户的同步更新；开发简单，共享性强。

# 工作目标 #
> 通过对研究现状的调研与分析，可以得到本论文的工作目标是：设计并实现高校实验室信息管理系统，使其能够满足信息管理、工作管理、设备管理和提示预警服务功能。能够为实验室信息提供网络化管理平台。

# 工作内容 #
> 为了实现工作目标，本论文把工作内容划分为四个组件：信息管理、工作管理、设备管理和提示预警服务，之后将分别对各个组件进行详细说明。

# 信息管理组件 #
> 信息管理组件是对个人信息、项目信息、论文检索等相关信息的集中管理。根据使用者的身份进行查询限制，对于未登录的用户限制查询内部信息，对于登录查询权限不够的用户，限制查询保密信息。
在这里直接将使用用户区分为三类，普通页面浏览者，即未登录用户；实验室内部人员，即普通登录用户；实验室内部管理人员，即拥有密级权限登录用户。

# 工作管理组件 #
> 工作管理组件是实验室信息管理系统对实验室日常工作管理的组件。在这里可以对实验室项目进行创建和删除，项目小组组建和解散，项目组长任命等行政工作。同时也可以对项目小组人员的工作进行安排、汇报，另外项目组长还可以向上级进行项目总情况的进度汇报。
在这里的使用用户限制为实验室信息内部使用人员，对游客不开发。

# 设备管理组件 #
> 设备管理组件是本系统简单的后勤管理组件，拥有实验室管理员对人员设备使用情况的具体核实和设备损坏的上报功能。为提示预警服务组件提供逻辑判断信息。
在这里的使用用户限制为实验室信息内部使用人员，对游客不开发。

# 提示预警服务组件 #
> 提示预警服务组件是实验室信息管理系统在收集到大量数据后对使用人员的辅助支持组件。当使用人员填写相应的时间安排表，该组件将会根据需求给予适时的提醒或预警。例如：填写了工作安排表，在工作时间快要结束时会提示工作截至时间。在填写了实验室设备损坏上报表后，系统将向实验是管理者给予设备预警信息的提示。
在这里的使用用户限制为实验室信息内部使用人员，对游客不开发。

# 拟采取的技术路线 #
> Struts2 + Spring + Hibernate + J2EE框架。

> Velocity、Javascript、Ajax实现页面表现层。

# 技术难点 #
> 创建合理优化的数据库表及数据信息的维护；
> 用户使用过程中的权限管理；
> 系统内外网信息交互及信息安全；
> 系统提供的服务功能及定义。