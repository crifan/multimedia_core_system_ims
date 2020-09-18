# TISPAN

此处整理`TISPAN`相关内容。

* `TISPAN`=`tispan`
  * 一句话简介：`ETSI`下的一个工作组
    * 是NGN的具体实现方案
      * the NGN global solution
    * 往往也叫：`TISPAN NGN`
  * 起源
    * 2003年9月成立
    * 合并自
      * SPAN=Services and Protocols for Advanced Networks
        * 一个合并后的工作小组
          * 合并自
            * SPS=Services, Protocols & Switching
            *  NA=Network Aspects
        * 主要负责EURO-ISDN
      * TIPHON=Telecommunications and Internet Protocol Harmonization Over Networks
        * 1997年成立的
        * 一个ETSI的项目
        * 最开始研究VoIP
        * 后来扩展到基于IP传输任何电信（包括MM=Multimedia=多媒体）数据
  * （TISPAN NGN ）架构=architecture
    * 总体架构
      * ![tispan_r1_architecture](../../assets/img/tispan_r1_architecture.png)
      * ![tispan_architecture_overview](../../assets/img/tispan_architecture_overview.png)
      * ![tispan_ngn_global_solution](../../assets/img/tispan_ngn_global_solution.png)
    * 架构含义解释
      * 最初
        * ![tispan_r1_arch_inital](../../assets/img/tispan_r1_arch_inital.png)
      * NASS子系统 负责接入：地址管理、授权和认证等
        * ![tispan_r1_arch_nass](../../assets/img/tispan_r1_arch_nass.png)
      * RACS子系统：负责会话管理和控制
        * ![tispan_r1_arch_racs](../../assets/img/tispan_r1_arch_racs.png)
      * PSTN Emulation=PSTN仿真：支持非IMS的旧有系统
        * ![tispan_r1_arch_pstn_emulation](../../assets/img/tispan_r1_arch_pstn_emulation.png)
  * 相关内容
    * 生态和协议
      * 概述
        * ![tispan_eco_system_overview](../../assets/img/tispan_eco_system_overview.png)
    * IPTV方面
      * IPTV协议生态
        * ![tispan_iptv_standard_eco](../../assets/img/tispan_iptv_standard_eco.png)
      * IPTV相关协议
        * ![tispan_iptv_specifications](../../assets/img/tispan_iptv_specifications.png)
      * IMS-based IPTV vs Integrated IPTV
        * Specification协议规范
          * ![iptv_ims_based_integrated](../../assets/img/iptv_ims_based_integrated.png)
        * Protocols Used
          * ![iptv_ims_dedicated_protocol](../../assets/img/iptv_ims_dedicated_protocol.png)
        * 特点Characteristic
          * ![tispan_non_ngn_ngn_iptv_feature_1](../../assets/img/tispan_non_ngn_ngn_iptv_feature_1.png)
          * ![tispan_non_ngn_ngn_iptv_feature_2](../../assets/img/tispan_non_ngn_ngn_iptv_feature_2.png)
          * ![tispan_non_ngn_ngn_iptv_feature_3](../../assets/img/tispan_non_ngn_ngn_iptv_feature_3.png)
          * ![tispan_non_ngn_ngn_iptv_feature_4](../../assets/img/tispan_non_ngn_ngn_iptv_feature_4.png)
    * 测试方面
      * ![tispan_testing_ecosystem](../../assets/img/tispan_testing_ecosystem.png)
    * Home Network相关
      * Home Networking Security
        * ![tispan_home_net_security](../../assets/img/tispan_home_net_security.png)
      * Service Requirements
        * ![tispan_service_requirements](../../assets/img/tispan_service_requirements.png)
      * 架构和协议
        * 说明
          * TISPAN sees Home Networks as an IMS NGN end-point
        * Architecture Specifications
          * ![tispan_arch_specifications](../../assets/img/tispan_arch_specifications.png)
        * IPTV Specifications
          * ![etsi_iptv_specifications](../../assets/img/etsi_iptv_specifications.png)
        * Security, Energy Monitoring
          * ![etsi_security_monitor_specifications](../../assets/img/etsi_security_monitor_specifications.png)
        * TV URI
          * ![etsi_tv_uri_specifications](../../assets/img/etsi_tv_uri_specifications.png)
      * Home Networking Details详情
        * ![etsi_home_net_detail](../../assets/img/etsi_home_net_detail.png)

---

* 总体内容和架构
  * 文字版
      * Service Layer Model
        * Subsystems
          * Core
            * IMS= IP Multimedia Subsystem
          * Other
            * PES=PSTN/ISDN Emulation subsystem
              * IPTV Subsystem
        * Common components
          * UPSF=User Profile Server Function
          * SLF=Subscription Locator Function
          * ASF=Application Server Function
          * IWF=Interworking Function
      * Transport layer
        * Transport control sublayer
          * NASS=Network Attachment Subsystem
          * RACS=Resource and Admission Control Subsystem
        * Transport processing function
          * BGF=Border Gateway Function
          * RCEF=Resource Control Enforcement Function
          * ARF=Access Relay Function
          * MGF=Media Gateway Function
          * MRFP=Media Resource Function Processor
          * SGF=Signalling Gateway Function
          * AMF=Access Management Function
          * BTF=Basic Transport Function
            * EFF=Elementary Forwarding Function
            * ECF=Elementary Control Function
      * UE=User Equipment
  * 图
    * TISPAN NGN overall architecture
      * ![tispan_ngn_overall_architecture](../../assets/img/tispan_ngn_overall_architecture.png)
    * Example architecture with xDSL access
      * ![tispan_ngn_arch_example_xdsl](../../assets/img/tispan_ngn_arch_example_xdsl.png)
    * Transport processing functions overview
      * ![tispan_ngn_arch_transport_process](../../assets/img/tispan_ngn_arch_transport_process.png)
    * TISPAN R1参考模型
      * ![tispan_r1_refer_model](../../assets/img/tispan_r1_refer_model.png)
      * ![tispan_ims_refer_model](../../assets/img/tispan_ims_refer_model.png)
* TISPAN 不同模块内容
  * Distributed subsystems
    * ![tispan_module_distributed_subsys](../../assets/img/tispan_module_distributed_subsys.png)
  * Access and aggregation segments
    * ![tispan_module_access_aggregation_seg](../../assets/img/tispan_module_access_aggregation_seg.png)
  * Common components overview
    * ![tispan_module_common_component](../../assets/img/tispan_module_common_component.png)
  * Charging and Data Collection Functions
    * ![tispan_module_charging_data](../../assets/img/tispan_module_charging_data.png)
  * Network interconnection at transfer level
    * ![tispan_module_net_interconn_transfer](../../assets/img/tispan_module_net_interconn_transfer.png)
  * `User Equipment`=`UE`
    * ![tispan_module_user_equipment](../../assets/img/tispan_module_user_equipment.png)
    * 说明
      * `UE`=`User Equipment`
      * `TE`=`Terminal Equipment`
      * `CPN`=`Customer Premises Network`
      * `CND`=`Customer Network Devices`
      * `CNG`=`Customer Network Gateway`
      * `R-MGF`=`Residential MGF`
  * Authentication
    * NGN Authentication Levels
      * ![ngn_auth_level](../../assets/img/ngn_auth_level.png)
