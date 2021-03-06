# rc-cluster-netty

[Netty](https://github.com/netty/netty)：Netty is an asynchronous event-driven network application framework for rapid development of maintainable high performance protocol servers & clients.(Netty是一个异步的，事件驱动的网络应用程序框架，用于快速开发可维护的高性能协议服务器和客户端)

![components](http://netty.io/images/components.png)

## Netty重要组件

* Channel（通道）：相当于一个链接
* ChannelHandler（通道处理器），类似过滤器，或者拦截器，请求过来后，会通过一个一个的ChannelHandler得到一个一个的处理，处理完成后交给业务方法，完成业务的处理...
* pipeline（管道），多个ChannelHandler构成

## Environment

* JDK Version 1.8.0_152
* DevTool：IDEA
* Netty Version：4.1.25.Final
* Protobuf Version：3.10.0
* Thrift Version：0.13.0

> RoadMap 和详细知识笔记请查看[Wiki](https://github.com/RootCluster/rc_netty/wiki)

项目结构，请按照如下 **顺序进行** 学习

```
rc-cluster-netty/
    ├── main/java/org/incoder
    │   ├── netty
    │   │   ├── heartbeat       # 基于 heartbeat 的 netty 应用
    │   │   ├── http            # 基于 HTTP 的 netty 应用
    │   │   ├── protobuf        # 使用 protobuf 编解码的 netty 应用
    │   │   ├── socket          # 基于 socket 的 netty 应用
    │   │   └── websocket       # 基于 websocket 的 netty 应用
    │   ├── protobuf            # 使用 protobuf 的示例
    │   ├── thrift              
    │   │   ├── java
    │   │   │   ├── generate    # thrift 的 Java 自动模板代码
    │   │   │   └── ……          # 相关示例
    │   │   └── py
    │   │       ├── generate    # thrift 的 Python 自动模板代码
    │   │       └── ……          # 相关示例
    │   └── grpc                # 使用 grpc 的示例
    │       ├── gen/            # grpc 生成的相关代码
    │       └── websocket       # 基于 websocket 的 netty 应用
    ├── idl-grpc/               # grpc 的描述定义文件
    ├── idl-protoc/             # protoc 的描述定义文件
    ├── idl-thrift/             # thrift 的描述定义文件
    └── webapp/
        └── websocket.html      # 使用 websocket 网页
```

## License
```
Copyright (c) 2018 Jerry xu.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```