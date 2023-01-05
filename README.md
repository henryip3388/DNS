# Apple iOS & MacOS DNS Profiles

## Providers

`Censorship=yes` means the profile will not send true information about `hostname=IP` relation for some hosts because there will be filtering when resolving the domain name.

| Name                      | Country | Censorship | Notes                                                                                                                                   | Install button                                                                                                                                                                                                      |
|---------------------------|---------|------------|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AdGuard Default           | 🇷🇺      | Yes          | [Operated](https://adguard-dns.io/kb/general/dns-providers/#default) by AdGuard (Filters ads, tracking & phishing)                                            | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-default-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-default-tls.mobileconfig)                                                                                                                           |
| AdGuard Family            | 🇷🇺      | Yes          | [Operated](https://adguard-dns.io/kb/general/dns-providers/#family-protection) by AdGuard (Filters Default + malware & adult content)                                       | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-family-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-family-tls.mobileconfig)                                                                               |
| AdGuard No Filter         | 🇷🇺      | No          | [Operated](https://adguard-dns.io/kb/general/dns-providers/#non-filtering) by AdGuard (Non-filtering)                                     | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-nofilter-https.mobileconfig),  [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/adguard-nofilter-tls.mobileconfig)                                                                                                                    |
| AliDNS                    | 🇨🇳      | Yes          | [Operated](https://www.alidns.com/) by Alibaba in China                                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/alibaba-https.mobileconfig),  [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/alibaba-tls.mobileconfig)                                    |
| Alekberg                  | 🇳🇱      | No          | [Independent](https://alekberg.net) hoster in Netherlands                                                                               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/alekberg-https.mobileconfig)                                                                                                                          |
| BlahDNS CDN Filtered      | 🇺🇸      | Yes          | [Independent](https://blahdns.com/)                                                                               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-cdn-adblock-doh1.mobileconfig)                                                                                                                          |
| BlahDNS CDN Unfiltered    | 🇺🇸      | No          | [Independent](https://blahdns.com/)                                                                               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-cdn-unfiltered-doh1.mobileconfig)                                                                                                                          |
| BlahDNS Finland Adsblock  | 🇫🇮      | Yes          | [Independent](https://blahdns.com/)                                                                               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-finland-doh.mobileconfig)                                                                                                                          |
| BlahDNS Germany Adsblock  | 🇩🇪      | Yes          | [Independent](https://blahdns.com/)                                                                               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-germany-doh.mobileconfig)                                                                                                                          |
| BlahDNS Japan Adsblock    | 🇯🇵      | Yes          | [Independent](https://blahdns.com/)                                                                               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-japan-doh.mobileconfig)                                                                                                                          |
| BlahDNS Singapore Adsblock| 🇸🇬      | Yes          | [Independent](https://blahdns.com/)                                                                               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-singapore-doh.mobileconfig)                                                                                                                          |
| BlahDNS Swiss Adsblock    | 🇨🇭      | Yes          | [Independent](https://blahdns.com/)                                                                               | [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/blahdns-switzerland-dot.mobileconfig)                                                                                                                          |
| Canadian Shield Private   | 🇨🇦      | No          | [Operated](https://www.cira.ca/cybersecurity-services/canadian-shield/configure) by the Canadian Internet Registration Authority (CIRA) | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-private-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-private-tls.mobileconfig)     |
| Canadian Shield Protected | 🇨🇦      | Yes          | [Filters](https://www.cira.ca/cybersecurity-services/canadian-shield/configure) malware                                                 | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-protected-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-protected-tls.mobileconfig) |
| Canadian Shield Family    | 🇨🇦      | Yes          | [Filters](https://www.cira.ca/cybersecurity-services/canadian-shield/configure) malware & adult content                                 | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-family-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/canadianshield-family-tls.mobileconfig)       |
| Cloudflare                | 🇺🇸      | No          | [Operated](https://developers.cloudflare.com/1.1.1.1/dns-over-https) by Cloudflare 1.1.1.1                                              | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/cloudflare-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/cloudflare-tls.mobileconfig)                             |
| Cloudflare Malware        | 🇺🇸      | Yes          | Filters malware                                                                                                                         | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/cloudflare-malware-https.mobileconfig)                                                                                                                |
| Cloudflare Family         | 🇺🇸      | Yes          | Filters malware & adult content                                                                                                         | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/cloudflare-family-https.mobileconfig)                                                                                                                 |
| DNSPod                    | 🇨🇳      | Yes          | [Operated](https://www.dnspod.cn/Products/publicdns?lang=en) by DNSPod (Tencent) in China                                               | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/dnspod-https.mobileconfig),  [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/dnspod-tls.mobileconfig)                                                                                                                            |
| Google                    | 🇺🇸      | No          | [Operated](https://developers.google.com/speed/public-dns/docs/secure-transports) by Google                                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/google-https.mobileconfig),  [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/google-tls.mobileconfig)                                    |
| OpenDNS                   | 🇺🇸      | No          | [Operated](https://support.opendns.com/hc/en-us/articles/360038086532) by OpenDNS                                                       | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/opendns-https.mobileconfig)                                                                                                                           |
| OpenDNS Family            | 🇺🇸      | Yes          | Filters malware & adult content                                                                                                         | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/opendns-family-https.mobileconfig)                                                                                                                    |
| Quad9                     | 🇨🇭     | Yes          | [Operated](https://www.quad9.net/news/blog/doh-with-quad9-dns-servers/) by CleanerDNS, Inc. Filters malware                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/quad9-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/quad9-tls.mobileconfig)                                        |
| Quad9 With ECS            | 🇨🇭     | Yes          | [Operated](https://www.quad9.net/news/blog/doh-with-quad9-dns-servers/) by CleanerDNS, Inc. Filters malware                             | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/quad9-ECS-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/quad9-ECS-tls.mobileconfig)                                        |
| Tiar.app                  | 🇸🇬 🇺🇸    | Yes          | ["Privacy-first DNS provider"](https://doh.tiar.app) from SG, hosted on Digital Ocean. Filters malware                                  | [HTTPS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/tiarapp-https.mobileconfig), [TLS](https://github.com/paulmillr/encrypted-dns/raw/master/profiles/tiarapp-tls.mobileconfig)                                    |


## Installation

To make settings work in **iOS** & **MacOS**, you’ll need to install a configuration profile. This profile would tell operating system to use DoH or DoT. Note: it’s not enough to simply set server IPs in System Preferences — you need to install a profile, unfortunately.

To install, simply open the file in GitHub by using Safari (other browsers will just download the file and won't ask for installation), and then click/tap on install button. The profile should download. On macOS, double click on the downloaded file to open it in settings, and approve instalation. On iOS, go to **System Settings => General => Profile**, select downloaded profile and tap the “Install” button.

## Contributing a new profile

Profiles are basically text files. Copy an existing one and change its UUID, for example, by generating a new one online (https://www.uuidgenerator.net/). Make sure you update README with new profile's info.
