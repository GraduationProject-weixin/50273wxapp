# [首页查询更多项目](https://github.com/GraduationProject-weixin) 包安装运行


# 50273wxapp微信小程序的刷题系统的设计与实现+springboot

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)]()


# 绪论
## 1.1课题开发背景
网络和科技的进步以及人们生活条件的提高都让微信小程序技术越来越平民化，深入日常生活中。网络更是成为生活的必备条件，大到国家单位、科研项目，小到大街小巷都充斥着网络的身影。在日常办公中，计算机起到了文字编辑、打印、信息检索、统计等的作用。使用计算机可以使日常繁杂的信息进行科学的加工，使信息变得更加的有序、可利用。计算机技术已成为热门。

正是因为网络、科技、计算机技术使现代人的生活和工作变得便利、轻松，给实体行业带来了巨大的冲击。学习也遇到了前所未有的挑战。现如今，对于试题信息的管理有很多的局限性，究其原因是因为刷题的根本是信息的运动。在新时代的环境下，传统的管理方式不再满足用户的需求，难以管理现代的工作。传统的管理方式不仅跟不上时代的发展，还不能实现最基本的工作要求，例如对于试卷的传递还停留在打印大量的纸质文件，发到学生手里进行填写，这种方式对于结果统计非常不便，效果也非常不好。对于基本工作信息的管理也还是采用人工管理，人工管理出错率大，效率低。对于信息的传递都需要经过多人审核才可以完成，想要定期进行分析和总结更是难上加难。因为每种信息之间的关系错综复杂，在定期的统计和查询中就会出现重复出现的问题，对工作人员来说工作压力非常大。
## 1.2课题研究现状
现在刷题已有一些学校使用了基本的管理软件，这些软件都是依靠客户端，只可以特定人员使用，不能实现信息的共享。虽然可以帮助工作人员减少工作量，但从根本上还是无法满足用户的需求。这些软件都还是基于网络发展之初的要求，没有利用现代网络的技术，体现不了更为实用的功能。依靠客户端的系统开发时没有考虑园际化的问题，所以也满足不了国际化的要求。最近几年来，我国网络快速发展，传统的管理方式也越来越适应不了新时代的要求，在处理大量信息时表现不足，开发一个依托现代技术、网络技术的基于微信小程序的刷题系统迫在眉捷。这类系统将会改变刷题的现状。
## 1.3课题开发目的与意义
想要改变传统刷题的现状，就需要采用更为先进的管理方式。本基于微信小程序的刷题系统就是在新时代发展下开发的。本系统的开发非常有意义，体现了行业的创新。本系统是以信息管理为主导，而信息管理就是行业最大的问题，可以极大的提高工作效率。试题信息的信息化管理是目前刷题管理的核心，解决了信息化的问题就可以使刷题管理工作更进一步。开发本系统可以使试题信息更加的清晰、透明，便于管理人员操作。使用本系统可以使管理工作实现部分自动化，减少人工，提高正确率。

本系统是将网络技术和现代的管理理念相结合，根据试题信息的特点进行重新分配、整合形成动态的、分类明确的信息资源，实现了刷题的自动化，减少人工管理过程，为管理人员的决策提供帮助。使用新型的管理系统已成为时代的标志，本系统可以提高学习的竞争力，提高考试质量，使工作人员的管理工作更加轻松。
## 1.4课题开发主要内容
本课题的主要内容包括管理员和用户两个部分，管理员负责考试相关信息的管理，包括试卷信息、试题信息的管理，还可以管理用户信息、知识点信息和科目类型信息、考试信息。用户可以在线学习知识点和收藏知识点、管理错题本、在线考试和刷题。本基于微信小程序的刷题系统满足了用户和管理人员两方的要求，符合了信息化现代的要求。
## 1.5论文结构安排
本论文分为四个部分，摘要、外文翻译部分，目录部分，正文部分和致谢、参考文献部分。其中正文部分包括：

1. 绪论，从课题开发的背景、现状等进行阐述证明课题开发的意义和目的；
1. 系统分析，从系统开发可能遇到的所有问题进行提前分析，确定系统设计时可以进行解决；
1. 系统设计，进行系统功能的设计和数据库的设计；
1. 系统实现，进行系统界面和功能的详情实现阐述；
1. 系统测试，测试部分为正文的最后一部分，此部分是保证系统准确性、稳定性的重要方法。

























