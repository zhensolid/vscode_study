
<h1 style=color:red align=center>个人文档</h1>
-
开始我的测试

## 我的第一个测试文档
- 大地工作
  - 点小部门
  - 客服部

### 配送公司

### 资金返回

## 我的第二个测试文档

###家人安排工作
- 建筑工作
  - 待定
  - 待定

###待定工作

- [ ] 完成
- [ ] 未完成


<h2 style=color:red align=center>目录</h2>

[toc]


```mermaid
gantt
        dateFormat  YYYY-MM-DD

        title 时间图标

        section 设计
        需求:done,des1, 2019-01-06,2019-01-08
        原型:active,des2, 2019-01-09, 3d
        UI设计:des3, after des2, 5d
        未来任务:des4, after des3, 5d

        section 开发
        学习准备理解需求:crit, done, 2019-01-06,24h
        设计框架:crit, done, after des2, 2d
        开发:crit, active, 3d
        未来任务:crit, 5d
        休息时间:2d

        section 测试
        功能测试:active, a1, after des3, 3d
        压力测试:after a1, 20h
        测试报告: 48h
```

---

```mermaid
sequenceDiagram
对象A->对象B:中午吃什么？
对象B->>对象A: 随便
loop 思考
    对象A->对象A: 努力搜索
end
对象A-->>对象B: 火锅？
对象B->>对象A: 可以
Note left of 对象A: 我是一个对象A
Note right of 对象B: 我是一个对象B
participant 对象C
Note over 对象C: 我自己说了算
```

---

```sequence
Title:时序图示例
客户端->服务端: 我想找你拿下数据 SYN
服务端-->客户端: 我收到你的请求啦 ACK+SYN
客户端->>服务端: 我收到你的确认啦，我们开始通信吧 ACK
Note right of 服务端: 我是一个服务端
Note left of 客户端: 我是一个客户端
Note over 服务端,客户端: TCP 三次握手
participant 观察者⌛
```

# 自主学习flow
```flow
str=>start: 开始
op=>operation: 学习
op1=>operation: 目标
cond=>condition: 过程
e=>end

str(right)->op->op1->cond
cond(yes)->e
cond(no)->op

```

```sequence

A->B:how are you?

B-->>A:fine.
```

