---
title: 7.逻辑判断与分支
---

:::info 信息
[教材](https://coding-newbies-group.github.io/programming-co_creation-docs/docs/pilot/p1-3-structure-2#%E5%87%BD%E6%95%B0)
[视频](https://www.bilibili.com/video/BV1Hx4y1F7pH/?vd_source=4a888db8814702b2062fcaf2575be745)
:::



## if, else if, else

当部署好上面的机器人后，用下面的代码：

```js
client.loopBlaze({
  onMessage(msg) {
    if (msg.data === "你好") {
      client.sendmessagetext(msg.user_id, "你也好！");
    } else if (msg.data === "你是谁") {
      client.sendmessagetext(msg.user_id, "我是编程学习小助手");
    } else {
      client.sendmessagetext(msg.user_id, "我不知道你在说什么");
    }
  },
  onAckReceipt() {},
});
```

替换掉：

```js
client.loopBlaze({
  onMessage(msg) {
    client.sendMessageText(msg.user_id,"我的第一个Mixin机器人")
  },
});
```



Python代码：

```python
a = 5
if (a > 5):
    print("a大于5")
elif (a < 5):
    print("a小于5")
else:
    print("a等于5")
```



## 课程用到的代码

[coding-newbies-group/learn-code at 1-7](https://github.com/coding-newbies-group/learn-code/blob/1-7/index.js)



## 作业

请大家想想下面的代码，会收到什么回复？请解释一下为什么？

```
if( msg.data === "你好"){
	client.sendmessagetext(msg.userid, "你也好！")
} else if (msg.data === "你好"){
	client.sendmessagetext(msg.userid, "我是编程学习小助手")
} else {
    client.sendmessagetext(msg.userid, "我不知道你在说什么")
}
```