# 第2章 系统分析
## 2.1系统使用相关技术分析介绍
本基于微信小程序的刷题系统采用微信端和服务端结合的方式。在服务端采用myeclipse软件进行调试运行，在代码编写中采用java语言，数据库采用mysql软件。加入了springboot框架。微信端采用微信开发者工具。以下分为几节进行阐述。
### 2.1.1Myeclipse环境介绍
Myeclipse是一个非常实用的一个javaee开发平台，兼容性非常的强，可以支持各种框架和数据库，比如servlet，struts,sql,mysql等。目前用于开发javaee的平台主要分为eclipse ，myeclipse和idea三种，而每个都有自己的优缺点，首先是eclipse，属于一个开源软件，开源免费使用，而且对硬件要求不高，占用内存很小，但是最大的缺点就是自带的插件很少，如果需要开发项目，需要自己单独安装和配置所需要的插件，对于新手来说，是一个非常大的挑战，所以目前使用eclipse进行开发的技术人员越来越少。而myeclipse软件最大的不同就是集成了开发javaEE所需要的所有插件，比如jdk，tomcat，可以直接使用，不需要单独进行配置，对于新手来说非常的友好，而且还可以直接进行编码，测试，然后发布。而idea跟myeclipse功能差不多，最大的特点是增加了智能助手，开发过程中可以进行代码提示，自动检查，更加的智能化，但是最大的缺点就是对硬件方面要求比较高，而且比较占用内存。所以综合考虑，还是使用myeclipse进行软件开发是比较适合的。
### 2.1.2Java语言介绍
Java语言跟c++语言非常的相似，可以说是从c++上进行衍生出来的一个新型开发语言，他充分吸收了其他语言的优点，而避开了它们的缺点，使编程语言更加的简单，而且java系统非常的小，摒弃掉了之前的运算符重载，然后造成的卡顿现象，然后添加了垃圾自动清理，增加了开发的简单和可靠性。当然了java最大的特点是平台独立性，只要可以支持java虚拟机环境，就可以直接运行所有程序，而且还是面向对象开发的技术，有很好的封装行，采用了动态编码技术，可以使程序更好的呈现。可以多线程进行运行，用户随时可以加入新的 实例然后不影响整体程序执行，使开发更有灵活性，因为java是在公共密钥技术上进行建立开发的，所以也有一定的安全保障，除此之外，还有一定的跨平台性，可扩展性等优点，可以和不同的操作环境进行互联共享，所以java语言是目前使用最广泛的一个语言开发技术。
### ` `2.1.3Mysql数据库介绍
Mysql数据库最初是由瑞典MySQL AB公司进行开发出来的，后来被SUN公司进行了收购，然后进行了一系列的优化改进，最后被oracle公司收购。mysql数据库是一种关系型数据库，而且采用的是开发式结构，支持大多的平台，而且功能很多，性能很高。Mysql数据库最大的特性就是把自己所编译好的数据进行单独存放，而不是跟传统数据库一样，全部放到一起，这样的话就保证了数据的安全性和灵活性，大大的提供了数据的访问速度，当用户需要调取数据时候可以直接通过sql语句进行查询。Mysql的数据存储非常的稳定，而且是一个开源代码，使用成本非常的低，最大的特点就是安装包非常的小，对硬件没有特别要求，不会造成硬件卡顿，非常便于维护。Mysql还支持多种语言，比如php ，安卓等，都可以支持数据存储。
### 2.1.4微信开发者工具
本工具是用来开发微信小程序的应用软件，通过本应用软件可以运行借助微信软件的项目。微信开发者工具为开源的软件可以在网上找到下载地址，安装包包括32位和64位，安装时非常简单，也不占用电脑内存。微信开发者工具是现在开发公众号、小程序最常用的工具。
## 2.2系统需求分析
在当今信息化社会发展的条件下人们越来越追求自动化，刷题做为提高学习成绩的主要方法越来越受欢迎。这种情况下就造成试题内容的多样化，如果还是采用传统的管理方式势必会造成信息统计的复杂，工作人员的烦躁，使学习的效果降低。

本基于微信小程序的刷题系统采用b/s框架进行设计，结合网络的技术，可以单独运行，不再需要固定的客户端。可以实现试题信息的快速管理，同时可以保证考试质量，提高信息统计的效率。
### 2.2.1系统性能要求分析
系统的性能要求包括服务器和客户机两部分，主要是对系统存储和后续存储的要求，还有对系统运行的速度和系统的安全性进行考虑。

