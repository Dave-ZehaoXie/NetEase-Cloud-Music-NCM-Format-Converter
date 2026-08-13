# 网易云音乐 NCM 格式转换器

## 中文说明

Windows 桌面批量转换工具，可将网易云音乐 .ncm 文件转换为 FLAC 或 WAV。

### 使用方法

1. 从 Releases 下载并运行 NCM无损批量转换器.exe。
2. 添加一个或多个 NCM 文件，也可以添加整个文件夹。
3. 选择 FLAC 或 WAV、输出目录以及同名文件处理方式。
4. 点击“开始转换”。

程序完全在本地运行，不会上传音频。FFmpeg 已内置，无需额外安装。源音频若为 FLAC，导出 FLAC 时会直接解密，不重新编码。若 NCM 内部原本是 MP3 或 AAC，转换为 FLAC/WAV 不会恢复已经损失的音质。

请仅处理你依法取得并有权转换的文件。本工具不包含或提供任何音乐内容。

---

# NetEase Cloud Music NCM Format Converter

A Windows batch conversion tool for converting NetEase Cloud Music .ncm files to FLAC or WAV.

### Usage

1. Download NCM无损批量转换器.exe from Releases and run it.
2. Add one or more NCM files, or add a complete folder.
3. Select FLAC or WAV, an output directory, and a duplicate-file policy.
4. Click Start Conversion.

All processing is performed locally. No audio is uploaded. FFmpeg is included. Converting a lossy MP3/AAC source to FLAC or WAV cannot restore lost audio quality.

Only process files that you legally own or are authorized to convert. This tool does not include or distribute music.

## SHA-256

See SHA256SUMS.txt and verify the downloaded executable before running it.
