## 让 tekton 在 kubernetes 的安装变简单
由于 tekton 相关的 docker 镜像在 google 的镜像仓库（gcr.io），一般在国内无法拉取，
所以将镜像同步到了阿里云镜像仓库。

本项目旨在让 tekton 在 kubernetes 的安装变简单。

## tekton 版本支持
目前支持的 tekton 版本：
* v0.23.0

## 使用方式

由于原始的 release.yml 中的镜像使用了 sha256 校验码，而镜像同步到阿里云仓库后，sha256 校验码发生了变化，pull 到本地后也没有 sha256 校验码信息，
所以这里使用阿里云镜像仓库的镜像替换了 release.yml 文件中的 gcr.io 的镜像。

使用 kubectl 命令安装 tekton：
```bash
kubectl release.yaml
```
