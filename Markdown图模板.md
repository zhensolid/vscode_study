<h1 align=center style=color:red>Markdown图</h1>

# flow图
```flow
str=>start: 开始学习
op=>operation: 学习过程
op2=>operation: 检查学习结果
cond=>condition: 学习是否熟练
e=>end: 完成学习

str(right)->op->op2->cond
cond(no)->op
cond(yes)->e
```

# sequence图
```sequence
Title:连接建立的过程
客户主机->服务器主机: 连接请求（SYN=1,seq=client_isn）
服务器主机->客户主机: 授予连接（SYN=1,seq=client_isn）\n ack=client_isn+1
客户主机->服务器主机: 确认（SYN=0,seq=client_isn+1）\n ack=server_isn+1
```

# mermaid图横向
```mermaid
graph LR
A[方形] -->B(圆角)
    B --> C{条件a}
    C -->|a=1| D[结果1™]
    C -->|a=2| E[结果2]
    D -->G[结束]
    E -->G
    F[横向流程图]
```

# mermaid图竖向
```mermaid
graph TD
A[方形] -->B(圆角)
    B --> C{条件a}
    C -->|a=1| D[结果1]
    C -->|a=2| E[结果2]
    F[竖向流程图]
```

# mermaid标准时序图样例(sequenceDiagram)

```mermaid
sequenceDiagram
    participant 张三
    participant 李四
    张三->>王五: 王五你好吗？
    loop 健康检查
        王五->王五: 与疾病战斗
    end
    Note right of 王五: 合理 食物 <br/>看医生...
    李四-->>张三: 很好!!
    王五->李四: 你怎么样?
    李四-->王五: 很好!
```

# mermaid甘特图(gantt)
```mermaid
gantt
dateFormat  YYYY-MM-DD
title 软件开发甘特图

section 设计
需求:done,des1, 2014-01-06,2014-01-08
原型:active,des2, 2014-01-09, 3d
UI设计:des3,after des2, 5d
未来任务:des4,after des3, 5d

section 开发
学习准备理解需求:crit, done, 2014-01-06,24h
设计框架:crit, done, after des2, 2d
开发:crit, active, 3d
未来任务:crit, 5d
耍:2d

section 测试
功能测试:active, a1, after des3, 3d
压力测试:after a1  , 20h
测试报告: 48h
```