# HW-8


https://get.jenkins.io/war-stable/latest/
sudo apt install openjdk-11-jdk
firewall-cmd --permanent --zone=public --add-port=8087/tcp
firewall-cmd --reload
java -jar jenkins.war --httpPort=8087


https://get.jenkins.io/war-stable/2.346.3/


✅ 删除 Jenkins 插件的方式
Jenkins 的插件都存放在主目录下的 plugins/ 文件夹中。删除这个文件夹中的内容即可移除所有插件。

🧹 步骤一：关闭 Jenkins
bash
复制
编辑
# 如果你是用命令行启动 Jenkins 的，可以直接 Ctrl+C 结束进程
# 或者用系统服务的方式关闭
sudo systemctl stop jenkins
🗑️ 步骤二：删除插件目录下的所有插件
bash
复制
编辑
cd ~/.jenkins/plugins
rm -rf *
也可以删除整个插件目录：

bash
复制
编辑
rm -rf ~/.jenkins/plugins



va.io.IOException: Failed to load: bouncycastle API Plugin (bouncycastle-api 2.30.1.78.1-233.vfdcdeb_0a_08a_a_)
 - Jenkins (2.361.4) or higher required
	at hudson.PluginWrapper.resolvePluginDependencies(PluginWrapper.java:1018)
	at hudson.PluginManager$2$1$1.run(PluginManager.java:542)
	at org.jvnet.hudson.reactor.TaskGraphBuilder$TaskImpl.run(TaskGraphBuilder.java:175)
	at org.jvnet.hudson.reactor.Reactor.runTask(Reactor.java:305)
	at jenkins.model.Jenkins$5.runTask(Jenkins.java:1158)
	at org.jvnet.hudson.reactor.Reactor$2.run(Reactor.java:222)
	at org.jvnet.hudson.reactor.Reactor$Node.run(Reactor.java:121)
	at jenkins.security.ImpersonatingExecutorService$1.run(ImpersonatingExecutorService.java:68)
	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1136)
	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:635)
	at java.base/java.lang.Thread.run(Thread.java:840)
2025-04-05 01:11:55.189+0000 [id=31]	SEVERE	jenkins.InitReactorRunner$1#onTaskFailed: Failed Loading plugin Instance Identity v185.v303dc7c645f9 (instance-identity)
java.io.IOException: Failed to load: Instance Identity (instance-identity 185.v303dc7c645f9)
 - Jenkins (2.361.4) or higher required
 - Failed to load: bouncycastle API Plugin (bouncycastle-api 2.30.1.78.1-233.vfdcdeb_0a_08a_a_)
	at hudson.PluginWrapper.resolvePluginDependencies(PluginWrapper.java:1018)
	at hudson.PluginManager$2$1$1.run(PluginManager.java:542)
	at org.jvnet.hudson.reactor.TaskGraphBuilder$TaskImpl.run(TaskGraphBuilder.java:175)
	at org.jvnet.hudson.reactor.Reactor.runTask(Reactor.java:305)
	at jenkins.model.Jenkins$5.runTask(Jenkins.java:1158)
	at org.jvnet.hudson.reactor.Reactor$2.run(Reactor.java:222)
	at org.jvnet.hudson.reactor.Reactor$Node.run(Reactor.java:121)
	at jenkins.security.ImpersonatingExecutorService$1.run(ImpersonatingExecutorService.java:68)
	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1136)
	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:635)
	at java.base/java.lang.Thread.run(Thread.java:840)
