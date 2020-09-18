# SIP授权认证

* SIP confidentiality and integrity
  * 相关
    * `ESP`=（IPsec 的）`Encapsulating Security Payload`
    * `SA`=`Security Association`=`安全关联`
  * 建立安全关联
    * ![security_associaton_setup](../../assets/img/security_associaton_setup.png)
  * `SA1`和`SA2`的使用
    * ![sa1_sa2_usage](../../assets/img/sa1_sa2_usage.png)
* SIP Digest
  * 是一种认证方法，只适用于非3GPP的访问网络
  * 基于`HTTP DIGEST`，实现UE和HE之间的双向认证
  * SIP Digest
    * ![sip_digest_flow](../../assets/img/sip_digest_flow.png)
    * ![sip_digest_variables](../../assets/img/sip_digest_variables.png)
* SIP Digest with TLS
  * SIP Digest with TLS
    * ![sip_digest_with_tls](../../assets/img/sip_digest_with_tls.png)
* `GIBA`=`GPRS-IMS-Bundled Authentication`
  * 背景：
    * 3GPP的IMS安全功能，很好
    * 但是早期的时候，早期设备，并不能很好的支持这方面的功能
    * 比如早期的2G手机，不支持`USIM`、`ISIM`
      * 因为本身不支持`IPsec`
    * 需要一个简单但够用的安全机制
    * -》出现了：`GIBA`
  * 别名：`early IMS security`=`早期IMS安全（机制）`
  * 原理
    * 在`HSS`中创建一个安全绑定
      * 在两者之间
        * `SIP`级的标识 ：公开/私有的用户身份
        * `GRPS`级别的 承载/网络层的标识：IP地址
  * GIBA认证流程
    * ![giba_auth_flow](../../assets/img/giba_auth_flow.png)
* `GAA`=`Generic Authentication Architecture`
  * 背景：
    * 许多应用（程序）都有个需求是，在通讯之前，实现互相认证，以实现在一个客户端（比如UE）和一个AS（应用程序服务器）的通讯
    * 所以需要一个通用认证的架构
    * -》`GAA`
  * GAA应用举例
    * ![gaa_usage_example](../../assets/img/gaa_usage_example.png)
  * GAA机制签发资格证书
    * ![gaa_mechanisms_issue_auth](../../assets/img/gaa_mechanisms_issue_auth.png)
* `GBA`
  * =`Generic Bootstrapping Architecture`=`通用引导架构`
  * GBA架构
    * ![gba_arch](../../assets/img/gba_arch.png)
  * 服务发现过程
    * `BSF`地址
      * ![gba_bsf_address](../../assets/img/gba_bsf_address.png)
  * 引导初始化
    * GBA的引导过程的初始阶段
      * ![gba_initial_bootstrapping](../../assets/img/gba_initial_bootstrapping.png)
    * GBA引导过程
      * ![gba_bootstrapping_procedure](../../assets/img/gba_bootstrapping_procedure.png)
    * GBA引导使用过程
      * ![gba_bootstrapping_usage_procedure](../../assets/img/gba_bootstrapping_usage_procedure.png)
  * `SSC`架构
    * 签发证书
      * ![ssc_arch_cert_issue](../../assets/img/ssc_arch_cert_issue.png)
  * 相关
    * `BSF`=`Bootstrapping Server Function`
    * `NAF`=`Network Application Function`
