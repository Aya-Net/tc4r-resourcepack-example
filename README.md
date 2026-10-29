# TC4R Resource-Pack Authoring Example

English · [简体中文](README.zh-CN.md)

**This resource pack is an independent learning example, separate from and not part of the TC4R core project. It is provided solely for studying resource-pack creation. Materials remain the property of their respective rights holders; please open an issue in the example repository to request removal of infringing material. Existing permissions remain applicable.**

An example for studying Minecraft resource-pack layout, model and texture references, language files, and sound definitions. The resource packs are distributed separately through this repository’s Releases.

## Compatible versions

This batch targets [TC4R 1.0](https://github.com/Aya-Net/tc4r-release/releases/tag/v1.0). Select the exact matching Minecraft version and loader. Download: [example resource packs v1.0](https://github.com/Aya-Net/tc4r-resourcepack-example/releases/tag/v1.0).

| Minecraft | Loader | TC4R version | Example resource pack |
| --- | --- | --- | --- |
| 1.20.1 | Forge | 1.0 | [tc4r-1.20.1-forge-1.0-example-resources.zip](https://github.com/Aya-Net/tc4r-resourcepack-example/releases/download/v1.0/tc4r-1.20.1-forge-1.0-example-resources.zip) |
| 1.21.1 | NeoForge | 1.0 | [tc4r-1.21.1-neoforge-1.0-example-resources.zip](https://github.com/Aya-Net/tc4r-resourcepack-example/releases/download/v1.0/tc4r-1.21.1-neoforge-1.0-example-resources.zip) |

## Usage

Place the matching ZIP, still compressed, in the instance’s `resourcepacks` folder and enable it in the game’s resource-pack menu. It uses the `tc4r` namespace. It is a resource pack, not a runtime mod for `mods` or a server data pack.

## Exact matching runtime files

Earlier files may share the 1.0 version number. Match the runtime JAR SHA-256 below:

| Runtime JAR / 运行包 | SHA-256 |
| --- | --- |
| `tc4r-1.20.1-forge-1.0.jar` | `0316787169a40065cfacdc186d54f5eccfa4e8428232dec97bdc80ab2e9c46d4` |
| `tc4r-1.21.1-neoforge-1.0.jar` | `85d299e9ad4fa9494680e75e6322fe595a4d45e14b19a1d572b0af9d6b7d520e` |

## Materials and removal requests

Preserve `NOTICE-EXAMPLE-RESOURCES.txt` and existing rights notices inside the packs. This repository grants no new permission over third-party materials. Rights holders may use this repository’s [Issues](https://github.com/Aya-Net/tc4r-resourcepack-example/issues) to identify affected files and request their removal.

## Integrity verification

Each ZIP has a detached RSA-3072 / SHA-256 signature to detect file changes. This does not encrypt or lock assets; Minecraft does not verify these signatures automatically.

Obtain the trusted public key from this repository, then download the ZIP and its matching `.zip.sig` from the release into the same folder. With OpenSSL installed, run the matching command:

```sh
openssl dgst -sha256 -verify TC4R-EXAMPLE-PUBLIC-KEY.pem -signature tc4r-1.20.1-forge-1.0-example-resources.zip.sig tc4r-1.20.1-forge-1.0-example-resources.zip
openssl dgst -sha256 -verify TC4R-EXAMPLE-PUBLIC-KEY.pem -signature tc4r-1.21.1-neoforge-1.0-example-resources.zip.sig tc4r-1.21.1-neoforge-1.0-example-resources.zip
```

Public key: [TC4R-EXAMPLE-PUBLIC-KEY.pem](TC4R-EXAMPLE-PUBLIC-KEY.pem)

Public-key file SHA-256: `c5340a50ddea2571de955cefdbcc28aa2f84e6bc9c924320359e906e7df5a9e0`

Trust the key obtained from the repository; do not trust a replacement key supplied with a suspect ZIP.

[OpenSSL signature verification](https://docs.openssl.org/3.0/man1/openssl-dgst/)
