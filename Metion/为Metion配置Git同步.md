---
title: 为Metion配置Git同步
date: 2023-03-11 15:19
---
Metion 是一款写作 APP，我之前一直将其当作写作入口来写博客。现在我开启了 TIL（Today I Learned）项目，自然也想使用它。因为Metion 支持 iOS 端、iPad 端及 Mac 端，写起笔记来很是方便，
但也涉及到同步问题，可以使用 iCloud，但其并不稳定。我本来就将 TIL 项目放在 GitHub 上，所以最好是使用 Git。幸好， Metion 支持 Git。
在配置 Git 过程中，我遇到了一个错误： `You're using an RSA key with SHA-1, which is no longer allowed. Please use a newer client or a different key type.`
这是因为 GitHub 已不再支持 SHA-1 的加密方式。为了解决这个问题，需要将加密方式改为`ECDSA`，按如下命令重新生成密钥对即可：
```bash
ssh-keygen -t ecdsa -b 521
```
这将在`~/.ssh/`目录下生成私钥`id_ecdsa`与公钥`id_ecdsa.pub`。然后，将私钥添加到 Metion 中，将公钥添加到 GitHub 中，就可以在 Metion 中写作，然后利用 Git 同步到 GitHub 对应仓库中了。