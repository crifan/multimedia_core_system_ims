# IMS概述

* `IMS`
  * `IMS`=`IP Multimedia Subsystem`=`Internet Protocol Multimedia Subsystem`=`IP多媒体子系统`
    * =`IMCNS`=`IM CN Subsystem`=`IP Multimedia Core Network Subsystem`=`IP多媒体核心网络子系统`
  * 是什么：一个基于互联网协议提供多媒体业务的体系架构
    * 属于3GPP组织旗下的
    * `3GPP`=`3rd Generation Partnership Project`
  * 作用：提供一种通用的架构，用来实现/提供VoIP和多媒体服务
  * 背景
    * 之前
      * 是一种创新方式，实现电信服务迁移
        * 旧
          * 服务：电话
          * 基于PS = 属于PS domain领域
        * 新
          * 领域：基于（端对端的）IP
          * 服务：各种新（多媒体）服务
    * 用于访问IMS服务的方式
      * CS=Circuit Switched
      * PS=Packet Switched
    * 3GPP设计（引入）IMS是作为PS的扩展
      * 后来又支持新的，基于IP的多媒体服务
        * 应该理解为：
          * IMS不仅是个服务，更是个框架
            * 底层：基于数据包packet
            * 实现了：高级IP服务和应用
  * 发展历史
    * IMS发展历史
      * 3GPP R5
        * 第一次提出IMS概念：
        * 2G发展到3G阶段，出现W-CDMA网络（UMTS）
        * 基于SIP多媒体领域（domain） 加到了 NGN网络
          * 也支持GSM和GPRS网络
      * 3GPP R6
        * 新增支持WLAN的互联（interworking）
      * 3GPP R7
        * 支持固定网络，和TISPAN一起支持更多类型网络
          * 其内部是：SOA=Subsystem-Oriented Architecture=面向子系统的架构
      * 出现 Early IMS=早期IMS
        * 支持IPv4网络
        * 为IPv6提供扩展路径
      * 最新叫法：IMS = core IMS
    * 蜂窝网络发展历史
      * 1G
        * 使用模拟信号传输
        * 只支持CS传输电话语音
      * 2G
        * 全数字
        * 支持CS的语音和数据（传输）服务
      * 2.5G
        * 新增PS交换数据服务
          * 在2G基础上
      * 3G
        * （尝试）提供基于PS的全部类型的服务
          * 包括传统的电话语音
  * 特点
    * 模块化modular
    * 可扩展extendable
  * 背景
    * 文字
      * 传统移动电话使用类电路交换网络提供语音通话服务
        * 而非使用计算机分组交换通信方式的网络。
      * 虽然已有很多方式在智能手机上提供网络电话与其他互联网多媒体服务
        * 但并未形成行业标准
      * IMS则为此提供了一个标准化体系架构
    * 图
      * 应用演化直到IMS
        * ![application_evolution_to_ims](../assets/img/application_evolution_to_ims.png)
      * 希望用IMS实现各种功能和服务
        * ![ims_implemented_various_app](../assets/img/ims_implemented_various_app.png)
  * 接入方式=接入网络
    * 早期
      * GPRS
    * 后续：支持其他
      * WLAN
      * CDMA2000
      * 固定电话线
      * 等
  * 新应用
      * presence information 
      * video conferencing
      * POC=Push to talk over Cellular
      * multiparty gaming
      * community services
      * content sharing