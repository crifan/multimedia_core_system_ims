# 用户标识=User identities

* `用户标识`=`User Identities`=`User Identitiy`
  * IMS可以使用多种用户标识
    * IMPI=IP Multimedia Private Identity=IP多媒体私有标识
      * 一种由主网络操作者永久性分派的全局性标识
      * 可以用于注册、认证、管理和计费等用途
      * 每个IMS用户可以有多个IMPI
    * IMPU=IP Multimedia PUblic Identity=IP多媒体公共标识
      * 当IMS用户想要和其他用户通信时，需要使用IP多媒体公有标识
        * 它可以写在那个人的名片上
      * IMS允许一个IMPI上绑定多个IMPU。
      * IMPU也可以和其它电话共享
        * 就像一个家庭使用一个电话号码
    * WPUI=Wildcarded Public User Identity=通配公共享户标识
      * 表示一组相似的IMPU
    * GRUU=Globally Routable User Agent URI=全局可路游用户代理统一资源标识符
      * 一个由IMPU和UE实例组成的标识符
      * IMS中有两类GRUU
        * 公共GRUU(P-GRUU)
          * 明示了用户的IMPU并且长期有效
        * 临时GRUU(T-GRUU)
          * 隐藏了用户的IMPU
          * 当用户显式注销T-GRUU或者过了有效期时，T-GRUU就会失效
  * 说明
    * IMPI和IMPU是一种URI
      * URI=统一资源标识符
    * 它可以是
      * 数字：Tel URI
        * 举例
          * `tel: +1-555-123-4567`
      * 字符标识符SIP URI
        * 举例：
          * `sip:john.doe@example.com`
    * 去掉前缀后
      * 举例
        * `+31 72 5621771`
        * `sales@vc4.com`

## IMS中用户身份和编号基础知识

* IMS中用户身份和编号 基础知识
  * ISIM文件结构
    * ![imsm_file_structure](../../assets/img/isim_file_structure.png)
  * ADFI SIM包含内容
    * EF<b><sub>IMPI</sub></b> – IMS private user identity,
    * EF<b><sub>DOMAIN</sub></b> - Home Network Domain Name,
    * EF<b><sub>IMPU</sub></b> - IMS Public User Identity (one or more),
    * EF<b><sub>AD</sub></b> - Administrative Data (UE operation mode, e.g. normal or type approval),
    * EF<b><sub>ARR</sub></b> - Access Rule Reference (access rules for files located under the ISIM ADF),
    * EF<b><sub>IST</sub></b> - ISIM Service Table (lists available optional services:P-CSCF address, Generic Bootstrapping Architecture (GBA), HTTP Digest, GBA-based Local Key Establishment Mechanism, support of P-CSCF discovery for IMS local break out),
    * EF<b><sub>P-CSCF</sub></b> - P-CSCF Address (one or more),
    * EF<b><sub>GBABP</sub></b> - GBA Bootstrapping parameters (contains the AKA Random challenge (RAND) and Bootstrapping Transaction Identifier (B-TID) associate with a GBA bootstrapping procedure),
    * EF<b><sub>GBANL</sub></b> - GBA NAF List (contains the list of NAF_ID and B-TID associated to a GBA NAF derivation procedure)
    * EF<b><sub>NAFKCA</sub></b> - NAF Key Centre Address (one or more).
  * home domain
    * Home network domain name
      * ![home_network_domain_name](../../assets/img/home_network_domain_name.png)
      * 对应标准：`IETF RFC 1035`
      * Home network domain name derivation from IMSI
        * ![home_network_domain_name_from_imsi](../../assets/img/home_network_domain_name_from_imsi.png)
  * IMPI
    * Private user identity=Private Identity=IP Multimedia Private Identity=IMPI
    * 每个IMS用户都有一个Private User Identities
      * 是Home Network Operator网络运营商？分配的
    * 用途
      * Registration注册
      * Authorisation授权
      * Administration管理
      * Accounting计费
    * 形式
      * NAI=Network Access Identifier
      * 语法：username@realm
    * 举例
      * ![impi_example_private_use_identity](../../assets/img/impi_example_private_use_identity.png)
    * Private User Identity derivation from IMSI
      * 3GPP中没有IMSI，所以需要从IMSI中推算出来
        * IMSI=International Mobile Subscriber Identity=国际移动用户识别码
      * Private user identity derivation from IMSI
        * ![private_user_identity_from_imsi](../../assets/img/private_user_identity_from_imsi.png)
  * IMPU
    * =Public User Identity=Public identity=IP Multimedia PUblic identity=IMPU
    * 概述
      * 每个IMS用户都有1或多个IMPU
      * 任何用户都可以用IMPU去和其他用户通信
        * 例如，可以被包含到一个商务名片中
    * 格式
      * 种类
        * SIP URI
          * 协议标准：IETF RFC 3261
          * 格式：sip:username@domain
        * Tel URI
          * 协议标准：`IETF RFC 3966`
            * `E.164 number`
          * 格式：`tel:<Global Number>`
            * 说明
              * 不带分隔符
                * contains a global number without visual separators
    * 举例
      * 文字
        * SIP URI
          * `sip:jakub.bluszcz@ekiga.net`
        * Tel URI
          * `tel:48399571981`
        * SIP URI
          * `sip:+1-212-555-1212 @gateway.com;user=phone`
      * 图
        * ![public_user_identity](../../assets/img/public_user_identity.png)
  * WPUI=Wildcarded Public User Identity=通配公共享户标识
    * IMPU可能会被以WPUI的方式存储在HSS中
    * WPUI目的是为了针对注册了大量的账号，且其处理方式都类似的场景实现优化
      * 保存成一组类似的账号
          * 也就是：WPUI=Wildcarded Public User Identity
    * 语法
      * 会用到ERE=Extended Regular Expression=扩展正则表达式
        * 分隔符delimiter是：感叹号！
    * 举例
      * `sip:user!.*!@example.com`
      * `tel:4832376630!.*!`
      * 图
        * ![wildcarded_user_identity](../../assets/img/wildcarded_user_identity.png)
  * IMPI 和 IMPU 关系
    * Relationship of Private and Public User Identities
      * ![private_and_public_use_identity_relation](../../assets/img/private_and_public_use_identity_relation.png)
