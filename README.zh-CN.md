# TC4R 资源包创作示例

[English](README.md) · 简体中文

**本示例资源包独立发布，与 TC4R 本体项目无关，仅作资源包创作学习参考。素材权利归各自权利人所有；如有侵权，请在示例仓库提交 Issue 联系删除（侵删）。本说明不改变素材原有的授权条件。**

用于学习 Minecraft 资源包目录、模型与贴图引用、语言文件和声音定义的组织方式。资源包独立保存在本仓库的 Release 中。

## 对应版本

本批示例适配 [TC4R 1.0.1](https://github.com/Aya-Net/tc4r-release/releases/tag/v1.0.1)；请选择完全对应的 Minecraft 与加载器版本。下载：[示例资源包 v1.0.1](https://github.com/Aya-Net/tc4r-resourcepack-example/releases/tag/v1.0.1)。

| Minecraft | 加载器 | TC4R 版本 | 示例资源包 |
| --- | --- | --- | --- |
| 1.20.1 | Forge | 1.0.1 | [tc4r-1.20.1-forge-1.0.1-example-resources.zip](https://github.com/Aya-Net/tc4r-resourcepack-example/releases/download/v1.0.1/tc4r-1.20.1-forge-1.0.1-example-resources.zip) |
| 1.21.1 | NeoForge | 1.0.1 | [tc4r-1.21.1-neoforge-1.0.1-example-resources.zip](https://github.com/Aya-Net/tc4r-resourcepack-example/releases/download/v1.0.1/tc4r-1.21.1-neoforge-1.0.1-example-resources.zip) |

## 使用方式

将对应 ZIP 保持压缩状态，放入实例的 `resourcepacks` 文件夹，然后在游戏的资源包菜单启用。它使用 `tc4r` 命名空间，不是放入 `mods` 的运行模组，也不是服务端数据包。

## 精确适配的运行包

请以以下运行 JAR 的 SHA-256 精确匹配本批示例。

| Runtime JAR / 运行包 | SHA-256 |
| --- | --- |
| `tc4r-1.20.1-forge-1.0.1.jar` | `61bfaeced3e96656d567583a5e43c91280d84949f319742cf73f4e5504c375b8` |
| `tc4r-1.21.1-neoforge-1.0.1.jar` | `ca70722d8d76d78602886e179eefc532111f57ad300d6a4e7976dec0ec78bae5` |

## 素材与移除请求

保留资源包内的 `NOTICE-EXAMPLE-RESOURCES.txt` 和已有权利声明。本仓库不对第三方素材授予新的许可。权利人如需移除相关内容，请通过本仓库 [Issues](https://github.com/Aya-Net/tc4r-resourcepack-example/issues) 提供涉及的文件和说明。

## 完整性验证

每个 ZIP 均附 RSA-3072 / SHA-256 数字签名。它可以检出文件改动；不会加密或锁定素材，Minecraft 也不会自动验签。

从本仓库获取可信公钥，并从对应 Release 下载 ZIP 及同名 `.zip.sig`，置于同一目录。安装 OpenSSL 后执行对应命令：

```sh
openssl dgst -sha256 -verify TC4R-EXAMPLE-PUBLIC-KEY.pem -signature tc4r-1.20.1-forge-1.0.1-example-resources.zip.sig tc4r-1.20.1-forge-1.0.1-example-resources.zip
openssl dgst -sha256 -verify TC4R-EXAMPLE-PUBLIC-KEY.pem -signature tc4r-1.21.1-neoforge-1.0.1-example-resources.zip.sig tc4r-1.21.1-neoforge-1.0.1-example-resources.zip
```

公钥：[TC4R-EXAMPLE-PUBLIC-KEY.pem](TC4R-EXAMPLE-PUBLIC-KEY.pem)

公钥文件 SHA-256：`c5340a50ddea2571de955cefdbcc28aa2f84e6bc9c924320359e906e7df5a9e0`

公钥须来自可信的仓库页面；请勿直接信任与可疑 ZIP 一同提供的替换公钥。

[OpenSSL 验签说明](https://docs.openssl.org/3.0/man1/openssl-dgst/)