2025-04-05 01:11:55.509+0000 [id=33]	INFO	jenkins.InitReactorRunner$1#onAttained: Prepared all plugins
2025-04-05 01:11:55.511+0000 [id=33]	INFO	jenkins.InitReactorRunner$1#onAttained: Started all plugins
2025-04-05 01:11:55.515+0000 [id=32]	INFO	jenkins.InitReactorRunner$1#onAttained: Augmented all extensions
2025-04-05 01:11:55.636+0000 [id=32]	INFO	jenkins.InitReactorRunner$1#onAttained: System config loaded
2025-04-05 01:11:55.639+0000 [id=32]	INFO	jenkins.InitReactorRunner$1#onAttained: System config adapted
2025-04-05 01:11:55.644+0000 [id=31]	INFO	jenkins.InitReactorRunner$1#onAttained: Loaded all jobs
2025-04-05 01:11:55.645+0000 [id=31]	INFO	jenkins.InitReactorRunner$1#onAttained: Configuration for all jobs updated
2025-04-05 01:11:55.661+0000 [id=52]	INFO	hudson.model.AsyncPeriodicWork#lambda$doRun$1: Started Download metadata
2025-04-05 01:11:55.664+0000 [id=52]	INFO	hudson.model.AsyncPeriodicWork#lambda$doRun$1: Finished Download metadata. 1 ms
2025-04-05 01:11:55.773+0000 [id=36]	INFO	jenkins.InitReactorRunner$1#onAttained: Completed initialization
2025-04-05 01:11:55.781+0000 [id=25]	INFO	hudson.lifecycle.Lifecycle#onReady: Jenkins is fully up and running
^Z
[1]+  Stopped                 java -jar jenkins.war --httpPort=8087
root@linux:/home/vboxuser/Desktop# ^C
root@linux:/home/vboxuser/Desktop# ^C
root@linux:/home/vboxuser/Desktop# ^C
root@linux:/home/vboxuser/Desktop# java -jar jenkins.war --httpPort=8087
Running from: /home/vboxuser/Desktop/jenkins.war
webroot: $user.home/.jenkins
2025-04-05 01:13:13.651+0000 [id=1]	INFO	org.eclipse.jetty.util.log.Log#initialized: Logging initialized @166ms to org.eclipse.jetty.util.log.JavaUtilLog
2025-04-05 01:13:13.690+0000 [id=1]	INFO	winstone.Logger#logInternal: Beginning extraction from war file
2025-04-05 01:13:13.701+0000 [id=1]	WARNING	o.e.j.s.handler.ContextHandler#setContextPath: Empty contextPath
2025-04-05 01:13:13.726+0000 [id=1]	INFO	org.eclipse.jetty.server.Server#doStart: jetty-9.4.45.v20220203; built: 2022-02-03T09:14:34.105Z; git: 4a0c91c0be53805e3fcffdcdcc9587d5301863db; jvm 17.0.14+7-Ubuntu-122.04.1
2025-04-05 01:13:13.835+0000 [id=1]	INFO	o.e.j.w.StandardDescriptorProcessor#visitServlet: NO JSP Support for /, did not find org.eclipse.jetty.jsp.JettyJspServlet
2025-04-05 01:13:13.852+0000 [id=1]	INFO	o.e.j.s.s.DefaultSessionIdManager#doStart: DefaultSessionIdManager workerName=node0
2025-04-05 01:13:13.852+0000 [id=1]	INFO	o.e.j.s.s.DefaultSessionIdManager#doStart: No SessionScavenger set, using defaults
2025-04-05 01:13:13.852+0000 [id=1]	INFO	o.e.j.server.session.HouseKeeper#startScavenging: node0 Scavenging every 660000ms
2025-04-05 01:13:14.019+0000 [id=1]	INFO	hudson.WebAppMain#contextInitialized: Jenkins home directory: /root/.jenkins found at: $user.home/.jenkins
2025-04-05 01:13:14.075+0000 [id=1]	INFO	o.e.j.s.handler.ContextHandler#doStart: Started w.@2c9399a4{Jenkins v2.346.3,/,file:///root/.jenkins/war/,AVAILABLE}{/root/.jenkins/war}
2025-04-05 01:13:14.079+0000 [id=1]	INFO	o.e.j.server.AbstractConnector#doStop: Stopped ServerConnector@8e24743{HTTP/1.1, (http/1.1)}{0.0.0.0:8087}
2025-04-05 01:13:14.080+0000 [id=1]	INFO	o.e.j.server.session.HouseKeeper#stopScavenging: node0 Stopped scavenging
2025-04-05 01:13:14.081+0000 [id=1]	INFO	hudson.WebAppMain#contextDestroyed: Shutting down a Jenkins instance that was still starting up
java.lang.Throwable: reason
	at hudson.WebAppMain.contextDestroyed(WebAppMain.java:383)
	at org.eclipse.jetty.server.handler.ContextHandler.callContextDestroyed(ContextHandler.java:1080)
	at org.eclipse.jetty.servlet.ServletContextHandler.callContextDestroyed(ServletContextHandler.java:584)
	at org.eclipse.jetty.server.handler.ContextHandler.contextDestroyed(ContextHandler.java:1043)
	at org.eclipse.jetty.servlet.ServletHandler.doStop(ServletHandler.java:319)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.stop(ContainerLifeCycle.java:180)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStop(ContainerLifeCycle.java:201)
	at org.eclipse.jetty.server.handler.AbstractHandler.doStop(AbstractHandler.java:108)
	at org.eclipse.jetty.security.SecurityHandler.doStop(SecurityHandler.java:430)
	at org.eclipse.jetty.security.ConstraintSecurityHandler.doStop(ConstraintSecurityHandler.java:423)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.stop(ContainerLifeCycle.java:180)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStop(ContainerLifeCycle.java:201)
	at org.eclipse.jetty.server.handler.AbstractHandler.doStop(AbstractHandler.java:108)
	at org.eclipse.jetty.server.session.SessionHandler.doStop(SessionHandler.java:520)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.stop(ContainerLifeCycle.java:180)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStop(ContainerLifeCycle.java:201)
	at org.eclipse.jetty.server.handler.AbstractHandler.doStop(AbstractHandler.java:108)
	at org.eclipse.jetty.server.handler.ContextHandler.stopContext(ContextHandler.java:1066)
	at org.eclipse.jetty.servlet.ServletContextHandler.stopContext(ServletContextHandler.java:386)
	at org.eclipse.jetty.webapp.WebAppContext.stopWebapp(WebAppContext.java:1454)
	at org.eclipse.jetty.webapp.WebAppContext.stopContext(WebAppContext.java:1420)
	at org.eclipse.jetty.server.handler.ContextHandler.doStop(ContextHandler.java:1120)
	at org.eclipse.jetty.servlet.ServletContextHandler.doStop(ServletContextHandler.java:297)
	at org.eclipse.jetty.webapp.WebAppContext.doStop(WebAppContext.java:547)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.stop(ContainerLifeCycle.java:180)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStop(ContainerLifeCycle.java:201)
	at org.eclipse.jetty.server.handler.AbstractHandler.doStop(AbstractHandler.java:108)
	at org.eclipse.jetty.server.Server.doStop(Server.java:470)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at winstone.Launcher.shutdown(Launcher.java:354)
	at winstone.Launcher.<init>(Launcher.java:217)
	at winstone.Launcher.main(Launcher.java:405)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:569)
	at Main._main(Main.java:342)
	at Main.main(Main.java:117)
