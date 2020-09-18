# MRF

* `MRF`
  * =`Media Resource Function`=`媒体资源功能组`
  * 提供与媒体相关的功能，包括媒体处理（如混音）、播放拨号音和语音提示
  * 进一步划分为
    * `MRFC`=`Media Resource Function Controller`=`媒体资源功能控制器`
      * MRFC是信号层面的节点，它根据来自AS和S-CSCF的信息来操控MRFP
      * 作用类似于：SIP B2BUA
    * `MRFP`=`Media Resource Function Processor`=`媒体资源功能处理器`
      * MRFP是媒体层面的节点，用来混合、产生或者处理媒体流。
      * 它也可以管理共享资源的访问权限
  * `MRB`
    * =`Media Resource Broker`=`媒体资源协商器`
    * 一个功能实体。
    * 负责收集已经发布的MRF信息，并且向AS这样的信息消费实体提供适当的MRF信息。
    * MRB通常有两个模式：
      * 查询模式：AS主动查询MRB相应的媒体并且创建使用MRB回应的调用。
      * 线性模式：AS向MRB发送SIP INVITE，由MRB创建调用。
