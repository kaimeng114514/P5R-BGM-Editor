P5R BGM Editor
 
女神异闻录5皇家版（Persona 5 Royal）音频替换工具
 
一键导入、识别、试听并替换游戏的 BGM / 音效 / 角色语音 三类音频，自动完成 ADX 编码、P5R 加密与多维音频对齐，生成 Reloaded-II（FEmulator + Ryo Framework）兼容 Mod。
 
 
 
功能特性
 
- 三类音频支持
BGM（主 BGM + 额外 BGM）、音效（E*SE / SYSTEM / TITLE 等）、角色语音（BP01~BP10 / VOICE* / EVENT 等）
​
- 一键替换
任意格式（MP3 / WAV / OGG / FLAC / M4A）→ 转 WAV → ADX 编码 → P5R 加密 → 多维对齐 → 生成 Mod
​
- 9 项音频对齐（解决替换后"声音炸"）
等长匹配 · 响度匹配(RMS) · 频谱对齐 · 带宽对齐 · 底噪对齐 · 立体声宽度 · 包络对齐 · 感知响度(LUFS) · 动态限幅
​
- Ryo Framework 播放层控音量
集成 Ryo（volume=0.5），彻底解决游戏内音量被自动放大的问题（P5R 存在硬编码通道增益）
​
- 角色语音替换
走 Ryo 路径，可完整播放超长音频，不受原时长限制，无需强制等长
​
- 批量替换
支持范围批量替换（如  232000-232003 ），自动补齐全部 Ryo Cue
​
- AI 语音识别 + 翻译
Whisper 微调模型（日文识别）+ NLLB-200（日中翻译），台词自动标注与校准映射随工具发布
​
- 试听预览 / 原曲导出 / 状态持久化 / 重复音效折叠
内置播放器、原曲解密导出 WAV、替换记录自动保存恢复、相同音频自动分组
​
- 工具完整性管理
自动校验 / 备份 / 恢复 tools 目录
 
 
 
系统要求
 
- Windows 10/11
​
- Python 3.8+（源码版）
​
- Reloaded-II + P5R Essentials + CRI FileSystem V2 Hook
​
- Ryo Framework（非流式音频 / 角色语音替换）
 
快速开始
 
1. 双击根目录  启动.bat 
​
2. 文件 → 导入 BASE.CPK 所在文件夹（自动解包识别三类音频）
​
3. 顶部切换「BGM / 音效 / 角色语音」→ 选择曲目 →「选择音乐文件」
​
4. 调整高级选项（对齐 / 循环点 / Ryo 音量 / 批量范围）→「执行替换」
​
5. 替换多首后「导出 Mod」→ 放入 Reloaded-II Mods 目录并启用
 
 
 
技术原理
用户音频(MP3/OGG/etc.)
   → WAV → 多维对齐(等长/响度/频谱/带宽/底噪/立体声/包络/LUFS/动态)
   → VGAudioCli 编码(GcAdpcm, ADX v4) → 加密(keycode 9923540143823782 + 偏移19=0x09)
   → P5R 兼容加密 ADX
   ├─ 流式(BGM/音效) → FEmulator/AWB/
   └─ 非流式(TITLE/语音) → Ryo Framework(volume=0.5)
致谢
 
本工具使用并致敬以下开源项目（工具内 作者 → 参考工具 可点击跳转）：
VGAudio (Thealexbarney) · vgmstream (bnnm) · FFmpeg · CriFsV2Lib / CriPakTools (Sewer56 / esperknight) · Atlus-Script-Tools (tge-was-taken) · PersonaVCE (ShrineFox) · Reloaded-II / FileEmulationFramework (Sewer56) · Ryo Framework (RyoTune) · faster-whisper (SYSTRAN) · Whisper (OpenAI) · ctranslate2 (OpenNMT) · NLLB (Meta AI) 等
 
免责声明
 
本工具仅供学习和个人使用，请尊重游戏版权，勿将替换后的音频用于商业用途或非法分发。