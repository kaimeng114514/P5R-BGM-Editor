# P5R-BGM-Editor 女神异闻录5皇家版 音乐替换工具
一键替换《女神异闻录5 皇家版》(P5R) 游戏背景音乐（BGM）的工具，并自动生成 Reloaded-II Mod。
 
核心功能
 
- 自动解包：选择 BASE.CPK 所在文件夹，自动提取游戏全部 BGM（其他 CPK 不受影响）
- 曲目识别：自动匹配每首 BGM 的歌曲名（基于 amicitia 社区曲目库）
- 试听预览：内置播放器，支持进度条拖拽、暂停/停止，播放完毕自动停止
- 一键替换：导入 MP3/WAV/OGG 等格式，自动完成 转WAV → ADX编码 → P5R加密 全流程
- 原曲导出：可将任意原曲解密导出为 WAV 素材
- 状态持久化：替换记录自动保存，重启软件自动恢复
- Mod 导出：自定义名称/简介，生成标准 Reloaded-II Mod
 
运行环境：Windows + Python 3.10+，需安装 pythonnet / pygame / Pillow
 
致谢：基于 P5R Modding 社区研究成果开发
