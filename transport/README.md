# 传输层

传输层是为不同应用进程之间提供逻辑通信服务。 

## UDP: User Datagram Protocolf (rfc768)
基于IP协议做了多路复用/分用，简单错误检测。

UDP属于“Best effort”服务，他尽可能的传输数据。从而可能会产生丢失和数据的非按需到达。

UDP是无连接的，发送方和接受方不需要握手。

### UDP为什么会存在呢？
+ 无需建立链接，延迟短（DNS走的就是UDP ）。
+ 实现简单，无需维护连接状态。
+ 头部包含信息少，开销少。
+ 没有拥塞控制，应用可更好的控制发送时间和速率。

### 用途
+ 常用于流媒体应用
  + 容忍丢失。
  + 速率敏感。
+ UDP还用于
  + DNS
  + SNMP

### UDP报文断格式
![udp-segment](/transport/images/udp-segment.png)

## 可靠数据传输
不错、不丢、不乱。

### 可靠数据传输协议
RDT

