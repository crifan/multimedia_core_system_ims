# HSS

* `HSS`=`Home Subscriber Server`=`归属用户服务器`=`HSS用户数据库`
  * 功能
    * Stores all the static and dynamic information for a subscriber
    * Maintains a list of features and services associated with a user, and also the location and means of access to the user
    * Provides user profile information
  * 主用户数据库
    * 它为IMS网络中实际管理通话的实体提供支持
    * 如访问用户相关的信息（称之为用户配置），对用户认证和授权以及 提供用户位置IP地址等相关信息
    * 在同时使用多个HSS时，需要SLF映射用户保存的位置
      * SLF=Subscriber Location Function=用户位置功能组
      * 即当查询某个用户配置时，由SLF指出哪个HSS保存了这个用户配置
  * 保存用户信息
    * `IMPU`
    * `IMPI`
    * `IMSI`=`国际移动用户标识符`
    * `MSISDN`
    * 用户服务配置
    * 服务开关
    * 其它信息
  * 其他说明
    * 类似的
      * GSM的
        * `HLR`=`Home Location Regiser`=`归属位置寄存器`
        * `AuC`=`Authentication Centre`=`认证中心`
