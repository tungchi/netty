![Build project](https://github.com/netty/netty/workflows/Build%20project/badge.svg)

# Netty Project

Netty is an asynchronous event-driven network application framework for rapid development of maintainable high
performance protocol servers & clients.

Netty是一个异步事件驱动的网络应用框架，用于快速开发可维护的高性能协议服务器和客户端。

## Links

* [Web Site](https://netty.io/)
* [Downloads](https://netty.io/downloads.html)
* [Documentation](https://netty.io/wiki/)
* [@netty_project](https://twitter.com/netty_project)
* [Official Discord server](https://discord.gg/q4aQ2XjaCa)

## How to build

For the detailed information about building and developing Netty, please
visit [the developer guide](https://netty.io/wiki/developer-guide.html). This page only gives very basic information.

关于构建和开发Netty的详细信息，请访问开发者指南。这一页只提供非常基本的信息。

You require the following to build Netty:

* Latest stable [OpenJDK 8](https://adoptium.net/)
* Latest stable [Apache Maven](https://maven.apache.org/)
* If you are on Linux or MacOS, you need [additional development packages](https://netty.io/wiki/native-transports.html)
  installed on your system, because you'll build the native transport.

Note that this is build-time requirement. JDK 5 (for 3.x) or 6 (for 4.0+ / 4.1+) is enough to run your Netty-based
application.

## Branches to look

Development of all versions takes place in each branch whose name is identical to `<majorVersion>.<minorVersion>`.  For example, the development of 3.9 and 4.1 resides in [the branch '3.9'](https://github.com/netty/netty/tree/3.9) and [the branch '4.1'](https://github.com/netty/netty/tree/4.1) respectively.

## Usage with JDK 9+

Netty can be used in modular JDK9+ applications as a collection of automatic modules. The module names follow the
reverse-DNS style, and are derived from subproject names rather than root packages due to historical reasons. They
are listed below:

Netty可以在模块化的JDK9+应用中作为自动模块的集合使用。模块名称遵循反向dns风格，并且由于历史原因从子项目名称而不是根包派生。它们列在下面:
 * `io.netty.all`
 * `io.netty.buffer`
 * `io.netty.codec`
 * `io.netty.codec.dns`
 * `io.netty.codec.haproxy`
 * `io.netty.codec.http`
 * `io.netty.codec.http2`
 * `io.netty.codec.memcache`
 * `io.netty.codec.mqtt`
 * `io.netty.codec.redis`
 * `io.netty.codec.smtp`
 * `io.netty.codec.socks`
 * `io.netty.codec.stomp`
 * `io.netty.codec.xml`
 * `io.netty.common`
 * `io.netty.handler`
 * `io.netty.handler.proxy`
 * `io.netty.resolver`
 * `io.netty.resolver.dns`
 * `io.netty.transport`
 * `io.netty.transport.epoll` (`native` omitted - reserved keyword in Java)
 * `io.netty.transport.kqueue` (`native` omitted - reserved keyword in Java)
 * `io.netty.transport.unix.common` (`native` omitted - reserved keyword in Java)
 * `io.netty.transport.rxtx`
 * `io.netty.transport.sctp`
 * `io.netty.transport.udt`

Automatic modules do not provide any means to declare dependencies, so you need to list each used module separately
in your `module-info` file.

自动模块不提供任何声明依赖关系的方法，所以你需要在你的模块信息文件中单独列出每个使用的模块。