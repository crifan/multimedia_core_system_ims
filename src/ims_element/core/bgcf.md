# BGCF

* `BGCF`
  * =`Breakout Gateway Control Function`=`出口网关控制功能`
  * 是一个SIP代理，它处理来自S-CSCF的路由请求。
  * BGCF有基于电话号码的路由功能，用来选择与PSTN网络的接口点。
  * 当BGCF发现被叫网络位于一个PSTN网络时，BGCF就选择一个媒体网关控制功能(MGCF)，将会话路由到MGCF，MGCF负责与PSTN网络交互。
