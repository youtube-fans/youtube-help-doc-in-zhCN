# 嵌入视频和播放列表

您可以通过嵌入的方式将 YouTube 视频或播放列表加入到网站或博客中。

[
Embed videos and playlists
](https://www.youtube.com/watch?v=lJIrF4YjHfQ)

订阅我们的 [YouTube 帮助](https://www.youtube.com/user/youtubehelp?sub_confirmation=1)频道，了解最新动态和提示并获取帮助。

## 嵌入视频

1. 在计算机上，找到想要嵌入的 YouTube 视频。
2. 在视频下方，点击 **分享**  ![分享](https://storage.cloud.google.com/support-kms-prod/dJviTGFzvddvW4FXLvi4NS4ZrkJKjtwkqxyn "分享")。
3. 点击 **嵌入** 。
4. 复制出现的方框中的 HTML 代码。
5. 将该代码粘贴到您的博客或网站 HTML 中。

如果您要在您面向儿童的网站或应用中嵌入 YouTube 视频，您必须使用[这些工具](https://support.google.com/policies/answer/9664901)自行标识您的网站和应用。您进行自行标识后，Google 就不会在这些网站或应用中投放个性化广告，并会停用嵌入式播放器中的部分功能。

在此提醒您，在访问和使用 YouTube 嵌入式播放器时，需遵守 [YouTube API 服务条款](https://developers.google.com/youtube/terms/api-services-terms-of-service)和[开发者政策](https://developers.google.com/youtube/terms/developer-policies)。

## 嵌入播放列表

1. 在计算机上登录 YouTube 帐号。
2. 在页面的左侧，选择您想要嵌入的播放列表。
3. 从相应网址上复制播放列表 ID。
4. 执行以下操作，修改某个视频的嵌入代码：
  * 将视频 ID（在“embed/”之后）替换为“videoseries?list=”。
  * 将播放列表 ID 粘贴到“=”后面。
  * 将该代码粘贴到您的博客或网站 HTML 中。

**示例：**

* <iframe width="560" height="315" src="https://www.youtube.com/embed/videoseries?list=PLx0sYbCqOb8TBPRdmBHs5Iftvv9TPboYG" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## 管理视频嵌入选项

启用隐私权保护增强模式

在隐私权保护增强模式下，您可以嵌入 YouTube 视频，而不使用 Cookie 跟踪观看行为。这意味着系统不会收集相关活动数据来提供个性化观看体验。系统会改为推荐与当前视频内容相关的视频。在隐私权保护增强模式下播放视频不会影响观看者在 YouTube 上的浏览体验。

请注意，此模式仅适用于网站上的嵌入式播放器。要在应用中使用隐私权保护增强模式，开发者需要使用网站视图实例。

在此提醒您，在访问和使用 YouTube 嵌入式播放器时，需遵守 [YouTube API 服务条款](https://developers.google.com/youtube/terms/api-services-terms-of-service)和[开发者政策](https://developers.google.com/youtube/terms/developer-policies)。

**注意：**

* 如果观看者点击或点按退出嵌入式播放器并被重定向到其他网站或应用，那么该网站或应用可能会根据自身的政策和条款来跟踪观看者的行为。
* 隐私权保护增强模式目前仅适用于网站上的嵌入式播放器。要在应用中使用，开发者必须将启用了隐私权保护增强模式的播放器封装到网站视图实例中。

要使用隐私权保护增强模式，请在 HTML 中将嵌入网址的网域从 https://www.youtube.com 更改为 https://www.youtube-nocookie.com，如下面的示例所示：

**更改前**
<iframe width="1440" height="762"
src="https://www.youtube.com/embed/7cjVj1ZyzyE"
frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

**更改后**
<iframe width="1440" height="762" src="https://www.youtube-nocookie.com/embed/7cjVj1ZyzyE"
frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

由于网域发生了变化，因此除了 youtube.com 之外，网络管理员还需要将网域 youtube-nocookie.com 添加到自己的防火墙白名单中。

使嵌入的视频自动播放

要使嵌入的视频自动播放，请在视频的嵌入代码中加入“ **&autoplay=1** ”，使其紧跟在视频 ID（“embed/”后面的一系列字母）后面。

自动播放的嵌入视频不会增加视频的观看次数。

**示例：**

> <iframe width="560" height="315" src="https://www.youtube.com/embed/D6Ac5JpCHmI? **&autoplay=1** "frameborder="0"  allowfullscreen></iframe>

让嵌入的视频从特定时间点开始播放

要让视频从特定时间点开始播放，可在视频的嵌入代码中加入  **?start=** ，后跟要让视频开始播放的时间点（以秒表示）。

例如，如果您想要视频从 1 分 30 秒处开始播放，那么嵌入代码就该如下所示：

> <iframe allowfullscreen="" frameborder="0" height="315" src="http://www.youtube.com/embed/UkWd0azv3fQ **?star** *t=90* " width="420"></iframe>

为嵌入的视频添加字幕

在视频的嵌入代码中加上“ **&cc_load_policy=1** ”，即可让嵌入的视频自动显示字幕。

您还可以为嵌入的视频选择字幕语言。为此，只需在视频的嵌入代码中加上“ **&cc_lang_pref=fr&cc_load_policy=1** ”即可。

* “cc_lang_pref”可设置视频中显示的字幕语言。
* “cc_load_policy = 1”可默认打开字幕。
* “fr”代表法语的语言代码。您可以在 [ISO 639-1 标准](http://www.loc.gov/standards/iso639-2/php/code_list.php)中查询各种语言的双字母语言代码。

关闭视频嵌入功能

**注意** ：如果您现在使用的是 [YouTube 工作室测试版](https://studio.youtube.com/)，请选择左侧菜单中的创作者工作室传统版并按相关步骤操作。

如果您不想让其他人将您上传的视频嵌入到外部网站，请按照下列步骤操作：

1. 访问[视频管理器](http://www.youtube.com/my_videos)。
2. 找到要关闭嵌入功能的视频，然后点击 **修改** 。
3. 在视频下方，点击 **高级设置** 。
4. 在“分发选项”下，取消选中 **允许嵌入** 复选框。