`　`对于系统的性能要求还需要操作的流畅性、理解性以及可靠、维护性。用户使用本系统时要求系统非常好理解，便于用户的操作。售后人员使用本系统时要求系统可读和便于测试。可靠性则指的是系统的准确和运行稳定，在尽可能的情况下利用所有的工具可以使上述要求得到最大的满足。
## 2.3系统可行性分析
可行性分析主要是分析本系统是否有开发的必要性，是否存在开发难度，是否能实现一定的商业价值，所以主要是从技术可行性，经济可行性，法律可行性等方面进行研究分析。
### 2.3.1技术可行性
开发本系统采用目前比较主流的java开发语言，具有很好的扩展性和平台兼容性，而且功能非常强大，易操作。页面技术采用jsp技术，jsp可以实现动态编码，通过html进行页面效果呈现，最大的特点就是本系统采用b/s框架进行开发，b/s可以不受本机系统的限制，可以把数据存放到服务器，用户可以直接通过浏览器进行系统访问，对于用户来说非常的简单省事。本系统采用移动端基于微信的小程序，不需要安装其它软件，非常简单。所以从技术层面考虑是非常可行的。
### 2.3.2法律可行性
本系统没有抄袭市面上的任何网站系统，不管是界面风格，还是后台代码，都是自己原创，所以不存在版权方面的纠纷，而且开发环境都是开源的，开源共享的，所以不管是硬件方面还是软件方面都不存在侵权行为，在法律上是完全可行的。
### 2.3.3操作可行性
本系统采用的全是可视化操作界面，不管是对于系统的管理者还是用户者，都可以在没有任何编程背景的基础下进行系统操作，而且系统界面还存在各种功能提示，用户都可以简单操作，所以在操作可行性上是可行的。
## 2.4系统流程分析
本系统的流程为先进行登录，登录选择不同的身份，选择管理员身份可以对试卷信息管理，可以审核试题信息，对学生信息、科目类型的信息进行管理等；选择学生身份可以在线进行考试以及学习知识点、管理错题本、收藏记录等。用户登录流程图如下图2.1所示：

![](/md/blog.001.png)

图2.1用户登录流程图

学生考试的流程图如下图2.2所示：

![](/md/blog.002.png)

图2.2学生考试流程图

系统操作的整体流程如下图2.3所示：

![](/md/blog.003.png)图2.3系统操作流程图
## 2.5系统用例分析
本系统的主要角色为管理员和用户，管理员的用例包括用户管理、知识点管理、科目类型管理、试题管理、试卷管理、系统管理和考试管理。管理员的用例图如下图2.4所示：

![](/md/blog.004.png)

图2.4管理员用例图

用户的用例包括浏览试卷信息、在线考试，查看成绩和知识点，并且可以管理自己的错题本，收藏信息和考试记录。用户用例图如下图2.5所示：

![](/md/blog.005.png)

图2.5用户用例图




# 第3章 系统设计
## 3.1系统总体结构设计
一个好的设计不止是功能完整，操作流畅，还要符合用户的审美和界面的友好。在进入正式系统实施前，不可缺少的步骤为系统的总体结构设计，本系统为实用性的系统，所以开发的功能都是针对试题信息相关的。本系统的结构可以分为管理员界面和用户操作界面。在管理员界面主要内容是试卷、试题、用户信息、科目类型、考试信息等，学生的主要功能是考试和刷题。本系统的总体结构图如下图3.1所示：

![](/md/blog.006.png)

`           　　　`图3.1基于微信小程序的刷题系统的功能结构图
## 3.2系统开发步骤
系统的开发步骤可以分为系统开发、系统规划和系统实施。每一步都是在上上步的基础上进行的，不能跳级，在下一级进行时，不会对上一级的工作进行大的改变。所以就需要在每一级设计时充分保证正确才可以进行一下级的设计。这种开发步骤是最省时省力的方法，是经过国内外长久实践得出的最有效方法。
## 3.3数据库设计
### 3.3.1数据库概念结构设计
数据库的概念结构设计就是需要在系统分析的过程中分析开发本系统是要做什么，然后设计出大的框架，根据大的框架把系统进行转换成怎么做的物理模型。然后再进行设计。

