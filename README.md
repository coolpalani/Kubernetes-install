# Kubernetes-install

本篇文章主要介绍kubernetes v1.9.x版本(启用TLS bootstrap认证方式)的安装步骤和注意事项；而不是使用kubeadm等自动化方式来部署集群。

安装步骤和流程，Kubernetes搭建部分参考文章：`和我一步步部署kubernetes集群`。主要修改：移除Token认证，增加了Node TLS bootstrap认证，后面增加了Prometheus监控报警，日志搜集等等；以及简单说明各个组件和服务的原理和作用。

本篇文章主要包含几部分：Kubernetes ipvs模式，CoreDNS，监控报警，日志搜集，私有仓库等等一系列解决方案；安装过程中，可能不会详细说明各组件的启动参数和作用；启动参数的详细介绍请参考其他的优秀博客和官方文档。

所有服务的搭建过程均在CentOS7，内核版本：4.4.xx系统上操作通过，其他系统未验证，有任何问题欢迎反馈。

## 步骤列表

1. [创建TLS证书和秘钥](创建TLS证书和秘钥.md)
1. [搭建etcd集群服务](搭建etcd集群服务.md)
1. [搭建flannel服务](搭建flannel服务.md)
1. [搭建Kubrnetes-Master节点](搭建Kubrnetes-Master节点.md)
1. [搭建Kubrnetes-Node节点](搭建Kubrnetes-Node节点.md)
1. [部署CoreDNS服务](部署CoreDNS插件.md)
1. [部署Dashboard插件](部署Dashboard插件.md)
1. [搭建Prometheus服务](搭建Prometheus服务.md)
1. [搭建Grafana服务](搭建Grafana服务.md)
1. [搭建Alertmanager服务](搭建Alertmanager服务.md)
1. [后续相关组件待补充......](后续相关组件待补充.md)
