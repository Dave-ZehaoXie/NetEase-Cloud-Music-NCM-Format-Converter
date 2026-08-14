# 网易云音乐 NCM 格式转换器

**批量处理 NCM，优先保持内部真实音频格式，不把有损音频伪装成无损。**

## 下载

前往 [Releases](../../releases) 下载最新版：

- **v1.1.0：** `NCM格式批量转换器-v1.1.0.exe`
- 建议下载后按仓库中的 `SHA256SUMS.txt` 校验文件完整性

## 中文说明

这是一个 Windows 桌面批量处理工具。程序会先解开 NCM 并检测内部真实编码，再根据所选模式输出。

### 推荐用法

1. 从 Releases 下载并运行 `NCM格式批量转换器-v1.1.0.exe`。
2. 添加一个或多个 NCM 文件，也可以添加整个文件夹。
3. 优先选择 **“保持原始格式（推荐）”**。
4. 选择输出目录和同名文件处理方式，点击“开始转换”。

### v1.1.0 音质策略

- **FLAC 源：** 原样导出 FLAC，不重新编码。
- **MP3 / AAC / M4A / Atmos 源：** 默认保持原编码和容器，避免无意义转码。
- **保真 WAV：** 有损或浮点解码源使用 32-bit float WAV，保留超过 0 dBFS 的峰值，避免整数削波。
- **多声道：** 5.1 / Atmos 转 WAV 时保留原声道，不自动下混成立体声。
- **强制 FLAC：** 有损源转 FLAC 不会恢复已损失的音质，程序会明确提示。

每次处理都会生成 `NCM转换报告.csv`，记录真实编码、采样率、声道、样本格式和处理方式。

程序完全在本地运行，不会上传音频。FFmpeg 已内置，无需额外安装。

> 请仅处理你依法取得并有权转换的文件。本工具不包含或提供任何音乐内容。

---

# NetEase Cloud Music NCM Format Converter

**Batch-process NCM files while preserving the real embedded codec whenever possible.**

## English

This Windows desktop tool decrypts each NCM file, detects its real embedded audio codec, and selects a fidelity-preserving output path.

### Recommended workflow

1. Download and run `NCM格式批量转换器-v1.1.0.exe` from Releases.
2. Add NCM files or a complete folder.
3. Choose **Keep Original Format (Recommended)**.
4. Select the output directory and duplicate-file policy, then start conversion.

### Fidelity behavior in v1.1.0

- FLAC sources are exported directly without re-encoding.
- MP3, AAC/M4A, and Atmos sources keep their original codec/container by default.
- Fidelity WAV uses 32-bit float for lossy or floating-point decoder sources to avoid integer peak clipping.
- 5.1/Atmos sources remain multichannel; no automatic stereo downmix is applied.
- Forced FLAC conversion warns that transcoding lossy audio cannot restore lost quality.
- Each run creates `NCM转换报告.csv` with codec and processing details.

All processing is local. No audio is uploaded. FFmpeg is bundled.

> Only process files that you legally own or are authorized to convert. This tool does not include or distribute music.

## SHA-256

Verify the downloaded executable using `SHA256SUMS.txt`.