`　　`在所有的系统设计中数据库的设计占有举足轻重的地位，选择合适的数据库软件进行设计非常重要。因为本系统的功能非常有针对性，没有进行扩展，所以本系统采用小型轻便的mysql软件进行设计。数据库的安全保障着系统里数据的安全，本系统的主要数据为试题信息、试卷信息以及用户信息、知识点信息。本系统的ER关系图如下图3.2所示：

![](/md/blog.007.png)

图3.2实体关系ER图

（1）管理员的属性包括编号、用户名和密码等，管理员的ER图如下图3.3所示：

![](/md/blog.008.png)

图3.3管理员信息ER图

（2）试卷信息主要为管理员进行管理，学生进行浏览，试卷信息的属性包括编号、题目、数量、分数等，详细的试卷信息ER图如下图3.4所示：

![](/md/blog.009.png)

图3.4试卷信息ER图

(3)成绩信息的属性包括编号、学生、分数等，成绩信息的ER图如下图3.5所示：

![](/md/blog.010.png)

图3.5成绩信息ER图

` `(5)用户信息属性包括账号、密码、姓名、性别、编号等，用户信息ER图如下图3.6所示：

![](/md/blog.011.png)

图3.6用户信息ER图
### 3.3.2数据库逻辑结构设计
数据库的逻辑结构设计也可以称为数据库表的设计，一般情况下采用第三范式进行设计，因为数据库的概念结构可以单独使用，不特定于某个数据库所以就需要对数据库的概念结构进行转换，从上节的数据ER图转换出本系统的数据库表，主要包括管理员信息表、用户信息表、试卷信息表、试题信息表、知识点信息表等，具体的数据库表如下表3.1－3.7所示：

表3.1　config


|序号|列名|数据类型|长度|小数位|标识|主键|外键|允许空|默认值|说明|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1|id|bigint|20||是|是||否||auto\_increment|
|2|name|varchar|100|||||否|||
|3|value|varchar|100|||||是|||
表3.2　discusszhishidian


|序号|列名|数据类型|长度|小数位|标识|主键|外键|允许空|默认值|说明|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1|id|bigint|20||是|是||否||auto\_increment|
|2|addtime|timestamp||||||是|CURRENT\_TIMESTAMP||
|3|refid|bigint|20|||||否|||
|4|userid|bigint|20|||||否|||
|5|nickname|varchar|200|||||是|||
|6|content|longtext||||||否|||
|7|reply|longtext||||||是|||
表3.3　exampaper


|序号|列名|数据类型|长度|小数位|标识|主键|外键|允许空|默认值|说明|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1|id|bigint|20||是|是||否||auto\_increment|
|2|addtime|timestamp||||||是|CURRENT\_TIMESTAMP||
|3|name|varchar|200|||||否|||
|4|time|int|11|||||否|||
|5|status|int|11|||||否|0||
表3.4　examquestion


|序号|列名|数据类型|长度|小数位|标识|主键|外键|允许空|默认值|说明|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1|id|bigint|20||是|是||否||auto\_increment|
|2|addtime|timestamp||||||是|CURRENT\_TIMESTAMP||
|3|paperid|bigint|20|||||否|||
|4|papername|varchar|200|||||否|||
|5|questionname|varchar|200|||||否|||
|6|options|longtext||||||是|||
|7|score|bigint|20|||||是|0||
|8|answer|varchar|200|||||是|||
|9|analysis|longtext||||||是|||
|10|type|bigint|20|||||是|0||
|11|sequence|bigint|20|||||是|100||
表3.5　examrecord


|序号|列名|数据类型|长度|小数位|标识|主键|外键|允许空|默认值|说明|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1|id|bigint|20||是|是||否||auto\_increment|
|2|addtime|timestamp||||||是|CURRENT\_TIMESTAMP||
|3|userid|bigint|20|||||否|||
|4|username|varchar|200|||||是|||
|5|paperid|bigint|20|||||否|||
|6|papername|varchar|200|||||否|||
|7|questionid|bigint|20|||||否|||
|8|questionname|varchar|200|||||否|||
|9|options|longtext||||||是|||
|10|score|bigint|20|||||是|0||
|11|answer|varchar|200|||||是|||
|12|analysis|longtext||||||是|||
|13|myscore|bigint|20|||||否|0||
|14|myanswer|varchar|200|||||是|||
表3.6　kemuleixing


