# hub-mirror

使用 docker.io 来提供（但不限于） gcr.io、k8s.gcr.io、quay.io、ghcr.io 等国外镜像加速下载服务

# 使用


## 12. 自己动手，Fork 本项目，开启 issues 并绑定你自己的 Docker 账号

开启 `Settings`-`Options`-`Features` 中的 `Issues` 功能

在 `Settings`-`Secrets` 新建 `DOCKERHUB_USERNAME`（你的 Docker 用户名） 和 `DOCKERHUB_TOKEN`（你的 Docker 密码） 两个 Secrets

在 `Issues`-`Labels` 添加三个 label ：`hub-mirror`、`success`、`failure`

最后在 `Actions` 里选择 `hub-mirror` ，在右边 `···` 菜单里选择 `Enable Workflow`

## 2. 已有魔法，本地使用

```shell
go install github.com/myysophia/hub-mirror
```

```shell
hub-mirror --username=xxxxxx --password=xxxxxx --content='{ "hub-mirror": ["gcr.io/google-samples/microservices-demo/emailservice:v0.3.5"] }'
```

