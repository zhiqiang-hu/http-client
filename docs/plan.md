# 开发计划

本文档是开发的计划，随时更新，欢迎以 [GitHub Issues](https://github.com/jiejieTop/httpclient/issues) 的形式提交功能需求、问题和bug报告等。

框架如下：

![httpclient框架](http://qiniu.jiejie01.top/httpclient.png)

## 平台抽象层

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 内存管理 |
| ☑ | 线程管理 |
| ☑ | 时间管理 |
| ☑ | 互斥锁 |
| ☑ | socket API |
| ☑ | tcp直连 |
| ☑ | tls加密传输 |

## network网卡

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 网卡初始化 |
| ☑ | 连接服务器 |
| ☑ | 终止连接 |
| ☑ | 读操作 |
| ☑ | 写操作 |
| - | 使用 openssl |

## 通用组件开发

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 列表操作 |
| ☑ | 日志显示 |
| ☑ | 错误代码 |
| ☑ | 随机数生成器 |

## 基础组件开发

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 字符串与整形互转 |
| ☑ | 动态计算字符串的大小，可变参数 |
| ☑ | 处理字符串时的内存动态分配，realloc 方式 |
| ☑ | 字符串连接，可变参数 |
| - | - |


## url解析器

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 通过url解析各个字段的内容 |
| - | - |


## HTTP报文处理

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 报文字段动态管理内存空间 |
| ☑ | 报文字段的连接、追加 |
| - | - |

## HTTP请求

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | http 请求初始化 |
| ☑ | 根据 path 构建请求起始行 |
| ☑ | 根据 key-value 构建请求头部 |
| - | 根据需求构建请求主体 |
| - | 填充必要的 http 请求报文信息 |
| - | 构建完整的 http 请求报文 |
| - | 完成正常的 http 请求操作 |
| - | 长连接 / 非长连接 |
| - | - |

## HTTP响应

| 完成度 | 功能需求 |
| -- | -- |
| - | 解析 HTTP 响应报文 |
| - | - |

## 拦截器

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 拦截器初始化网卡 |
| ☑ | 根据解析的 url 信息连接服务器 |
| ☑ | 发起 http 请求 |
| - | 初始化 http_parser、parser_settings，为解析响应报文做准备 |
| - | 处理响应报文 |
| - | 处理重连请求 |
| - | 处理重定向信息 |
| - | 处理 404 逻辑 |
| - | 数据正常递交给上层 |
| - | - |


## 工作队列

| 完成度 | 功能需求 |
| -- | -- |
| - | 创建工作队列 |
| - | 根据先后顺序将数据递交给拦截器 |
| - | - |


## 连接管理器

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 连接的相关参数初始化 |
| ☑ | 连接参数的获取、设置 |
| - | 初始化线程池 |
| - | 创建内部处理的线程 |
| - | 创建连接结构 |
| - | 租借连接结构 |
| - | 回收连接结构 |
| - | - |

## 路由

| 完成度 | 功能需求 |
| -- | -- |
| - | 哈希算法的实现 |
| - | 根据url的参数查找最优处理 |
| - | 递交数据给连接管理器 |
| - | - |

## url解析器

| 完成度 | 功能需求 |
| -- | -- |
| ☑ | 解析url各个字段的参数 |
| - | - |


## 如何参与开发

[如何参与开发，提交PR？](./how_to_pr.md)