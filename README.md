# 网易云音乐 NCM 格式转换器

NetEase Cloud Music NCM Format Converter

Windows 桌面批量处理工具。程序会检测 NCM 内部的真实音频编码，再按所选模式进行保真处理。所有转换均在本地完成，不会上传音频。

## 下载

最新版：[v1.3.0 Release](https://github.com/Dave-ZehaoXie/--NCM-/releases/tag/v1.3.0)

下载 `NCM格式批量转换器-v1.3.0.exe` 后，请使用仓库中的 `SHA256SUMS.txt` 核对文件完整性。

| 版本 | 主要更新 |
| --- | --- |
| [v1.3.0](https://github.com/Dave-ZehaoXie/--NCM-/releases/tag/v1.3.0) | 保留 NCM 原封面；修复裸 AAC、覆盖、取消和报告边缘问题 |
| [v1.2.0](https://github.com/Dave-ZehaoXie/--NCM-/releases/tag/v1.2.0) | 新增智能无损模式：普通音乐输出 FLAC，Atmos 保留 M4A |
| [v1.1.1](https://github.com/Dave-ZehaoXie/--NCM-/releases/tag/v1.1.1) | 修复批量转换音质标签错误 |
| [v1.1.0](https://github.com/Dave-ZehaoXie/--NCM-/releases/tag/v1.1.0) | 检测真实编码，新增保持原格式和保真 WAV |

## 使用方法

1. 运行 `NCM格式批量转换器-v1.3.0.exe`。
2. 添加一个或多个 NCM 文件，也可以添加整个文件夹。
3. 选择输出模式、输出目录和同名文件处理方式。
4. 点击“开始处理”。

默认的“智能无损（推荐）”模式会：

- 真 FLAC：原样导出 FLAC，不重新编码。
- 普通 MP3/AAC：转换为 FLAC；转换过程使用无损编码，但不能恢复源文件此前已经损失的音质。
- Atmos/E-AC-3：保持原始 M4A，不改变空间音频码流。

## 封面处理

- FLAC、MP3、M4A、OGG/Opus：封面直接内嵌到音频文件。
- WAV、裸 AAC/E-AC-3：在音频旁生成同名 `.cover.jpg` 或 `.cover.png`。
- 源 NCM 没有封面：音频仍会正常输出，报告中会标记“源文件无封面”。

每次处理都会生成 `NCM转换报告.csv`，记录状态、真实编码、采样率、声道、样本格式、处理方式和封面处理结果。

## 安全与使用范围

- 程序完全在本地运行，不上传音频。
- FFmpeg 已内置，无需另行安装。
- 本仓库仅发布 Windows EXE、使用说明和 SHA-256 校验值，不公开转换源码。
- 请仅处理你依法取得并有权转换的文件。本工具不包含或提供任何音乐内容。

## English

This Windows desktop tool batch-processes NCM files, detects the real embedded audio codec, and chooses a fidelity-preserving output path. All processing is local; no audio is uploaded.

The recommended Smart Lossless mode exports true FLAC without re-encoding, converts ordinary MP3/AAC sources to FLAC without claiming to restore lost quality, and preserves Atmos/E-AC-3 in its original M4A container. Version 1.3.0 also preserves the original NCM cover art.

Only process files that you legally own or are authorized to convert. This repository distributes only the Windows executable, documentation, and SHA-256 checksums; it does not include music content.

## SHA-256

See `SHA256SUMS.txt` for the complete checksum list.
