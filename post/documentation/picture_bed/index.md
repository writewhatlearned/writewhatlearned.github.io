# Picture Bed

<!--more-->

随着接触的信息类型、数量等剧增，将信息转换成知识的链路过程越来越长，因此逐渐由轻记录养成了撰写博客的习惯，慢慢开始高频使用[**Markdown**](https://baike.baidu.com/item/markdown?fromModule=lemma_search-box)来撰写博客。

在深度使用兼容Markdown语言的编辑器，撰写博客过程中发现，Markdown编辑器的纯文本编辑和图文编辑与以Word为主的文本编辑器存在不同。

Markdown不同于Word（Word直接把图片、文本等统一打包在.doc文件内部），而是以**链接**(https://baike.baidu.com/item/markdown/markdown.png)和**文件路径**(./blog/20230105/markdown.png)等方式支持图片访问，使得纯文本和图片、视频、音频等资源分开存储。

>  Markdown 是一种轻量级标记语言，允许人们使用易读易写的纯文本格式编写文档，然后转换成有效的 XHTML、HTML文档。 由于 Markdown 的轻量化、易读易写特性，并且对于图片，图表、数学式都有支持，许多网站都广泛使用 Markdown 来撰写帮助文档或是用于论坛上发表消息。 如 GitHub、Reddit、Diaspora、Stack Exchange、OpenStreetMap 、SourceForge、简书等，甚至还能被使用来撰写电子书。 

### **Markdown文件共享**

在需要进行Markdown文件共享时，通常采用以下两种方式，否则会遇到图片文件无法显示（图片等资源丢失）的尴尬局面。

1、如果**图片文件**以**文件路径**方式存放，进行Markdown文件共享时，常常需要将源文件和图片文件打包，才能进行源文件共享。

2、如果图片文件以**外链（URL）**方式存放，进行Markdown文件共享时，只需要进行源文件共享即可。

### **一、基于Github搭建图片、视频等资源外链**

但是如何获取图片外链，特别是本地图片如何生成外链。

此时就需要用到**图床**，即存储图片同时也可以为每一张图片提供访问链接。

> **图床**：存储图片同时也可以为每一张图片提供访问链接。 

### **1.1** [**注册Github**](https://github.com/)

![img](https://raw.githubusercontent.com/WriteWhatLearned/imgs_repos/master/writing/202306171531623.png)

### **1.2** [**创建Github仓库**](https://github.com/new)

- *仓库名称可自定义；*
- *仓库属性为Public；*
- *Description、README、License等可自定义添加；*

![img](https://pic3.zhimg.com/80/v2-c87c1b377173e024fcce05f3272274e5_1440w.jpg)

### **1.3** [**生成仓库访问密钥**](https://github.com/settings/tokens)

- 1.3.1 单击`Generate new token`，生成仓库访问Token；

![img](https://raw.githubusercontent.com/WriteWhatLearned/imgs_repos/master/writing/202306171532907.png)

**注意：** 

- Token生成后只会显示一次！注意离线保存使用。

### **二、基于Github生成的Token配置PicGo**

![img](https://pic4.zhimg.com/80/v2-50115e508aa6ebc9d4dcf22aa021c61f_1440w.jpg)

### **2.1 详细配置介绍**

### **2.1.1 设定仓库名**

仓库名的格式是用户名/仓库，比如我创建了一个叫做WX_BLOG_IMG的仓库，在PicGo里我要设定的仓库名就是WriteWhatLearned/WX_BLOG_IMG。

### **2.2.2 设定分支名**

一般我们选择main分支即可。然后记得点击确定以生效，然后可以点击设为默认图床来确保上传的图床是GitHub。

### **2.2.3 设定Token**

基于以上生成的Token。

### **2.2.4 设定存储路径**

如果需要对图片作分文件存储，需要在Github新建文件夹。

### **2.2.5 设定自定义域名**

设定图片外链自定义命名方式，如上图采用jsdeliver作图片资源的CDN加速的格式为https://cdn.jsdelivr.net/gh/用户名/仓库名@分支名。

### **三、其他**

目前提供图床功能的主流服务主要有以下几种：

| 编号 | 服务                                                         | 链接                                                         | 备注                                                         | 开源 |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| 1    | SM.MS                                                        | [https://smms.app/](https://link.zhihu.com/?target=https%3A//smms.app/) | - 原官网链接，[https://sm.ms/](https://link.zhihu.com/?target=https%3A//sm.ms/)已被屏蔽。  - 速度一般，传输和存储都有限制。 - 单次上传最多10张图片，单张图片最大5M。 | 是   |
| 2    | Github                                                       | [https://github.com/](https://link.zhihu.com/?target=https%3A//github.com/) | - 资源以公开仓库形式存储。  - 速度一般，速度和存储都有限制。 - 总容量限制1G，单张图片最大100M。 | 是   |
| 3    | 七牛云                                                       | [https://sso.qiniu.com/](https://link.zhihu.com/?target=https%3A//sso.qiniu.com/) | -                                                            | 否   |
| 4    | [腾讯云](https://www.zhihu.com/search?q=腾讯云&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2894522051})COS | [https://cloud.tencent.com/](https://link.zhihu.com/?target=https%3A//cloud.tencent.com/) | -                                                            | 否   |
| 5    | 阿里云COS                                                    | [https://www.aliyun.com/](https://link.zhihu.com/?target=https%3A//www.aliyun.com/) | -                                                            | 否   |

### **四、图床管理程序/软件 - PicGo**

[**软件下载**](https://picgo.github.io/PicGo-Doc/)

![img](https://raw.githubusercontent.com/WriteWhatLearned/imgs_repos/master/writing/202306171535182.png)