2025-04-05 01:13:14.082+0000 [id=1]	INFO	o.e.j.s.handler.ContextHandler#doStop: Stopped w.@2c9399a4{Jenkins v2.346.3,/,null,STOPPED}{/root/.jenkins/war}
Exception in thread "Jenkins initialization thread" java.lang.NoClassDefFoundError: hudson/util/HudsonFailedToLoad
	at hudson.WebAppMain$3.run(WebAppMain.java:261)
Caused by: java.lang.ClassNotFoundException: hudson.util.HudsonFailedToLoad
	at java.base/java.net.URLClassLoader.findClass(URLClassLoader.java:445)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:592)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:525)
	at org.eclipse.jetty.webapp.WebAppClassLoader.loadClass(WebAppClassLoader.java:538)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:525)
	... 1 more
2025-04-05 01:13:14.085+0000 [id=1]	INFO	winstone.Logger#logInternal: Jetty shutdown successfully
java.io.IOException: Failed to start Jetty
	at winstone.Launcher.<init>(Launcher.java:206)
	at winstone.Launcher.main(Launcher.java:405)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:569)
	at Main._main(Main.java:342)
	at Main.main(Main.java:117)
Caused by: java.io.IOException: Failed to bind to 0.0.0.0/0.0.0.0:8087
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:349)
	at org.eclipse.jetty.server.ServerConnector.open(ServerConnector.java:310)
	at org.eclipse.jetty.server.AbstractNetworkConnector.doStart(AbstractNetworkConnector.java:80)
	at org.eclipse.jetty.server.ServerConnector.doStart(ServerConnector.java:234)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:73)
	at org.eclipse.jetty.server.Server.doStart(Server.java:401)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:73)
	at winstone.Launcher.<init>(Launcher.java:202)
	... 7 more
