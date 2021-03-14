# 有道云笔记签到🌹

一点小羊毛。**好哥哥们顺手点个 star 吧。**

通过 github action 来实现自动签到（每天签到可以获得存储空间奖励）。

## 步骤

### 1 fork 这个仓库

点击右上角的 fork。

### 2 设置用户名（USERNAME）和密码（PASSWORD）

在 fork 后**自己的**仓库中依次点击 `Settings` - `Secrets` - `New repository secret`，如下图所示：

![image-20210111220035535](README.assets/image-20210111220035535.png)

然后添加 2 个 secret，分别为 `USERNAME` 和 `PASSWORD`。

`USERNAME` 就是签到账号，示例：

```text
150********@163.com
```

`PASSWORD` 是密码，示例：

```text
123456
```

### 3 运行

随便发起一个 push 请求，可以修改一下 `README.md`，或者自己给自己点个 star，就可以开始。之后就会每隔 6 小时进行一次签到（因为有时候签到会失败，好像是服务器不太好，就设置一下每小时签到一次保证成功吧）。

注意，在官方文档中有这么一段：

> To prevent unnecessary workflow runs, scheduled workflows may be disabled automatically. When a public repository is forked, scheduled workflows are disabled by default. In a public repository, scheduled workflows are automatically disabled when no repository activity has occurred in 60 days.

也就是说，**定时执行的任务需要每隔 60 天激活一次**。

