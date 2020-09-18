
# AS

* `AS`=`Application Server`=`应用服务器`
  * 作用：负责和提供SIP应用服务器服务
  * 其他说明
    * 它与`S-CSCF`之间使用`SIP`
  * 模式
    * 基于具体的服务不同，AS可以选择不同的SIP模式
      * SIP代理模式
      * SIP用户代理（`UA`=`User Agent`）模式
      * `SIP B2BUA`模式
  * 部署位置
    * 可以设置在：IMS本网内
      * 如果位于本网，它还可以使用Sh或Si接口查询HSS。
    * 也可以设置在：外部的第三方网络
  * 典型案例
    * `VCC Server`
      * 由3GPP开发的语音持续调用功能
    * `SIP AS`
      * 负责和提供IMS具体服务
    * `IM-SSF`
      * =`IP Multimedia Service Switching Function`=`IP多媒体切换功能`
      * `SIP`和`CAP`之间的接口，用于与`CAMEL`应用服务器通信
    * `OSA SCS`
      * =`OSA Service Capability Server`=`OSA服务性能服务器`
        * `OSA`=`Open Service Architecture`=`开放服务架构`
      * `SIP`和`OSA`框架之间的接口
      * 多个`OSA`服务之间的交互
  * 功能模型
    * `AD-ILCM`和`AS-OLCM`用来保存事务状态并且可以根据特定服务的需要保存会话状态
    * 对于`S-CSCF`来说
      * `AS-ILCM`接口是输入端
      * `AS-OLCM`接口是输出端
    * 应用逻辑提供服务和`AS-ILCM`、`AS-OLCM`之间的交互
  * `PSI`
    * =`Public Service Identity`=`公共服务标识`
    * 用来标识应用服务提供的服务
    * `PSI`可以提供两种标识格式
      * `SIP URI`
      * `Tel URI`
    * 通常被`HSS`以完整`PSI`或通配`PSI`保存
    * 说明
      * 完整`PSI`包含完整的`PSI`标识，可以直接用来路游
      * 通配`PSI`表达一组`PSI`标识

## IMS-SSF

* `IMS-SSF`
  * `IMS-SSF`=`IMS - Service Switching`=`IM-SSF`
  * 是什么：相当于一个网管gateway
    * 介于两者之间
      * 基于`SIP/Diameter`的`IMS`
      * 基于`CAP`的`CAMEL`的`AS`
    * 实现互相转换
      * `SIP/Diameter`的消息
      * `CAP`的消息
