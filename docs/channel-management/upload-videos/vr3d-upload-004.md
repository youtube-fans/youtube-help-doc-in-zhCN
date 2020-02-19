# 在 360 度全景视频和虚拟现实 (VR) 视频中使用空间音频

通过 YouTube 空间音频，您在观看视频时可以体验到逼真的全方位环绕音效。借助此功能，您可以进一步提升 360 度全景视频和虚拟实境视频的效果，让观看者获得身临其境的感觉。了解如何向 YouTube [上传 360 度全景视频](https://support.google.com/youtube/answer/6178631)和[虚拟实境视频](https://support.google.com/youtube/answer/6316263)。

## 上传含空间音频的视频

1. 按照以下要求制作含空间音频的 360 度全景视频或虚拟实境视频。
2. 针对视频运行最新版本的[元数据工具](https://github.com/google/spatial-media/releases/latest)。
3. 将视频上传到 YouTube。

#### 预先体验 VR 视频中的空间音频

要在上传 VR 视频之前预先体验 VR 视频中的空间音频，您可以使用 [Resonance Audio Monitor VST 插件](https://developers.google.com/resonance-audio/develop/vst-monitor/getting-started)。该插件可与任何能够呈现 4-6 声道音频文件并托管 VST 插件的数字音频工作站配合使用。

## 支持的空间音频格式

YouTube 支持两种不同的空间音频格式：

* 一阶环绕声
* 具有头部锁定立体声的一阶环绕声。

借助空间音频，如果观看者在观看 360 度全景视频或虚拟实境视频时转动头部，看向四周，则声音的位置会随之而变。这种音频格式称为 **一阶环绕声** 。您还可以在视频中添加头部锁定立体声。使用这种音频格式时，声音的位置不会随着观看者转动头部而发生改变。 **头部锁定立体声** 音轨通常用于解说类节目或背景音乐。

## 聆听体验因设备而异

观看者可以在所有设备上尽情体验 **一阶环绕声** 音频，使用移动设备或 Chrome/Firefox/Opera 网络浏览器则还能畅享 **具有头部锁定立体声的一阶环绕声** 音频。对于使用其他网络浏览器的观看者，我们会自动缩混音频的头部锁定部分，但声音效果可能不太一样。

## 各个设备的详细信息

YouTube 会根据所使用的设备以不同的方式处理空间音频。

**设备** **行为**
移动应用 YouTube 会使用头部相关传输函数 (HRTF) 将环绕声音轨解码为双耳立体声
桌面设备 Chrome、Opera 和 Firefox YouTube 会使用 Mid-Side（中间/两边）立体声技术将环绕声音轨解码为双耳立体声
其他浏览器 YouTube 会将音轨中的头部锁定立体声缩混到一阶环绕声的全向组分 (W) 中

## 技术要求

您可以查看完整的 [YouTube 空间音频规范](https://github.com/google/spatial-media/blob/master/docs/spatial-audio-rfc.md)，了解所有受支持的布局和阶数。请确保在使用空间音频时一定要满足以下这些最低要求：

## 使用空间音频的最低要求

1. **在您的文件中添加元数据。**
  * **​​** 可以使用[元数据工具](https://github.com/google/spatial-media/releases/latest)，也可以使用您自己的后期制作工具添加，只要其符合 [YouTube 规范](https://github.com/google/spatial-media/blob/master/docs/spatial-audio-rfc.md)
2. **只使用一个音轨。**
  * **​​** 不支持使用多音轨（如在一个文件中同时使用空间音轨和立体声/单声道音轨）。
3. **空间音频使用环绕声 (AmbiX) 格式：**
  * ACN 声道阶
  * SN3D 规范化
4. **支持的一阶环绕声 (FOA) 格式：**
  * **​​** 按 W、Y、Z、X 的顺序排列，并作为您的上传文件的 4 声道音轨，采样率：48 kHz
  * MOV 容器里的  **PCM**  编码音频：
  * MP4/MOV 容器里的  **AAC**  编码音频：
    * 最小比特率：256 kbps
  * MP4 容器里的  **OPUS**  编码音频：
    * 最小比特率：512 kbps
    * 声道映射组合：2
5. **支持的具有头部锁定立体声的一阶环绕声 (FOA) 格式：**
  * 按 W、Y、Z、X、L、R 的顺序排列，并作为您的上传文件的 6 声道音轨，采样率：48 kHz
  * MOV 容器里的  **PCM**  编码音频：
    * 采样率：48 kHz
  * MP4 容器里的  **OPUS**  编码音频：
    * 最小比特率：768 kbps
    * 声道映射组合：2