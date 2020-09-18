# OSA

* OSA
  * `OSA`=`Open Service Access`
  * 主要包含3个部分
    * Applications
      * 举例：VPN, conferencing, location based applications
      * 说明
        * 单个应用可能由一个或多个AS而实现
          * AS=应用服务器
    * Framework
      * Authentication
      * Registration
      * discovery function
    * 一堆的`SCS`=`Service Capability Server`
      * 提供服务的服务器
        * 服务
          * 举例
            * Call Control
            * User Location
      * 举例
        * `CAMEL`
        * `MExE`
  * 架构概览
    * Overview of Open Service Access
      * ![open_service_access_overview](../../assets/img/open_service_access_overview.png)
      * ![osa_parlay_scf](../../assets/img/osa_parlay_scf.jpg)
  * OSA和其他架构关系
    * ![osa_parlay_3gpp](../../assets/img/osa_parlay_3gpp.jpg)
    * ![osa_ims_call_state_ctrl_sip_routing](../../assets/img/osa_ims_call_state_ctrl_sip_routing.png)
* `OSA SCS`
  * `OSA SCS`=`OSA-SCS`=`OSA Service Capability Server`
  * 作用：相当于一个安全网关，介于底层网络和OSA架构中的应用
    * 方便应用层访问（底层）网络的功能
        * 提供了一个统一的接口
          * 比如
            * OSA API
              * 分2种
                * OSA API：对外部
                * OSA internal API：对内部
              * Parlay X Web Service
        * 其中
          * 网络功能Network Functionality
            * 被称为
              * `SCF`=`Service Capability Feature`
                * 也叫 Services
        * 总结
          * 此处：`SCF`=`Service`=`Network Functionality`
  * 细节
    * `OSA`的3个主要部分之一
