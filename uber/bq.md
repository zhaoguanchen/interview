# Self Introduction

 **I am Guanchen Zhao. I graduated from University of Science and Technology Beijing in 2018 with a bachelor's degree in Computer Science and Technology.**
**In order to learn some industrial experience, I started to work at eCart. My position is a software engineer, mainly responsible for the development of data architecture.** 

**After a year or so, I came to Yuanbao, a startup company. At the beginning, I worked as a software engineer and was involved in the development of crm. Then, I started to work on the new system - css as the person in charge. My team consisted of 2 junior engineers.**
**Last fall, I came to the US for graduate school. And graduated in spring this year with a maser degree  in Computer Sicence and Systems.**

# why uber?

Uber 让乘客和司机更方便。乘客可以在手机上管理自己的行程。对于我来说，更重要的是我能知道多少钱。司机可以轻松的在driver client app上安排自己的工作和路线。

同样的，对于客人和餐厅来说，Uber eats发挥着很大的作用。

因此，我认为，uber是一家改变了世界的公司。我非常希望加入他。

**Uber makes it easier for riders and drivers. Passengers can manage their trips on their phones. For me, it's more important that I can know how much it costs. Drivers can easily schedule their jobs and routes on the driver client app.** **Similarly, for guests and restaurants, Uber eats plays a big role.** **Therefore, I think uber is a company that has changed the world. I am very eager to join him.**



**About this position, I learned that it is Platform Engineer which will build and maintain backend services and solutions to support user-facing products, downstream services, or infrastructure tools and platforms used globally. Although it is not user-oriented, it is really the most important. It plays an important role in the stability of business applications and the efficiency of development within the company.**





# chanlenge



# disagree



ownership delever resultbackbone insist on high standardinvent and simplify
缺点  强迫症  总是聚焦在细节上，会影响整体进度。特别是deadline不紧张的时候，

【跟上司观点不同】单点登录，上司说不接。我经过调查研究，发现可以。跟他们提了一些问题和方案。最后成功接入。提高了账号的安全性。在确认方案后，我调整了任务分配，让组里一个工程师来着手做这个事情，这也是对他的一种锻炼，当然我会全程把握进度和代码质量。结果是非常好的，我们在10天内完成了这部分改造。

【挑战】对接呼叫中心。我觉得最有挑战性的是将对方的系统设计研究明白，并能够跟自己的业务结合起来。在做呼叫中心的时候，我们对接的是ZTTH提供的服务。

你知道有时候不能单单通过接口文档来了解功能，你需要站在他们的角度上来思考会怎么设计。最令我印象深刻的是，有一次我们需要根据用户的按键输入来进入不同的处理逻辑。当大家都不知道怎么做时，我发现了一个自定义参数的东西。

I think the most challenging part is to study and understand the other party's system design and be able to integrate it with your own business. When we were doing the call center, we were interfacing with the service provided by ZTTH.

You know sometimes you can't understand the functionality through the interface documentation alone, you need to put yourself in their shoes and think about how it will be designed. What struck me most was the time we needed to access different processing logic based on the user's key input. When no one knew how to do it, I found a custom parameter thing.

**custom parameter**



设计多机构用户菜单系统（疫情初期，比较混乱）（saas）。中间发现了一个问题，最后设计上企业，部门，人员，角色，菜单的体系。项目正常上线。学到了要预先排查可行性。





# mistake

I took responsibility for this incident.

在客服系统开发的后期，我的团队开始壮大。有的需求我会交给新人的同事来做。有一次一个简单的需求，通过短信的结果回调来变更数据库中的短信发送记录状态。实现方法比较简单，我们团队用了3天时间就完成了开发与测试。然而第二天9点噩梦开始了。数据库集群出现了大量的慢sql，导致CPU占用率达到了100%，进而导致了线上服务不可用。作为负责人，我第一时间进行了响应。经过查看报错信息，很快确定了原因。首先对版本进行了回滚，消除影响。然后联系运维部门的同事对数据库进程进行处理。在半小时内解决了问题。问题的原因是在生产数据库，涉及到的字段没有添加索引。为什么测试过程没有发现这个问题？因为只有并发较高的时候才会出现阻塞，而我们都忽略了这一点。作为项目负责人，我对此有很大的责任，即使不是我亲手写的。 由我对此次事故进行了复盘总结，并在之后的一次会议上向部门做了汇报。为了保护新人的积极性，我没有将责任归咎到开发者身上。我学到了永远要确认确认再确认，增加性能测试。





短信模版 业务会提一些批量发送短信的需求。我觉得我们不能单单做这一个简单的需求，而应该站在更大的角度系统的设计功能。经过与产品团队以及业务（客户）进行充分沟通，我们一致认为应该做一个短信服务。我们确定了短信的类型， 模版的构建以及相应的参数填充，并由我进行后端的开发，同时与前端和测试团队进行协调以及功能设计的同步。经过2周的努力，我们这个功能上线，客户工作的灵活性大大提高，日短信发送量提高了约300%。