Caused by: java.net.BindException: Address already in use
	at java.base/sun.nio.ch.Net.bind0(Native Method)
	at java.base/sun.nio.ch.Net.bind(Net.java:555)
	at java.base/sun.nio.ch.ServerSocketChannelImpl.netBind(ServerSocketChannelImpl.java:337)
	at java.base/sun.nio.ch.ServerSocketChannelImpl.bind(ServerSocketChannelImpl.java:294)
	at java.base/sun.nio.ch.ServerSocketAdaptor.bind(ServerSocketAdaptor.java:89)
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:344)
	... 14 more
2025-04-05 01:13:14.086+0000 [id=1]	SEVERE	winstone.Logger#logInternal: Container startup failed
java.net.BindException: Address already in use
	at java.base/sun.nio.ch.Net.bind0(Native Method)
	at java.base/sun.nio.ch.Net.bind(Net.java:555)
	at java.base/sun.nio.ch.ServerSocketChannelImpl.netBind(ServerSocketChannelImpl.java:337)
	at java.base/sun.nio.ch.ServerSocketChannelImpl.bind(ServerSocketChannelImpl.java:294)
	at java.base/sun.nio.ch.ServerSocketAdaptor.bind(ServerSocketAdaptor.java:89)
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:344)
Caused: java.io.IOException: Failed to bind to 0.0.0.0/0.0.0.0:8087
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:349)
	at org.eclipse.jetty.server.ServerConnector.open(ServerConnector.java:310)
	at org.eclipse.jetty.server.AbstractNetworkConnector.doStart(AbstractNetworkConnector.java:80)
	at org.eclipse.jetty.server.ServerConnector.doStart(ServerConnector.java:234)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:73)
	at org.eclipse.jetty.server.Server.doStart(Server.java:401)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:73)
	at winstone.Launcher.<init>(Launcher.java:202)
Caused: java.io.IOException: Failed to start Jetty
	at winstone.Launcher.<init>(Launcher.java:206)
	at winstone.Launcher.main(Launcher.java:405)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:569)
	at Main._main(Main.java:342)
	at Main.main(Main.java:117)
root@linux:/home/vboxuser/Desktop# cd ~/.jenkins/plugins
root@linux:~/.jenkins/plugins# rm -rf * 
root@linux:~/.jenkins/plugins# ls
root@linux:~/.jenkins/plugins# cd /home/vboxuser/Desktop
root@linux:/home/vboxuser/Desktop# ls
 code   jenkins.war  'New Folder'
