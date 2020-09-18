# IMS用户认证

* IMS认证总体流程
  * 3GPP网络环境中，即使IMS（订阅）用户通过了PS域的认证，也还要经过IMS的IMPI的认证，才能继续访问IMS的服务
  * -》即2步认证
    * 第一步：`PS`的认证
      * 具体实现：`3GPP AKA`
    * 第二步：`IMS`的`IMPI`
      * 具体实现：`IMS AKA`
  * 图
    * ![3gpp_aka_vs_ims_aka](../../assets/img/3gpp_aka_vs_ims_aka.png)
* 相关名词
  * `IMPI`=`IP Multimedia Private Identity`=`IP多媒体私有识别码`
  * `AKA`=`Authentication and Key Agreement`=`认证和密钥协商`
    * 常称为：`3GPP AKA`
* `UTMS AKA`
  * UTMS中的双向认证机制叫做：`UTMS AKA`
* `IMS AKA`
  * 认证流程
    * 认证成功
      * ![ims_aka_successful](../../assets/img/ims_aka_successful.png)
    * 用户认证失败
      * ![ims_aka_user_auth_failure](../../assets/img/ims_aka_user_auth_failure.png)
    * 网络认证失败
      * ![ims_aka_net_auth_failure](../../assets/img/ims_aka_net_auth_failure.png)
    * 同步失败
      * ![ims_aka_net_sync_failure](../../assets/img/ims_aka_net_sync_failure.png)
* Session Mode Messaging CallFlow
  * ![ims_session_mode_msg_callflow](../../assets/img/ims_session_mode_msg_callflow.png)
* IMS注册和认证 架构
  * IMS Registration – access networks
    * ![ims_registration_access_network](../../assets/img/ims_registration_access_network.png)
  * VoLTE Registration
    * ![ims_volte_registration](../../assets/img/ims_volte_registration.png)
  * 3GPP AKA
    * ![3gpp_aka_flow](../../assets/img/3gpp_aka_flow.png)
  * IMS AKA
    * ![ims_aka_flow](../../assets/img/ims_aka_flow.png)
  * IMS Registration
    * ![ims_reg_flow](../../assets/img/ims_reg_flow.png)
