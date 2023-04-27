[English](https://github.com/paulmillr/encrypted-dns/) | 简体中文 | [繁體中文](https://github.com/paulmillr/encrypted-dns/blob/master/README.cmn-TW.md)

# 加密 DNS 配置

[DNS over HTTPS](https://en.wikipedia.org/wiki/DNS_over_HTTPS) 和 [DNS over TLS](https://en.wikipedia.org/wiki/DNS_over_TLS) 的配置描述文件。查看这篇文章以获取更多信息：[paulmillr.com/posts/encrypted-dns/](https://paulmillr.com/posts/encrypted-dns/) 以及有关[提交新描述文件](#提交新描述文件)的信息。

### 注意事项

根据[谷歌这篇文章](https://security.googleblog.com/2022/07/dns-over-http3-in-android.html)的介绍，DoH 似乎比 DoT 的性能更优。

从 iOS 和 iPadOS 15.5 开始，为了简化咖啡厅、宾馆、机场等公共场所无线网络的身份认证，苹果将这些无线网络的[强制登录门户](https://en.wikipedia.org/wiki/Captive_portal)加入到了加密 DNS 排除规则中。这是个好消息，但还有一些其他问题我们无法修复，只有等苹果来解决：

- 无法启用加密 DNS：[Little Snitch & Lulu](https://github.com/paulmillr/encrypted-dns/issues/13)、[VPN](https://github.com/paulmillr/encrypted-dns/issues/18)
- 部分流量绕过加密 DNS：[终端和 App Store](https://github.com/paulmillr/encrypted-dns/issues/22)、[Chrome 浏览器](https://github.com/paulmillr/encrypted-dns/issues/19)

如果你需要更进一步的隐私保护，请查看[使用 Tor 网络的加密 DNS](https://github.com/alecmuffett/dohot)。

## 供应商

“`审查=是`”表示描述文件不会发送某些主机“`主机名=IP`”关系的真实信息。

| 名称                                                                                                                                             | 区域  | 审查 | 备注                                                               | 安装链接                                                                                                                                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ----- | ---- | ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [360 安全 DNS](https://sdns.360.net/dnsPublic.html)                                                                                              | 🇨🇳    | 是   | 由 360 数字安全集团运营                                            | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/360-https.mobileconfig)                                                                                                                                       |
| [AdGuard DNS 默认](https://adguard-dns.io/kb/zh-CN/general/dns-providers/#default)                                                               | 🇷🇺    | 是   | 由 AdGuard 运营，拦截广告、跟踪器和钓鱼网站                        | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-default-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-default-tls.mobileconfig)                   |
| [AdGuard DNS 家庭保护](https://adguard-dns.io/kb/zh-CN/general/dns-providers/#family-protection)                                                 | 🇷🇺    | 是   | 由 AdGuard 运营，除默认规则外，额外拦截恶意软件和成人内容          | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-family-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-family-tls.mobileconfig)                     |
| [AdGuard DNS 无过滤](https://adguard-dns.io/kb/zh-CN/general/dns-providers/#non-filtering)                                                       | 🇷🇺    | 否   | 由 AdGuard 运营，无过滤                                            | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-nofilter-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-nofilter-tls.mobileconfig)                 |
| [Alekberg 加密 DNS](https://alekberg.net)                                                                                                        | 🇳🇱    | 否   | 由个人提供                                                         | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/alekberg-https.mobileconfig)                                                                                                                                  |
| [阿里云公共 DNS](https://www.alidns.com/)                                                                                                        | 🇨🇳    | 是   | 由阿里云计算运营                                                   | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/alibaba-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/alibaba-tls.mobileconfig)                                   |
| [BlahDNS CDN 过滤](https://blahdns.com/)                                                                                                         | 🇺🇸    | 是   | 由个人提供，拦截广告、跟踪器和恶意软件                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-cdn-adblock-doh1.mobileconfig)                                                                                                                        |
| [BlahDNS CDN 无过滤](https://blahdns.com/)                                                                                                       | 🇺🇸    | 否   | 由个人提供，无过滤                                                 | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-cdn-unfiltered-doh1.mobileconfig)                                                                                                                     |
| [BlahDNS 芬兰](https://blahdns.com/)                                                                                                             | 🇫🇮    | 是   | 由个人提供，拦截广告、跟踪器和恶意软件                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-finland-doh.mobileconfig)                                                                                                                             |
| [BlahDNS 德国](https://blahdns.com/)                                                                                                             | 🇩🇪    | 是   | 由个人提供，拦截广告、跟踪器和恶意软件                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-germany-doh.mobileconfig)                                                                                                                             |
| [BlahDNS 日本](https://blahdns.com/)                                                                                                             | 🇯🇵    | 是   | 由个人提供，拦截广告、跟踪器和恶意软件                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-japan-doh.mobileconfig)                                                                                                                               |
| [BlahDNS 新加坡](https://blahdns.com/)                                                                                                           | 🇸🇬    | 是   | 由个人提供，拦截广告、跟踪器和恶意软件                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-singapore-doh.mobileconfig)                                                                                                                           |
| [BlahDNS 瑞士](https://blahdns.com/)                                                                                                             | 🇨🇭    | 是   | 由个人提供，拦截广告、跟踪器和恶意软件                             | [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-switzerland-dot.mobileconfig)                                                                                                                           |
| [Canadian Shield 隐私](https://www.cira.ca/cybersecurity-services/canadian-shield/configure/summary-cira-canadian-shield-dns-resolver-addresses) | 🇨🇦    | 否   | 由加拿大互联网注册局 (CIRA) 运营                                   | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-private-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-private-tls.mobileconfig)     |
| [Canadian Shield 保护](https://www.cira.ca/cybersecurity-services/canadian-shield/configure/summary-cira-canadian-shield-dns-resolver-addresses) | 🇨🇦    | 是   | 由加拿大互联网注册局 (CIRA) 运营，拦截恶意软件和钓鱼网站           | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-protected-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-protected-tls.mobileconfig) |
| [Canadian Shield 家庭](https://www.cira.ca/cybersecurity-services/canadian-shield/configure/summary-cira-canadian-shield-dns-resolver-addresses) | 🇨🇦    | 是   | 由加拿大互联网注册局 (CIRA) 运营，拦截恶意软件、钓鱼网站和成人内容 | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-family-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-family-tls.mobileconfig)       |
| [Cloudflare 1.1.1.1](https://developers.cloudflare.com/1.1.1.1/encryption/)                                                                      | 🇺🇸    | 否   | 由 Cloudflare 运营                                                 | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/cloudflare-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/cloudflare-tls.mobileconfig)                             |
| [Cloudflare 1.1.1.1 恶意软件防护](https://developers.cloudflare.com/1.1.1.1/setup/#1111-for-families)                                            | 🇺🇸    | 是   | 由 Cloudflare 运营，拦截恶意软件和钓鱼网站                         | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/cloudflare-malware-https.mobileconfig)                                                                                                                        |
| [Cloudflare 1.1.1.1 家庭](https://developers.cloudflare.com/1.1.1.1/setup/#1111-for-families)                                                    | 🇺🇸    | 是   | 由 Cloudflare 运营，拦截恶意软件、钓鱼网站和成人内容               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/cloudflare-family-https.mobileconfig)                                                                                                                         |
| [DNSPod 公共 DNS](https://www.dnspod.cn/products/publicdns)                                                                                      | 🇨🇳    | 是   | 由腾讯云计算旗下 DNSPod 运营                                       | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/dnspod-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/dnspod-tls.mobileconfig)                                     |
| [谷歌公共 DNS](https://developers.google.com/speed/public-dns/docs/secure-transports?hl=zh-cn)                                                   | 🇺🇸    | 否   | 由谷歌运营                                                         | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/google-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/google-tls.mobileconfig)                                     |
| [Mullvad](https://mullvad.net/zh-hans/help/dns-over-https-and-dns-over-tls/)                                                                     | 🇸🇪    | 是   | 由 Mullvad VPN 运营                                                | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/mullvad-doh.mobileconfig)                                                                                                                                     |
| [Mullvad 广告过滤](https://mullvad.net/zh-hans/help/dns-over-https-and-dns-over-tls/)                                                            | 🇸🇪    | 是   | 由 Mullvad VPN 运营，拦截广告和跟踪器                              | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/mullvad-adblock-doh.mobileconfig)                                                                                                                             |
| [OpenDNS 标准](https://support.opendns.com/hc/articles/360038086532)                                                                             | 🇺🇸    | 否   | 由思科 OpenDNS 运营                                                | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/opendns-https.mobileconfig)                                                                                                                                   |
| [OpenDNS 家庭防护](https://support.opendns.com/hc/articles/360038086532)                                                                         | 🇺🇸    | 是   | 由思科 OpenDNS 运营，拦截恶意软件和成人内容                        | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/opendns-family-https.mobileconfig)                                                                                                                            |
| [Quad9](https://www.quad9.net/news/blog/doh-with-quad9-dns-servers/)                                                                             | 🇨🇭    | 是   | 由 CleanerDNS 运营，拦截恶意软件                                   | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/quad9-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/quad9-tls.mobileconfig)                                       |
| [Quad9 ECS](https://www.quad9.net/news/blog/doh-with-quad9-dns-servers/)                                                                         | 🇨🇭    | 是   | 由 CleanerDNS 运营，支持 ECS，拦截恶意软件                         | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/quad9-ECS-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/quad9-ECS-tls.mobileconfig)                               |
| [Tiarap](https://doh.tiar.app)                                                                                                                   | 🇸🇬 🇺🇸 | 是   | 由 Tiarap 运营，拦截广告、跟踪器、钓鱼网站和恶意软件               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/tiarapp-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/tiarapp-tls.mobileconfig)                                   |

## 安装

要使设置在 **iOS**、**iPadOS** 和 **macOS** 中所有的应用程序上生效，你需要安装配置描述文件。此文件将指引操作系统使用 DoH 或 DoT。注意：只在系统无线局域网设置中设置 DNS 服务器 IP 是不够的——你需要安装描述文件。

iOS / iPadOS：使用 Safari 浏览器（其他浏览器只会下载该文件，不会弹出安装提示）打开 GitHub 上的 mobileconfig 文件，然后点击“允许”按钮，描述文件将完成下载。打开 **系统设置 => 通用 => VPN、DNS 与设备管理**，选择已下载的描述文件并点击“安装”按钮。

macOS [（官方文档）](https://support.apple.com/zh-cn/guide/mac-help/mh35561/)：

1. 下载并保存描述文件，将其重命名为 `NAME.mobileconfig`，而不是 txt 之类的扩展名。
2. 选取苹果菜单 >“系统设置”，点按边栏中的“隐私和安全性” ，然后点按右侧的“描述文件”。（你可能需要向下滚动。）
   安装期间，系统可能会要求你提供密码或其他信息。
3. 在“已下载”部分中，连按描述文件。
4. 检查描述文件内容，然后点按“继续”、“安装”或“注册”以安装描述文件。

   如果 Mac 上已安装了较早版本的描述文件，其设置将替换为更新版本中的设置。

## 范围

这条[额外选项](https://github.com/paulmillr/encrypted-dns/issues/22)似乎可以让描述文件在系统全局范围生效。如果有兴趣尝试，请将下面的内容添加到 mobileconfig 文件中：

```xml
<key>PayloadScope</key>
<string>System</string>
```

## 签名版描述文件

在 `signed` 文件夹中，存放了*稍微过时的*签名版描述文件。这些描述文件已由 [@Candygoblen123](https://github.com/Candygoblen123) 签名，因此当你安装时，界面上会有“已验证”的提示，此举还可确保这些描述文件未被篡改。但由于这些描述文件是交由第三方签名的，因此可能会稍微落后于未签名的版本。

[备注]: <> (我们建议安装签名版的描述文件，因为数字签名可以确保文件在下载时没有被修改。)

如要验证 DNS 解析器的 IP 和主机名，请将描述文件内容与其官方网站的文档进行比对，描述文件内部结构和属性在[苹果开发者网站](https://developer.apple.com/documentation/devicemanagement/dnssettings)上有详细讲解。如要验证签名版的描述文件，请将其下载到本地后用文本编辑器打开，因为 GitHub 会将签名版描述文件视为二进制文件而无法直接查看。

## 提交新描述文件

描述文件本质上是文本文件，将现有的描述文件复制一份并修改其 UUID 即可，请确保在本 README 文件中更新描述文件的相关信息。

随机 UUID 除了可以通过网站在线生成，还有很多其他获取方法：

- 在浏览器中按下 `F12` 打开“开发人员工具”，在控制台中运行这段代码

```javascript
crypto.randomUUID();
```

- 在 macOS / Linux 终端中运行此命令

```sh
# 适用于 macOS 和 Linux
uuidgen

# 适用于 Linux
cat /proc/sys/kernel/random/uuid
```

- 在 Powershell 中运行此命令

```powershell
New-Guid
```