root@linux:/home/vboxuser/Desktop# java -jar jenkins.war --httpPort=8087
Running from: /home/vboxuser/Desktop/jenkins.war
webroot: $user.home/.jenkins
2025-04-05 01:14:07.275+0000 [id=1]	INFO	org.eclipse.jetty.util.log.Log#initialized: Logging initialized @169ms to org.eclipse.jetty.util.log.JavaUtilLog
2025-04-05 01:14:07.325+0000 [id=1]	INFO	winstone.Logger#logInternal: Beginning extraction from war file
2025-04-05 01:14:07.336+0000 [id=1]	WARNING	o.e.j.s.handler.ContextHandler#setContextPath: Empty contextPath
2025-04-05 01:14:07.361+0000 [id=1]	INFO	org.eclipse.jetty.server.Server#doStart: jetty-9.4.45.v20220203; built: 2022-02-03T09:14:34.105Z; git: 4a0c91c0be53805e3fcffdcdcc9587d5301863db; jvm 17.0.14+7-Ubuntu-122.04.1
2025-04-05 01:14:07.472+0000 [id=1]	INFO	o.e.j.w.StandardDescriptorProcessor#visitServlet: NO JSP Support for /, did not find org.eclipse.jetty.jsp.JettyJspServlet
2025-04-05 01:14:07.487+0000 [id=1]	INFO	o.e.j.s.s.DefaultSessionIdManager#doStart: DefaultSessionIdManager workerName=node0
2025-04-05 01:14:07.487+0000 [id=1]	INFO	o.e.j.s.s.DefaultSessionIdManager#doStart: No SessionScavenger set, using defaults
2025-04-05 01:14:07.487+0000 [id=1]	INFO	o.e.j.server.session.HouseKeeper#startScavenging: node0 Scavenging every 600000ms
2025-04-05 01:14:07.663+0000 [id=1]	INFO	hudson.WebAppMain#contextInitialized: Jenkins home directory: /root/.jenkins found at: $user.home/.jenkins
2025-04-05 01:14:07.729+0000 [id=1]	INFO	o.e.j.s.handler.ContextHandler#doStart: Started w.@2c9399a4{Jenkins v2.346.3,/,file:///root/.jenkins/war/,AVAILABLE}{/root/.jenkins/war}
2025-04-05 01:14:07.748+0000 [id=1]	INFO	o.e.j.server.AbstractConnector#doStop: Stopped ServerConnector@8e24743{HTTP/1.1, (http/1.1)}{0.0.0.0:8087}
2025-04-05 01:14:07.748+0000 [id=1]	INFO	o.e.j.server.session.HouseKeeper#stopScavenging: node0 Stopped scavenging
2025-04-05 01:14:07.749+0000 [id=1]	INFO	hudson.WebAppMain#contextDestroyed: Shutting down a Jenkins instance that was still starting up
java.lang.Throwable: reason
	at hudson.WebAppMain.contextDestroyed(WebAppMain.java:383)
	at org.eclipse.jetty.server.handler.ContextHandler.callContextDestroyed(ContextHandler.java:1080)
	at org.eclipse.jetty.servlet.ServletContextHandler.callContextDestroyed(ServletContextHandler.java:584)
	at org.eclipse.jetty.server.handler.ContextHandler.contextDestroyed(ContextHandler.java:1043)
	at org.eclipse.jetty.servlet.ServletHandler.doStop(ServletHandler.java:319)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.stop(ContainerLifeCycle.java:180)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStop(ContainerLifeCycle.java:201)
	at org.eclipse.jetty.server.handler.AbstractHandler.doStop(AbstractHandler.java:108)
	at org.eclipse.jetty.security.SecurityHandler.doStop(SecurityHandler.java:430)
	at org.eclipse.jetty.security.ConstraintSecurityHandler.doStop(ConstraintSecurityHandler.java:423)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.stop(ContainerLifeCycle.java:180)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStop(ContainerLifeCycle.java:201)
	at org.eclipse.jetty.server.handler.AbstractHandler.doStop(AbstractHandler.java:108)
	at org.eclipse.jetty.server.session.SessionHandler.doStop(SessionHandler.java:520)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.stop(ContainerLifeCycle.java:180)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStop(ContainerLifeCycle.java:201)
	at org.eclipse.jetty.server.handler.AbstractHandler.doStop(AbstractHandler.java:108)
	at org.eclipse.jetty.server.handler.ContextHandler.stopContext(ContextHandler.java:1066)
	at org.eclipse.jetty.servlet.ServletContextHandler.stopContext(ServletContextHandler.java:386)
	at org.eclipse.jetty.webapp.WebAppContext.stopWebapp(WebAppContext.java:1454)
	at org.eclipse.jetty.webapp.WebAppContext.stopContext(WebAppContext.java:1420)
	at org.eclipse.jetty.server.handler.ContextHandler.doStop(ContextHandler.java:1120)
	at org.eclipse.jetty.servlet.ServletContextHandler.doStop(ServletContextHandler.java:297)
	at org.eclipse.jetty.webapp.WebAppContext.doStop(WebAppContext.java:547)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.stop(ContainerLifeCycle.java:180)
	at org.eclipse.jetty.util.component.ContainerLifeCycle.doStop(ContainerLifeCycle.java:201)
	at org.eclipse.jetty.server.handler.AbstractHandler.doStop(AbstractHandler.java:108)
	at org.eclipse.jetty.server.Server.doStop(Server.java:470)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.stop(AbstractLifeCycle.java:94)
	at winstone.Launcher.shutdown(Launcher.java:354)
	at winstone.Launcher.<init>(Launcher.java:217)
	at winstone.Launcher.main(Launcher.java:405)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:569)
	at Main._main(Main.java:342)
	at Main.main(Main.java:117)
