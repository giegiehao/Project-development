# **A6-智慧校园-综合服务学工平台 项目目标和需求解析**  
>从官网上可以得到以下内容，加以分析，明确需求。  

[官网链接](http://www.cnsoftbei.com/plus/view.php?aid=802)

>### 一、赛题简介
>#### 1.实现目标
>#### 2.实用价值
>#### 3.涉及技术
>#### 4.整体要求
>### 二、业务场景
>#### 1.适用对象
>#### 2.主要功能
>### 三、要求
>#### 1.基本功能要求
>#### 2.非功能要求
>### 四、实现条件
>### 五、评分项及占比

---
### 一、赛题简介
#### **1.实现目标**
>基于金蝶云·苍穹平台，围绕数字校园、智慧学工、学生关怀的时代趋势，结合学生和教职工的教务需求、协同需求、成长需求，开发构建智慧校园-综合服务学工
> 平台。平台使用全栈式PaaS能力平台引擎，运用当下主流低代码高效开发模式、配置化工作流、数据化服务、智慧服务引擎，全方位打造满足前沿趋势的智慧学
> 工业务系统。

其实我们只要关注两个重点：一个是基于金蝶云苍穹平台的开发（至少实现50%的功能）；二是主题“智慧学工平台”，而对于中间那些属于其它内容，不在这里展开。  
官网还提到**四个主要特点**：  
1.安全高效开发：这里不太需要关注，因为使用平台开发默认就是安全的，如果是开发插件时涉及到安全问题再作相应的处理。  
2.个性化数据服务：这点还是平台提供的数据服务能力  
3.移动开发：pc/移动端的开发  
4.智能化服务：
>借助苍穹AI能力，在学工业务各环节嵌入对话机器人与OCR能力，实现学工业务的智能指引与自助服务。 如在新生报到时，实现业务流程问答，地点指引，学校
> 介绍，班级信息介绍，校车查询，宿舍入住等学工常见业务的指引。在学生申请学生证、一卡通、助学贷款、实验室采购耗材等场景时，通过OCR自动识别各种
> 制式的表格和发票等，实现学生自主申请学生证、助学贷款、费用报销等。  

这里给了一大串貌似有用的东西，可以分析一下  
1. 嵌入对话机器人与OCR文字识别能力，看了一下开发者社区，平台好像也有提供
2. 有新生报到的主页功能
3. 实现学生端可以申请学生证、一卡通、助学贷款、费用报销等功能，对于学生端的这种功能，教师端也要有相应的功能，以审核学生的申请，具体在主要功能子
4. 标题再作详细讲解。  
>关键词：业务建模、数据分析、移动开发、智能服务  
___
#### **2.实用价值**   
>(1) 以“学生服务”全流程闭环管理为抓手，打造从新生报到、校内学务、宿舍、离校等高频交互场景。以规范化、信息化系统提高学生各项业务的管理工作效率
> 和服务质量，建设一体化服务与资源平台，实现信息共享，增强学校内部各部门之间的沟通和协作，提高信息共享。 

这里有个很陌生的概念 **‘全流程闭环管理’**，什么是全流程闭环管理，我们先百度看看
>>闭环管理把全公司的供一产一销管理过程作为一个闭环系统，并把该系统中的各项专业管理如：物资供应、成本、销售、质量、人事、安全等作为闭环子系统，
> 使系统和子系统内的管理构成连续封闭和回路且使系统活动维持在一个平衡点上；另一方面面对变化的客观实际，进行灵敏、正确有力的信息反馈并作出相应变
> 革，使矛盾和问题得到及时解决，决策、控制、反馈、再决策、再控制、再反馈....从而在循环积累中不断提高，促进企业超越自我不断发展。  

“一产一销” “决策、控制、反馈、再决策、再控制、再反馈” 再结合上我们的功能流程，我的理解是
：无论在这个学工平台的任何一个功能，也无论任何一个客户端（学生端，教师端、管理员端），每一个
业务都是完整的，比如，我作为学生在请假申请的应用中申请了一次请假，这个请假申请要让对应的辅导员看到，那么在辅导员的教师端就必须有一个请假审批的
应用，用来审批学生的请假申请，
再把审批结果发给学生，这一次的请假记录也会被后端记录起来。这只是一个功能的闭环管理，要实现全流程闭环管理要求所有功能都有。  
>(2) 借助苍穹移动开发平台，实现学工业务的移动化办公，打破时间、空间的限制，让学生能随时随地处理业务，享受到更加便捷、快速、高效、贴心的服务体验。  
> 
> (3) 将学工业务数字化沉淀，使校内业务数据有效汇集、融合，打通综合分析的数据壁垒。借助苍穹平台多维度数据分析与可视化模型，立体式呈现学生画像与
> 行为偏好，提供更精准的教育服务和个性化辅导，促进学生的全面发展。动态配置的规则结合业务健康度指标，为学工业务趋势分析与预警提醒提供数据支撑，
> 让学工业务进展和运营状况能够可视化的呈现，为学工业务监控、分析决策、环境安全提供有效保障。  

这乍一看感觉很抽象，说了很多但是不知道说了什么，值得我们好好思考一番。  
首先，第三点给我的第一感觉就是网络监控，推荐每个人所关注的东西。如果用在学工平台上，可以根据学生的成绩提供学生感兴趣或者可以提高成绩的信息。
关于 **“业务健康度指标”** 看看gpt怎么说  
>>业务健康度指标是指用来评估某个业务运营状况和发展趋势的指标体系，其目的是为了评估业务的健康状况并提供数据支持，以便及时发现业务异常和风险，
>>并采取相应的措施进行调整和改进。常见的业务健康度指标包括但不限于以下几个方面：  
>>
>>1.用户量和活跃度：包括用户数量、用户增长率、用户留存率、用户行为等。  
>> 
>>2.收入和盈利能力：包括营收、利润、毛利率、净利润率、ARPU 等。
>>
>>3.客户满意度和品牌价值：包括用户满意度、品牌知名度、口碑评价、客户反馈等。
>>
>>4.业务效率和运营效果：包括业务响应时间、效率、运营成本、运营效果等。
>>
>>通过对这些业务健康度指标的监控和分析，可以及时发现业务运营中的问题和风险，进而采取相应的措施进行调整和改进，保证业务的正常发展和健康运营。  

可以看出，其中包括 **业务效率和运营效果**、 **用户行为**，前者用于判断应用本身的业务能力，后者则与前面提到的网络监控有关，有利于给特定的人群
推荐感兴趣的消息。  

在哪些方面可以用到用户行为监控并且实现信息推荐：例如在学工平台的主界面，主界面上的内容可以根据用户的常用应用而更改，比如，我经常使用‘本周课表’
这个应用，系统就可以监控到这一用户习惯，在我下次打开页面的时候，将‘本周课表’放在考前的位置，让我能比较容易的看到它；再比如，在学工平台的论坛
区，我经常看关于Java的小知识，在我刷新或者下一次进入，系统就能根据我的爱好,给我推荐关于Java的帖子。  

___

#### **3.涉及技术**
>云原生框架、低代码开发、对话机器人、柔性工作流、领域模型设计、多源数据分析 ； 

___

#### **4.整体要求**
> 要求参赛选手使用金蝶云·苍穹低代码开发平台，使用云原生、低代码、领域模型设计以及事件驱动技术，利用其中的表单模型、服务模型、
> 流程模型、报表模型、权限模型等，适当结合苍穹平台的数据分析、移动开发、集成能力、AI能力来开发构建应用。   

比赛要求使用苍穹平台至少开发至少50%的内容，这个要求我们基本上是可以达到，毕竟里面很多的服务云是我们很难去实现的，
使用平台上的云服务可以让我们 快速的把应用开发出来，而在平台的基础上，我们可以自己做插件。

___

### 二、业务场景  
#### 1.系统适用对象  
>学生处管理员、院系负责人、教师、学生。  

- 各对象的大致需求
>1、学生处管理员：学工事务管理、查询、学生信息审核；
>
>2、院系负责人：学员画像、学员动态、教务审核；
>
>3、辅导员：学生信息、学工事务查询、学员评估；
>
>4、学生：学工事务申办、个人相关信息查询；  

官网上列出来的需求其实非常高度总结，比如说学生需求中的’学工事务申办‘，里面就可以包括‘请假申请’、‘水电费缴纳’、‘校巴预约’、‘实习证明’
等等很多的应用，要如何从高度总结的需求中一点一点拆分出精细的需求正是我们要做的需求分析，从而做出满足需求的应用功能。 

其实对于需求分析，如何能够快速知道一个项目要满足哪些需求，除了用户直接告诉你之外，最好的方法就是自己成为用户，比如说我是学生，
我想在这个学工平台看到每天的课表，我可以在上面请假，我可以在上面看到今天作业，我还想看一些有关专业的知识、资讯等等。 我自己是用户，
我希望这个软件给我带来什么，这个软件要帮我什么，我要让这个软件干什么，这些都是能从“我”身上知道的。

___

#### 2.系统主要功能  
>学生信息、迎新管理、学生工作、宿舍管理与离校管理
>
>1、学员信息管理：学生档案维护、档案查询、学籍调动申请、个人违纪处分等查询。辅导员、院系组织/负责人等管理与维护；
>
>2、迎新管理：预报到登记、接送与寄存、信息服务（学校概况、校园地图）、 报到行政流程（培训、安全）、现场接待活动；
>
>3、学生工作：学生证办理、校园卡充值、学籍成绩、学生奖惩（奖学金、荣誉称号、违纪处分等管理）、资助发放（困难生、助学金申请、勤工助学管理、
国家助学贷款等管理） 、学情测评、学员健康、学员通报；
>
>4、宿舍管理：学生住宿信息及查询、宿舍卫生检查、宿舍违纪管理、宿舍报修、网络服务、假期留校管理等；
>
>5、离校管理：准毕业生管理、离校事项、离校办理等；
>
>6、数据分析：学员画像、上课情况、考试成绩等数据进行数据集成与分析，通过平台反馈的数据对学生工作进行分析，为学生工作提供数据支撑；

单从功能数量来看，官网中要求我们实现的功能其实并不是特别多，但是作为开发者，我们在一个功能中需要考虑的事情就非常多，
比如学员信息管理应用中的学生档案维护的功能，要维护学生档案，**首先**需要收集录取学生档案，那就涉及到另外一个问题，
如何把纸质档案到保存数据库中？手动打字是不可能的，工作量特别多，直接拍照也不可取，不利于以后的档案调查等，所以这里就可以使用ocr文字识别技术，
通过ocr把每一份档案以文字数据保存到数据库中。**其次**就是对于档案的管理，增删改查，以数据可视化的界面展示给档案管理员，
管理员可以在客户端查看某一年入学的所有学生档案，或者修改某一个学生档案，也就是说在这个界面中要有筛选条件；**最后**要思考这一个应用的使用者是谁，
档案这种属于高度保密的东西，不应该会被其它学生或者无关人员看到，所以没有必要把这个应用入口开放给学生端的账号，只要开放给档案管理员就好了。  
总的来说，每一个应用下都有很多功能，每个功能又有不同实现方式，但是无论如何设计都不要离开一个原则，就是要使用户使用起来觉得很方便。 

下面我将展现一部分功能的实现建议和实现方法：（暂时无涉及苍穹云所提供的服务）

|         功能         |                 建议                 |    实现技术 |  
|:------------------:|:----------------------------------:|--------:|
|       学生档案维护       | 档案收集、档案增删改查、条件筛选（属性）、<br/>导出；档案负责人 | 数据库、orc |
|        档案查询        |         条件筛选、档案导出  ；档案负责人          |     数据库 |
|       学籍调动申请       |            申请表单、调动证明；学生            |  数据库、单据 |
|     个人违纪处分等查询      |    查询条件（时间段等）；辅导员可查本班学生，学生仅可查自己    |  数据库、单据 |
| 辅导员、院系组织/负责人等管理与维护 |     查询条件（班级、辅导员等）、数据导出；可对所有人开放     |  数据库、单据 |
|       预报到登记        |信息填写、报到时间；学生|  数据库、单据 |
|       接送与寄存        |信息填写、申请记录；所有人开放|  数据库、单据 |
|信息服务|学校概况、联系电话、校园地图；所有人开放|    静态页面 |

暂时写到这里，主要是越写越发现有问题，比如对苍穹的服务不了解，不能完全说出来可以使用哪一个苍穹服务解决问题，对帮助开发实际用处不大，
而且实际技术中大多包含数据库的设计，内容比较庞大，暂时不能只靠我一个人完全做完，但是在实际的开发过程中数据库设计是重要的一步，需要我们细细斟酌。

___

### 三、要求
#### 1.基本功能要求  
>1、要求参赛作品功能完整，业务可以形成闭环，使用过程中不出现明显的报错以及不明提示；
>
>2、针对特定业务场景可熟练应用表单模型、流程模型、服务模型和报表模型等建模工具进行微服务架构的自定义应用；
>
>3、通过引入云计算平台、云服务、大数据、集成、AI与云应用开发等实际应用场景，实现应用建模、服务组件、数据可视化应用、开发服务、运行服务、
服务管理、云支撑服务与运维服务等能力。

---
#### 2.非功能性要求
>1、系统运行顺畅，无明显卡顿、闪退等严重BUG
>
>2、UI界面美观、简洁、操作顺畅
>
>3、高并发、高可用能力设计考虑
>
>4、要求原创，禁止抄袭

---
### 四、实现条件
>开发环境：金蝶云·苍穹低代码PaaS平台
>
>开发语言：JAVA
>
>数据库： postgresql

--- 
### 五、评分项及占比

>创新性（20%），数据分析应用能力（10%），功能完整性与平台服务运用能力（50%），用户体验（10%），综合表现（10%）





