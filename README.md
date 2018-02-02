# Sentry On-Premise

fork from https://github.com/getsentry/onpremise

## 做了如下修改：

- 固定了 `SENTRY_SECRET_KEY`
- 关闭了用户注册功能
- 邮件发送相关设置修改


## 升级步骤

```
# 更新上游代码
git pull https://github.com/getsentry/onpremise.git master

# 更新镜像
docker-compose build

# 执行 sentry 的升级命令
docker-compose run --rm base sentry upgrade

# 更新容器
docker-compose up -d

# 最后整理一下变化，提交到 https://github.com/Datartisan/onpremise.git
```