【主人公】审视已有功能。发现有很多功能不再使用或者设计上已经过时。作为项目负责人，我会常常查看项目代码的运行情况。定时任务导致内存偏高，



会后我会进行了解，又一次我发现产品设计有问题（接口设计有问题））运营   要匹配用户进行广告推送，数据量很大（超过百万），利用mysql及Java服务做耗费性能（内存占用），有out of memory风险。  应该由大数据部门做，但需要时间。新启动一个服务，采用分片方法查询数据。后续大数据部门接口准备好后，切换数据来源接口。



 因为创业公司的特点，机会总是稍纵即逝。因此我们常常被要求快速的完成一些需求。因为我们不做，其他公司会推出产品并抢占市场。Because of the nature of startups, opportunities are always fleeting. So we're often asked to get something done quickly. Because if we don't do it, other companies will launch their products and grab the market.



运营   要匹配用户进行广告推送，数据量很大（超过百万），利用mysql及Java服务做耗费性能（内存占用），有out of memory风险。  应该由大数据部门做，但需要时间。新启动一个服务，采用分片方法查询数据。后续大数据部门接口准备好后，切换数据来源接口。做大屏展示。涉及到数据实时更新，研究websocket技术，做数据推送。



 **customer obsession’**
作为内部系统的开发者，我们的客户其实主要是我们的客服人员。作为技术的负责人，我总是跟他们保持着良好的关系和密切的沟通。我常常跟产品经理一起去跟他们沟通业务需求。
有一次他们提出了一个需求，提供一个全量订单的展示页面，这意味着我们需要以分页的方式从数据库中查询数据。因为我们的订单表数据有好几千万，这样的查询十分影响性能。由于查询较慢，客户需要等待几秒，非常影响体验。在充分了解需求后，我了解到他们只是需要根据一些特定的信息才查询某个客户的订单，比如名字，ID，订单号。在我的建议下，我们将这个功能改为了精确查找。这样我们可以通过mysql的索引来进行快速匹配，页面响应速度提高到了100ms以内，开发周期也大大缩短。
As an internal system developer, our customers are actually mainly our customer service staff. As the technical lead, I always maintain a good relationship and close communication with them. I often go with the product manager to communicate with them about their business needs. 
One time they raised a requirement to provide a display page for full volume orders, which meant we needed to query data from the database in a paginated way. Since we had tens of millions of order table data, such a query was very performance-intensive. Due to the slow query, customers had to wait for several seconds, which was very impactful to the experience. After fully understanding the requirements, I understood that they only needed to query a particular customer's order based on some specific information, such as name, ID, order number. With my suggestion, we changed this feature to exact lookup. This allowed us to do a quick match through mysql's index, and the page response speed improved to within 100ms, and the development cycle was greatly reduced.

有时候一些其他部门的同事会向我们提需求。有一次，AI 部门向我们提出了数据到导出的需求。他们希望对客户投诉的录音数据进行分析，来发现其中影响客户体验的因素。这本来应该是大数据部门的工作，由于大数据部门没有人力，他们找到了我。因为数据是非常隐私的东西，我拒绝了直接通过数据库导出的方式。我为他们设计了一个Restful接口，他们可以通过http调用来根据参数获取想要的数据。为了接口的安全起见，我为这个接口添加了鉴权。虽然他们表示这加大了他们的开发任务，但最后还是接受了这个方案。因为系统安全和数据安全是红线。最后，我用了1天时间完成了开发，并协助测试团队完成了测试，仅仅用时两天就完成了上线。
Sometimes some colleagues from other departments will ask us for something. In one case, the AI department came to us with a request for data to export. They wanted to analyze the recorded data of customer complaints to find out the factors that affect the customer experience. This was supposed to be the job of the big data department, and since the big data department didn't have the manpower, they approached me. Because data is very private, I refused to export it directly through the database. I designed a Restful interface for them, which they could call via http to get the desired data based on parameters. For the security of the interface, I added forensics to this interface. Although they said that it increased their development task, they finally accepted the solution. Because system security and data security are red lines. In the end, I finished the development in 1 day and assisted the testing team to complete the testing and went live in just 2 days.

运营   要匹配用户进行广告推送，数据量很大（超过百万），利用mysql及Java服务做耗费性能（内存占用），有out of memory风险。  应该由大数据部门做，但需要时间。新启动一个服务，采用分片方法查询数据。后续大数据部门接口准备好后，切换数据来源接口。



# 问题



1 . 我知道你已经在Uber工作了5年了，这非常了不起。如果我问你你why Uber， 你会怎么回答？

 I know you've been working at Uber for 5 years, which is pretty impressive. If I asked you WHY Uber, what would your answer be?