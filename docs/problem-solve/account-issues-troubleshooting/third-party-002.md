# 第三方应用身份验证问题

YouTube 已将 YouTube Data API 服务从 v2 升级到 v3，这项更新的技术能实现第三方应用与 YouTube 的整合。早在 2014 年，我们便向第三方应用开发者[告知了这项更改](https://youtube-eng.googleblog.com/2014/09/have-you-migrated-to-data-api-v3-yet.html)，让他们有足够的时间来采用我们的新技术。自那时起，我们一直致力于协助他们迁移至我们所支持的更新技术。

大多数第三方应用已经在使用 Youtube Data API (v3) 服务，因此，这对您使用这些已升级的第三方应用向 YouTube 上传视频没有任何影响。

但是，如果您使用的第三方应用尚未升级到较新的 YouTube Data API (v3) 服务，因此未采用这项技术向 YouTube 上传视频，则您将无法使用这些应用将视频上传至 YouTube。

## 排查身份验证问题

如果您在尝试登录到第三方应用时看到“用户名/密码组合无法通过验证”这一消息，请按照以下步骤上传您的视频：

1. 将视频从第三方应用中导出。
2. 使用 [youtube.com](https://support.google.com/youtube/answer/www.youtube.com) 桌面版网站或移动版 YouTube 应用上传视频。

您还可以尝试更新第三方应用。前提是开发者提供了该应用的升级版本，在较新的产品版本中使用 YouTube Data API (v3) 服务。如果更新应用仍无法解决问题，您可以与第三方应用开发者联系。