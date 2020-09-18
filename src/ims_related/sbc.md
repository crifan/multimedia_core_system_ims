# SBC

* `SBC`=`Session Border Controller`=`会话边界控制器`
  * 是什么：一个 控制器=网络节点=网络元素
    * 位置：
      * 位于`IMS`系统中
      * 介于2个网络之间的
    * 作用：控制所有的数据传输
      * 包括
        * 信号signalling
        * （媒体）数据media
  * 协议
    * `rfc5853`
      * https://tools.ietf.org/html/rfc5853
  * 用于解决各种问题
    * 多种（访问 接入）网络multiple access networks
      * IPv4/IPv6
      * SIP normalization
      * VPNs
    * 安全问题security issues
      * DOS attacks
      * topology hiding
      * 加密
        * 信号：TLS和IPSec
        * 媒体数据：SRTP
    * legislative issues=Regulatory=管制
      * emergency calls
      * legal intercept
      * interworking
    * 媒体相关问题media related problems
      * QoS
      * transcoding
      * media security
  * 实际作用
    * 最早：作为`NAT`
      * SBC as a NAT
        * ![sbc_as_a_nat](../assets/img/sbc_as_a_nat.png)
      * 具体例子
        * VoLTE Call – Data Path
          * ![sbc_example_volte_call_path](../assets/img/sbc_example_volte_call_path.png)
  * 现状
    * 各种类型SBC
      * `A-SBC`
      * `I-SBC`
      * `ICS-SBC`
      * `Enterprise SBC`
      * `Trunking SBC`
      * `WebRTC GW`
    * 功能重叠或独立
      * 某些功能可以独立出其他模块
        * 比如
          * `P-CSCF`
          * `E-CSCF`
    * 最新：把SBC理解为负责**安全**和**连接**方面的功能
    * 其他一些也可以被视为SBC的
        * `CBGF`
        * `E-CSCF`
        * `ATCF`
        * `ATGW`
        * `EATF`
        * `WebRTC GW`
        * `ICE`
  * 从IMS角度
    * 2种类型SBC
      * 包含
        * `A-SBC`=`Access-SBC`
          * 架构
            * ![sbc_ims_a_sbc](../assets/img/sbc_ims_a_sbc.png)
          * 相关内容=对应功能
            * `P-CSCF`=`Proxy Call Session Control Function`
            * `IMS-ALG`=`IMS Application Level Gateway`
            * `IMS-AGW`=`IMS Access Gateway`
        * `I-SBC`=`Interconnecting-SBC`
          * 相关内容=对应功能
            * `IBCF`=`Interconnection Border Control Function`
            * `TrGW`=`Translation Gateway`
            * `THIG`=`Topology Hiding Interwork Gateway`
            * `IWF`
    * 对比
      * A-SBC and I-SBC
        * ![a_sbc_i_sbc](../assets/img/a_sbc_i_sbc.png)
      * 稍微复杂点的情况
        * Call Forwarding and LI and Interconnect
          * ![sbc_calling_forward_li](../assets/img/sbc_calling_forward_li.png)
  * 漫游往往涉及到SBC
    * 可能方案1
      * ![sbc_roaming_solution_1](../assets/img/sbc_roaming_solution_1.png)
    * 可能方案2
      * ![sbc_roaming_solution_2](../assets/img/sbc_roaming_solution_2.png)
    * 可能方案3
      * ![sbc_roaming_solution_3](../assets/img/sbc_roaming_solution_3.png)
    * LBO-VR with OMR
      * ![sbc_lbo_vr_omr](../assets/img/sbc_lbo_vr_omr.png)
    * LBO-HR
      * ![sbc_lbo_hr](../assets/img/sbc_lbo_hr.png)
  * 其他相关架构
    * Logical Position of D-SBC and SmartEdge BGF in IMS or Other Multimedia Networks
      * ![d_sbc_smartedge_bgf_ims](../assets/img/d_sbc_smartedge_bgf_ims.png)