2025-04-05 01:14:07.752+0000 [id=1]	INFO	o.e.j.s.handler.ContextHandler#doStop: Stopped w.@2c9399a4{Jenkins v2.346.3,/,null,STOPPED}{/root/.jenkins/war}
Exception in thread "Jenkins initialization thread" java.lang.NoClassDefFoundError: hudson/util/HudsonFailedToLoad
	at hudson.WebAppMain$3.run(WebAppMain.java:261)
Caused by: java.lang.ClassNotFoundException: hudson.util.HudsonFailedToLoad
	at java.base/java.net.URLClassLoader.findClass(URLClassLoader.java:445)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:592)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:525)
	at org.eclipse.jetty.webapp.WebAppClassLoader.loadClass(WebAppClassLoader.java:538)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:525)
	... 1 more
2025-04-05 01:14:07.758+0000 [id=1]	INFO	winstone.Logger#logInternal: Jetty shutdown successfully
java.io.IOException: Failed to start Jetty
	at winstone.Launcher.<init>(Launcher.java:206)
	at winstone.Launcher.main(Launcher.java:405)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:569)
	at Main._main(Main.java:342)
	at Main.main(Main.java:117)
Caused by: java.io.IOException: Failed to bind to 0.0.0.0/0.0.0.0:8087
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:349)
	at org.eclipse.jetty.server.ServerConnector.open(ServerConnector.java:310)
	at org.eclipse.jetty.server.AbstractNetworkConnector.doStart(AbstractNetworkConnector.java:80)
	at org.eclipse.jetty.server.ServerConnector.doStart(ServerConnector.java:234)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:73)
	at org.eclipse.jetty.server.Server.doStart(Server.java:401)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:73)
	at winstone.Launcher.<init>(Launcher.java:202)
	... 7 more
Caused by: java.net.BindException: Address already in use
	at java.base/sun.nio.ch.Net.bind0(Native Method)
	at java.base/sun.nio.ch.Net.bind(Net.java:555)
	at java.base/sun.nio.ch.ServerSocketChannelImpl.netBind(ServerSocketChannelImpl.java:337)
	at java.base/sun.nio.ch.ServerSocketChannelImpl.bind(ServerSocketChannelImpl.java:294)
	at java.base/sun.nio.ch.ServerSocketAdaptor.bind(ServerSocketAdaptor.java:89)
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:344)
	... 14 more
2025-04-05 01:14:07.758+0000 [id=1]	SEVERE	winstone.Logger#logInternal: Container startup failed
java.net.BindException: Address already in use
	at java.base/sun.nio.ch.Net.bind0(Native Method)
	at java.base/sun.nio.ch.Net.bind(Net.java:555)
	at java.base/sun.nio.ch.ServerSocketChannelImpl.netBind(ServerSocketChannelImpl.java:337)
	at java.base/sun.nio.ch.ServerSocketChannelImpl.bind(ServerSocketChannelImpl.java:294)
	at java.base/sun.nio.ch.ServerSocketAdaptor.bind(ServerSocketAdaptor.java:89)
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:344)
Caused: java.io.IOException: Failed to bind to 0.0.0.0/0.0.0.0:8087
	at org.eclipse.jetty.server.ServerConnector.openAcceptChannel(ServerConnector.java:349)
	at org.eclipse.jetty.server.ServerConnector.open(ServerConnector.java:310)
	at org.eclipse.jetty.server.AbstractNetworkConnector.doStart(AbstractNetworkConnector.java:80)
	at org.eclipse.jetty.server.ServerConnector.doStart(ServerConnector.java:234)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:73)
	at org.eclipse.jetty.server.Server.doStart(Server.java:401)
	at org.eclipse.jetty.util.component.AbstractLifeCycle.start(AbstractLifeCycle.java:73)
	at winstone.Launcher.<init>(Launcher.java:202)
Caused: java.io.IOException: Failed to start Jetty
	at winstone.Launcher.<init>(Launcher.java:206)
	at winstone.Launcher.main(Launcher.java:405)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:77)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:569)
	at Main._main(Main.java:342)
	at Main.main(Main.java:117)

