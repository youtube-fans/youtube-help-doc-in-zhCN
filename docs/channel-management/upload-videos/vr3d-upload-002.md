# 上传虚拟实境视频

虚拟实境 (VR) 视频是一种全新的视频类型，可以带给您如临其境的观看体验。虚拟实境视频巧妙利用了人眼在看物体时的习惯或特点，可以在各个方向展现出深度效果，使近景和远景层次分明。

要充分感受 VR 视频的效果，我们建议您通过 [Daydream View](https://vr.google.com/daydream/smartphonevr/)（在[支持的手机](https://vr.google.com/daydream/smartphonevr/phones/)上）、[Google Cardboard](https://vr.google.com/cardboard/get-cardboard/) 或 PlayStation VR 观看。如果您使用的是上述设备，请确保您已安装最新版本的 YouTube 应用。

如果没有虚拟实境观看设备，您仍然可以在移动设备或计算机上使用 Chrome、Opera 或 Firefox 浏览器观看这些视频。在这种情况下，这类视频会显示为非 3D 格式的 360 度全景视频。

第 1 步：制作视频

VR 视频有两种形式：使用摄像机拍摄的真实场景（例如使用 [Jump](https://www.google.com/get/cardboard/jump/) 平台），以及可根据我们的指南（[下载 PDF](https://developers.google.com/cardboard/jump/rendering-ods-content.pdf) - 英文版）制作的计算机生成 (CG) 内容。

第 2 步：准备上传

上传之前，我们建议您以 1:1 的宽高比导出上下排列、等距柱状投影格式的内容。我们还建议采用 5120x5120 或更高（最高 8192x8192）的分辨率。请保持像素形状为正方形（即 1:1 像素/比例的宽高比）。请勿添加左右黑边，并且所有像素均应使用。生成的图像应以横向拉伸形式显示。

**提示** ：如果视频出现明显的压缩失真，可以尝试以较高的比特率（例如 150 Mbps）重新对其进行编码，然后再上传至 YouTube。

您的视频文件必须包含特定元数据。这样做可帮助 YouTube 将视频识别为 VR 视频，并开启恰当的播放模式。请按以下说明操作，将必要的元数据添加至新文件。

#### 通过应用制作 360 度全景视频文件

1. 下载最新的 [360 度全景视频元数据应用](https://github.com/google/spatial-media/releases/latest)。
2. 将下载的文件解压缩，然后打开 360 度全景视频元数据应用。如果您使用的是 Apple 计算机，则可能需要右键点击该应用，然后点击 **打开** 。
3. 选择视频文件。
4. 同时选中两个复选框，然后点击 **保存** 。
5. 为即将创建的文件输入名称。
6. 保存文件；新文件将自动创建并保存在与源文件相同的位置。
7. 将新文件上传至 YouTube。
8. 等待视频处理完毕，此过程最多可能需要一个小时。在此期间，视频可能无法正确呈现。

## 向 YouTube 上传 VR 视频时建议遵循的规范

向 YouTube 上传上下排列格式的 360 度全景视频时，建议遵循以下 Jump 规范：

* **分辨率** ：5120 x 5120，最高 8192 x 8192（如果画质低于 5K，可使用尽可能高的分辨率）
* **帧速率** ：25、29.97、50、59.94
* **格式** ：MP4、MOV
* **编解码器** ：H.264、ProRes、DNxHR
* **H.264 比特率** ：150 - 360Mbps
* **音频** ：AAC（请参阅 [YouTube 空间音频使用要求](https://support.google.com/youtube/answer/6395969?hl=en)了解空间音频）
* **Moov Atom** ：文件以 Moov Atom 开头

了解如何使用[空间音频](https://support.google.com/youtube/answer/6395969)、[360 度视频](https://support.google.com/youtube/answer/6178631)和[虚拟实境视频](https://support.google.com/youtube/answer/6316263)，以便让观看者在观看视频时体验到逼真的全方位环绕音效。