# Aspera 简介

本文中介绍的功能仅适合使用 YouTube [内容管理器](https://www.youtube.com/dashboard)来管理其受版权保护的内容的合作伙伴。

Aspera 是 IBM 推出的一款用于高速文件传输的桌面客户端软件。这款软件是免费的并且可以在“内容传送”下的“上传工具帐号”标签中下载。要使用这款软件，请与您的 YouTube 合作伙伴代表联系，以创建一个 Aspera 上传工具帐号。




# 为 Aspera Dropbox 生成 Secure Shell (SSH) 密钥对

本文中介绍的功能仅适合使用 YouTube [内容管理器](https://www.youtube.com/dashboard)来管理其受版权保护的内容的合作伙伴。

YouTube 要求使用 Secure Shell (SSH) 连接来连接到用于 YouTube 的 Dropbox。SSH 是一种网络协议，可以确保安全的数据传输。

SSH 会使用公钥加密方法验证您的身份。您需要创建一对密钥：一个是存储在您的客户端计算机上的私钥，一个是 Dropbox 服务器使用的公钥。您必须同时拥有这两个秘钥，这样您的计算机才能连接到 Dropbox。

您需要向合作伙伴代表提供您的 SSH 公钥，然后合作伙伴代表才能为您创建 Dropbox。此公钥是一个字符串，以“ssh-rsa”开头，以您的电子邮件地址结尾，中间包含一段生成的长字符串。例如：

`ssh-rsaAAAAB3NzaC1yc2EAAAADAQABAAABAQCXsM9ycbHV6E6t2L+B4p/uYHn9Q0jmu5gU XMYnFnnf4l39xrznfDo8KCASzRrqUkRnuzrno059CvZVzcljkbwWLzKKoE1EwbzH L3nYahMB4MdYNWhBbHbB+ybq6RNO7hkoKDBIQCfqQDY0FEB6sV3d3F1WYl0bAMjp 15yyZJzMKa/rRnZKWetHlcL1X+gFWmW2hQ93foPD463gb58/25GujjsS/tzjngw7 UJMVkm08U1QEY3z3DE/R++7ovJozTCzH0CTNDN0AH3/oSC3dmG+yDh3ZXFATjWjy PXJSOziNrp9TXgJhlqSmoHcPvpotMVjx21kIZ+T+SusQmnG+hK+Luser@yourdomain.com`

注意：该公钥不能包含换行符。

要为 Aspera Dropbox 生成 SSH 密钥，请执行以下操作：

1. 打开您的 Aspera 客户端。
2. 从  **Tools**  菜单中，选择“Manage Keys”。
3. 在  **SSH Keys**  窗口，点击  **+**  以弹出  **New SSH Key Pair**  窗口。![|477x269](https://lh5.ggpht.com/Q1SEVEmWLUYFuJJ28-Uc4ekkPqtpe1idIEL37YQOot8mwNi3CFmmPFHWvniA4sVr9JxFlldZAA=w477)
4. 在  **Identity**  框中为此密钥对输入名称。密钥将以此  **Identity**  名称显示在您的 SSH 密钥列表中。
5. 将  **Type**  下拉列表设为  **RSA** 。
6. 点击  **OK**  以生成密钥对。您的新 SSH 密钥名会出现在  **SSH Keys**  窗口内的列表中，公钥单独显示在  **Public Key**  文本框中。
7. 点击  **Copy to Clipboard**  以复制公钥。
8. 将公钥的文本发送给您的合作伙伴代表。您可以将公钥从剪贴板粘贴到电子邮件中。
9. 点击  **SSH Keys**  窗口中的  **Close** ，完成此过程。








# 配置您的 Dropbox

本文中介绍的功能仅适合使用 YouTube [内容管理器](https://www.youtube.com/dashboard)来管理其受版权保护的内容的合作伙伴。

在合作伙伴代表为您创建保管箱以后，您需要配置帐户的默认设置。

要配置您的 Dropbox，请执行以下操作：

1. 登录到 YouTube 内容所有者的[信息中心](https://www.youtube.com/dashboard)。
2. 点击 **内容传送** 框中的[ **上传者帐号** ](https://www.youtube.com/content_delivery#delivery/a)。
3. 记下 Dropbox 的名称和地址。今后您将需要使用此信息连接到 Dropbox。Aspera Dropbox 的名称以  **asp-**  开头；而 SFTP Dropbox 的名称则以  **yt-**  开头。Aspera Dropbox 的地址显示为 **服务器地址** ；而 SFTP Dropbox 的地址则是  `partnerupload.google.com` 。

有众多内容所有者的帐号可能有不止一个 Dropbox。请确保记下了自己的 Dropbox 信息。

4. 确认 **默认频道** 和  **SSH 公钥** 正确无误。如果内容 Feed 没有另行指定所有者，默认 YouTube 用户会标识出将被指定为所上传视频的所有者的帐号（频道）。 **SSH 公钥** 框应包含您发送给合作伙伴代表的 SSH 密钥。请确保密钥末尾含有您的电子邮件地址。
5. 在 **通知电子邮件地址** 文本框中输入一个或多个电子邮件地址，YouTube 将通过这些地址向您发送状态报告。输入多个电子邮件地址时，每行输入一个地址。点击 **保存** 。

请注意，一个 Dropbox 对应一个内容所有者，而不是对应一个频道。也就是说，您仅用一个 Dropbox 就可以向多个不同的频道上传内容。





# 关联至您的 Aspera Dropbox

本文中介绍的功能仅适合使用 YouTube [内容管理器](https://www.youtube.com/dashboard)来管理其受版权保护的内容的合作伙伴。

[配置 Dropbox](https://support.google.com/youtube/answer/answer.py?answer=3070575) 后，您需要在 Aspera 客户端与 Dropbox 之间创建一个可重复使用的连接。

确保准备好 Dropbox 名称和 IP 地址，方便需要时参考；您可以在 YouTube 内容管理器中的 [Dropbox 帐号设置页面](https://cms.youtube.com/dropbox_manage)上找到这些信息。

要创建 Aspera 连接，请执行以下操作：

1. 打开您的 Aspera 客户端。
2. 点击 **连接** 图标以打开  **Connection Manager** 。
3. 点击  **+**  以创建新连接。![|587x493](https://lh5.ggpht.com/r4yFzxFSN7-TJcyRT-s5d9hHKKkzoHXWfbQ0NaKydWANs7UYVvwgWE-bcekbwNN3wKdwPlUS_w=w587)
4. 在  **Host**  文本框中输入 Dropbox 的 IP 地址。
5. 在  **User**  文本框中输入 Dropbox 名称。
6. 选择  **Public Key**  作为身份验证选项，然后从可用密钥列表中为该 Dropbox 选择密钥。
7. 点击  **Advanced**  按钮以显示  **Advanced Connection Settings** 。
8. 将  **SSH Port (TCP)**  的值更改为 33001。
9. 点击两次  **OK**  以保存更改并返回到 Aspera 客户端主屏幕。您的新连接将出现在屏幕的右侧。





# 将内容上传到 Aspera Dropbox

本文中介绍的功能仅适合使用 YouTube [内容管理器](https://www.youtube.com/dashboard)来管理其受版权保护的内容的合作伙伴。

为批量上传[验证元数据](https://support.google.com/youtube/answer/answer.py?answer=3041024)后，您就可以上传文件了。要上传内容，您可以先将所需的文件复制到您的 Dropbox，然后创建一个名为 delivery.complete 的文件来提醒我们这些文件已经准备就绪。

您需要哪些文件来完成上传取决于您要上传的资产类型。每个上传作业都必须包括一个 XML 或 CSV 格式的元数据文件，以及该元数据文件通过名称引用的所有新媒体文件。

我们建议一次上传一个新资产，每个资产都有专属 Dropbox 文件夹和元数据文件。例如，如果您要上传三集电视节目，请创建三个不同的文件夹和三个不同的元数据文件。此方法有助于更轻松地跟踪上传进度并限制任何出现的问题所造成的影响，却不会对上传处理速度产生任何影响。

（[其他推荐的最佳做法](https://support.google.com/youtube/answer/answer.py?answer=3149776)）

Aspera Dropbox 的每周维护时间为美国太平洋时间星期一凌晨 1 点到 5 点。如果您在此期间上传内容，则您的 Aspera 客户端与 Dropbox 的连接可能会断开。如果连接断开，请在 5-10 分钟之后重新连接 Dropbox，然后重新传送整个元数据文件。

要将内容上传到您的 Aspera Dropbox，请按以下步骤操作：

1. 打开您的 Aspera 客户端。
2. 在右侧的  **Connection**  框中选择您的 Dropbox 的连接，然后点击  **Connection**  按钮。Aspera 客户端会连接到您的 Dropbox，并显示顶级文件夹。如果您尚未为您的 Dropbox 设置连接，请参阅[连接到您的 Aspera Dropbox](https://support.google.com/youtube/answer/3070594)。
3. 为新的上传作业新建一个文件夹。要创建文件夹，请右键点击父文件夹并选择  **New > Folder** 。为了避免可能出现的冲突，建议您每次发布内容时都新建一个目录，并在每个目录的名称中加入时间戳或增量 ID。
4. 将要打包上传的所有文件复制到新文件夹中。要将文件复制到一个文件夹中，首先要确保目标文件夹已在右侧打开，然后在左侧框中突出显示要复制的文件，再点击向右的箭头即可。![|635x272](https://lh6.ggpht.com/TUVW1WBcXIFPdpJsWw4y_YpQ3a1LK8luDGgcCVwbjMBnJ4PqCaU4Zb3Nj_m46TKKP2QIjtx7=w635)
5. 当所有文件都复制完毕后，将 delivery.complete 文件上传到同一文件夹中。

发布 delivery.complete 文件后，您不得再将任何新文件添加到目录或其任何子目录中。根据批次的大小，可能需要几秒钟或几分钟才能发现文件正在处理。 **每批次请仅上传一个 delivery.complete 文件。**

每次处理完批量上传后，上传引擎会发布一份状态报告，详细说明对该批次中的各项内容执行的操作。报告的名称为 status-xml-filename，其中 xml-filename 是您的元数据文件名。状态报告会放在您的 Dropbox 中，与批量上传的文件位于同一目录下。

处理批量上传和生成状态报告所需的时间因系统负荷和请求的操作而异。例如，系统处理资产的元数据更新所需的时间大大少于处理新参考文件的时间。此外，如果处理批量文件时发生失败操作，系统会重试某些失败的操作（目的是确保失败并非是系统停机等瞬态条件导致的），这也会造成上传引擎需花费更多的处理时间。在某些情况下，我们可能需要超过一天的时间来处理一次批量上传。




# Aspera Dropbox 上传最佳做法

本文中介绍的功能仅适合使用 YouTube [内容管理器](https://www.youtube.com/dashboard)来管理其受版权保护的内容的合作伙伴。

请遵循以下准则将内容（元数据和参考文件）上传到 Google。

### 为每次批量上传的内容创建一个专属文件夹

您发布到 Dropbox 的所有文件都必须位于文件夹中。Google 会忽略 Dropbox 根文件夹中的文件，包括任何  `delivery.complete`  文件。

为了避免可能的命名冲突，我们建议您在每次发布内容时都新建一个文件夹，并在每个文件夹的名称中加入时间戳或增量 ID。时间戳或 ID 是跟踪批量上传的绝佳方法。

### 缩减批次规模

创建多个较小的批次，而不是单个较大的批次。通常情况下，我们建议您一次上传一个资产的文件。如果您使用 Dropbox，请为每个资产创建一个单独的目录以及一个单独的  `delivery.complete`  文件。

处理 10 个分别包含一个资产的批次的时间，并不会比处理一个包含 10 个资产的批次长。但是，每个批次的处理速度都比较快，而且所有失败的上传操作仅影响有问题的资产。

建议每次批量上传的资产数目不超过 100 个。元数据文件（CSV 或 XML）不能超过 10MB。

### 包含所有参考文件

请确保元数据 CSV 或 XML 文件中引用的文件名与您上传的实际文件一致，包括文件扩展名。如果名称不一致或缺少参考文件，则上传将失败。

### 从 Dropbox 中移除成功上传的批次的文件夹

您的 Dropbox 是用于上传内容的暂存区。它的既定用途并非是长期存储。我们会自动移除 Dropbox 中超过 45 天的文件，同时，建议您删除已成功上传的批次的文件夹和状态文件。

Dropbox 帐号的  **`failed_packages`**  子目录包含我们无法成功上传的文件。请检查这些文件，纠正导致无法正常上传的问题，然后将这些文件移至相应文件夹，以进行新的批量上传。当您将  `delivery.complete`  文件添加到文件夹时，我们将再次处理这些文件。






# 诊断 Aspera Dropbox 的上传问题

本文中介绍的功能仅适合使用 YouTube [内容管理器](https://www.youtube.com/dashboard)来管理其受版权保护的内容的合作伙伴。

您在使用 Aspera Dropbox 向 YouTube 上传内容时遇到了问题？请回答下面的问题，以帮助找到并解决问题。

Aspera Dropbox 的每周维护时间为美国太平洋时间星期三凌晨 1 点到 5 点。如果您在此期间上传内容，则您的 Aspera 客户端与 Dropbox 的连接可能会断开。如果连接断开，请在 5-10 分钟之后重新连接 Dropbox，然后重新提交完整的元数据文件。

您能否使用 Aspera 客户端连接 Dropbox？能够连接 Dropbox。无法连接 Dropbox。