|序号|列名|数据类型|长度|小数位|标识|主键|外键|允许空|默认值|说明|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1|id|bigint|20||是|是||否||auto\_increment|
|2|addtime|timestamp||||||是|CURRENT\_TIMESTAMP||
|3|leixing|varchar|200|||||是|||
表3.7　storeup


|序号|列名|数据类型|长度|小数位|标识|主键|外键|允许空|默认值|说明|
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|1|id|bigint|20||是|是||否||auto\_increment|
|2|addtime|timestamp||||||是|CURRENT\_TIMESTAMP||
|3|userid|bigint|20|||||否|||
|4|refid|bigint|20|||||是|||
|5|tablename|varchar|200|||||是|||
|6|name|varchar|200|||||否|||
|7|picture|varchar|200|||||否|||

# 第4章 系统实现
## 4.1登录功能模块的实现
登录功能包括用户登录和管理员登录，在登录界面设计中包括用户名和密码、身份的检验。用户名和密码、身份的检验过程由数据库自动完成，此过程需要1秒左右。首先由用户填写账号和密码，然后选择身份，最后点击登录系统，数据库自行对用户名和密码进行对比，所填写数据正确方能进行登录，所填写数据错误则需要返回登录界面重新登录。用户登录界面的设计运行界面效果如下图4.1所示：

![](/md/blog.012.png)

图4.1用户系统登录界面效果
## 4.2 知识点管理功能界面的实现
知识点信息管理是最基本的功能，管理员可以对知识点进行添加和修改。在本界面里可以看到文字信息、图片信息等。知识点信息管理界面的运行效果界面如下图4.2所示：

![](/md/blog.013.png)

图4.2知识点信息界面的运行效果 
## 4.3密码信息管理模块实现 
密码信息管理是对用户的登录密码进行修改，可以防止密码的外泄，此功能非常的实用，也是一个系统必备的功能之一，密码信息管理功能的界面实现效果如下图4.3所示：

![](/md/blog.014.png)

图4.3密码信息管理功能实现界面
## 4.4 用户信息管理功能的实现
用户管理功能分为管理员管理用户信息和用户管理自己的信息两种，管理员可以看到用户的账号、真实姓名等信息，可以删除用户的账号信息。用户信息管理功能的界面实现效果如下图4.4所示：

![](/md/blog.015.png)

图4.4用户信息管理功能界面实现效果
## 4.5 试题信息管理功能的实现
系统里展示的试题信息包括判断题、选择题、填空题，管理员可以上新试题信息，也可以修改试题信息，当试题信息被淘汰时也可以直接进行删除，试题信息管理功能的界面实现效果如下图4.5所示：

![](/md/blog.016.png)

图4.5试题信息管理功能的运行效果界面

管理员添加试题信息的效果图如下图4.6所示：

![](/md/blog.017.png)

图4.6添加试题信息的界面效果
## 4.6考试管理功能的界面设计实现
考试管理功能为考试记录、错题本和试卷列表的管理。本功能与用户我的功能一样。考试信息管理功能的界面实现效果如下图4.7所示：

![](/md/blog.018.png)

图4.7考试信息管理功能的界面实现效果
## 4.7试卷信息管理功能的界面设计实现
本功能与试题信息功能一致，是对试卷生成的管理，管理员查询试卷信息的实现界面如下图4.8所示：

![](/md/blog.019.png)

图4.8查询试卷信息的实现界面效果
## 4.8科目类型管理功能的界面实现
管理员可以设置科目的类型，方便用户的学习。科目类型添加的界面实现如下图4.9所示：

![](/md/blog.020.png)

图4.9添加科目类型的功能实现界面
## 4.9用户首页功能的实现
本功能为用户的功能，可以在首页里看到知识点信息，可以收藏知识点和评论。首页功能的实现界面如下图4.10所示：

![](/md/blog.021.png)

图4.10首页功能实现界面
## 4.10前台展示知识点详情功能的实现
用户可以了解具体的知识点详情，在本界面里可以收藏知识点和评论知识点。知识点详情的实现界面如下图4.11所示：

![](/md/blog.022.png)

图4.11知识点详情实现界面
## 4.11在线考试功能的实现
用户可以实现在线考试，实现界面如下图4.12所示：

![](/md/blog.023.png)

图4.12在线考试实现界面
## 4.12用户错题本功能实现界面
用户在考试后对做错的题目可以显示在错题本里。错题本功能的实现界面如下图4.13所示：

![](/md/blog.024.png)

图4.13用户错题本功能实现界面
# 系










