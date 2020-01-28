# 代码辅助开发工具

## 🥚第一部分：软件构思和想法产生背景

### 1.想法产生背景

首先我是一个极其不愿意重复的人，喜欢优化重复性质的工作。在日常开发中我意识到，有很多工作都在思考过程中重复了

就是一件事情，我做的时候总能感觉到，我之前做过，也这样思考过，于是我这次做的就比较快了而已，但是还是会消耗一些时间，对于更复杂的事情来说，消耗的时间更多，即使这个复杂的事情我之前完全做过

这就让我非常的忧愁，或许别人所说的工作了2，3年没有提升，大多是将时间消耗在了这个地方

首先分析，这样的坏处就是

- 对自己：工作不好突破，没有提升，提高很慢
- 对公司：消耗额外的劳动力（虽然表现上，你是很努力的），加大企业人力成本，时间成本

---

### 2.软件构思

这时候我就想，能不能有一个平台，让我**所想即所得**，我想这个地方这么布局，然后这几十行代码就不用我写，自动能生成。前期就做这么一个简单的事情

---

## 🍥第二部分：软件功能规划（v0.9 Alpha）

### 1.行为单元编辑

- 行为单元可以是 只增加HTML代码，只增加CSS代码，或者同时增加HTML和CSS代码
- 行为单元提供增删改查的基本功能

---

### 2.行为单元组合

- 不同的行为单元可以组合起来，形成一个新的行为单元
- 问题一：行为单元组合，代码位置如何组合？
- 问题二：行为单元组合，小的行为单元改变后，整个行为单元是否跟着改变？

---

### 3.行为单元使用

- 使用行为单元来进行代码的快速书写
- 具有搜索功能，分类功能（也就是一个行为单元创建的时候，要标识它的分类）

---

### 4.代码编写

- 采用 vs code 同款编辑插件，尽量做到 部分编辑体现类似的效果

---

### 5.保存

- ctrl + s & 时隔10s 自动保存

---

### 6.预览功能（支持单页应用）

- 嫁接到本地文件
- 问题一：如何选中本地文件，进行文件的注入和更改？

---

## 🍡第三部分：项目工程规划

### 1.脚手架

- 脚手架采用 Vue-cli 3.0

---

### 2.项目结构

- db：本地数据库（JSON文件）
- server：服务端代码（Node + egg）
- src：前端代码编写（Vue-Cli）
- public 静态文件（Vue-Cli）

---

## 🍬第四部分：难点攻克记录

### （2020/1/28）难点一：如何在单页应用中，引入Js逻辑，并让其能够预览？

思考一：怎么想都不好在平台上进行实时预览，可以在本地启动一个预览程序，然后与平台关联上，平台生成的html，css代码都直接影响本地，然后通过本地的预览进行关联

- 写样式代码 & 结构代码：通过平台
- 写逻辑代码 & 启动预览服务：通过原来的方式




