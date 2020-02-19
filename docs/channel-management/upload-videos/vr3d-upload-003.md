# 上传 3D 视频

您可以上传和播放以下形式的 3D 视频：矩形 3D 视频或 360 度 3D 全景视频（虚拟实境视频）。本文说明了上传 3D 矩形视频所需的元数据。如需了解如何上传 360 度 3D 全景视频，请使用有关[上传虚拟实境视频](https://support.google.com/youtube/answer/6316263)的说明。请确保您的 3D 视频文件包含必需的 3D 元数据。

YouTube 支持从左到右 (LR) 并排立体布局的 3D 视频。视频应包含以下立体元数据：

* .mov/.mp4 视频应包含的[立体 3D 视频](https://github.com/google/spatial-media/blob/master/docs/spherical-video-v2-rfc.md#stereoscopic-3d-video-box-st3d)框 (st3d)，
* .mkv/.webm 视频应包含的设置为从左到右并排的 StereoMode 元素，或
* H264 补充增强信息 (SEI) 标头中的 FPA 元数据

**注意** ：如果您的 3D 视频没有 3D 元数据，您可以使用您偏好的视频编辑软件（Sony Vegas Pro 或 GoPro Studio 等）或 [FFmpeg 工具](https://ffmpeg.org/)添加此类元数据。

**采用 .mov 或 .mp4 容器的 H.264 编码视频**

`ffmpeg -i input_file.mkv -vcodec libx264 -x264opts \    "frame-packing=3:frame-packing-interpret=1:frame-packing-quincunx=0:frame-packing-grid=0,0,0,0" output_file.mp4`

**Matroska 和 WebM 视频**

`ffmpeg -i input_file.mkv -c copy -metadata:s:v:0 stereo_mode=1 output_file.mkv`