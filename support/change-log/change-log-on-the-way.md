Kuboard v1.0.x 的更新说明






必须完成：
* 文档
* 教程

* 群反馈 Pod 列表界面出现重复数据的问题

------------------
* 按名称空间查看 Events
* 按名称空间查看 top pods
* 修改 metadata.labels kuboard v1.0.7
* 支持 Headless Service
* 在服务器端配置 openid connect 的 client_secret 以增强安全性

* 安装文档中，将 daocloud 的镜像地址修改为阿里云的镜像地址
* 日志界面支持 ctrl + F
* 更新版本时，可以通过下拉列表选择仓库中的版本号
* 导入导出时，需要支持 nfs 等类型的数据卷

* 工作负载查看 --> 未显示 SecurityContext
* EndPoint
* 导入工作负载时，如果存储类没有 annotations，不应该报错
* 表单校验：数据卷名不能带小数点
* Prometheus 监控
* Limit Range

* https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/


* 容器组列表，筛选结果为空时，提示筛选 “其他”

* https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/

* https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/ha-topology/  专题：ETCD 集群是如何setup起来的

* Service --> SessionAffinity
              --> clientIP.timeoutSeconds
* Service --> .spec.clusterIP


* 存储卷声明去掉分配模式的字段
* 删除容器组时 - graceful period
* Pod Conditions: lastProbeTime/reason/message
* 显示 Deployment/StatefulSet/DaemonSet 的事件
* 控制台/日志界面，按 名称空间/工作负载/Pod/容器 进行切换
* StatefulSet 在 available 数与 replicas 数不一致时，链接到帮助提示


# 用户认证相关

* Gitlab
  * GitLab 的 idtoken 中只包含 sub 字段（此处的含义为用户的ID），没有用户名和邮箱地址等信息，因此不能直接和 Kubernetes OpenID Connect 对接
    *  https://docs.gitlab.com/ee/integration/openid_connect_provider.html#shared-information
