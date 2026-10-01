# 搬瓦工 THE AMSTERDAM PLAN：$39/年阿姆斯特丹 VPS 配置、线路与购买建议

搜索“搬瓦工 THE AMSTERDAM PLAN”的人，通常不是在找普通荷兰 VPS，而是在确认三个问题：

- 这个限量套餐现在是否还有货？
- $39/年的配置和线路到底值不值得买？
- 它与搬瓦工 Basic、E-Commerce、CN2 GIA 方案相比，适合什么用途？

The Amsterdam Plan 是 BandwagonHost 推出的限量版自管 KVM VPS，机房位于荷兰阿姆斯特丹 DC1。公开资料显示，它采用 **1 核 AMD CPU、1 GB 内存、20 GB RAID-10 SSD、每月 1 TB 流量和 2.5 Gbps 端口**，年付价格为 **39 美元**。它的吸引力不在于硬件有多豪华，而在于低价获得欧洲节点和面向中国大陆的优化网络。

不过，这个套餐也有两个现实限制：它属于限量产品，库存不会长期稳定；同时服务是严格自主管理，系统配置、应用部署、安全维护和故障排查都需要用户自己处理。

## The Amsterdam Plan 当前配置

根据近期公开的官方产品描述和多个独立测评页面，The Amsterdam Plan 的主要参数如下：

| 项目 | 配置 |
| --- | --- |
| 产品名称 | VPS - Self-managed - The Amsterdam Plan |
| 机房位置 | Amsterdam, Netherlands DC1 |
| 常见机房编号 | EUNL_1 |
| 虚拟化 | KVM / KiwiVM |
| CPU | 1 核 AMD |
| 内存 | 1 GB |
| 硬盘 | 20 GB RAID-10 SSD |
| 月流量 | 1,000 GB |
| 端口速率 | 2.5 Gbps |
| IPv4 | 1 个独立 IPv4 |
| IPv6 | 路由 /64 子网 |
| 系统权限 | Full root access |
| 备份 | 自动备份 |
| 快照 | 支持 |
| 计费周期 | 年付 |
| 公开价格 | $39/年 |
| 服务类型 | 自管式 VPS |

近期测试资料还记录到该套餐运行在 AMD EPYC-Genoa 平台上，使用 Debian 12 和 KVM 虚拟化。不过，CPU 型号、宿主机负载和具体 IP 网络表现可能随批次变化，不应该把第三方一次测试结果当成所有实例的固定承诺。

👉 [查看 The Amsterdam Plan 当前库存与年付价格](https://bandwagonhost.com/aff.php?aff=74518&pid=159)

## $39/年到底买到了什么

The Amsterdam Plan 的配置属于轻量级 VPS。1 GB 内存和 20 GB SSD 足够运行一些基础服务，但不适合把它当成高性能生产服务器。

比较合适的用途包括：

- 个人博客和小型展示站
- 静态网站
- 轻量级 API
- WireGuard、Tailscale 等网络工具
- 个人开发测试环境
- 监控、Webhook、定时任务
- 小型反向代理
- 轻量级 Docker 服务
- 低访问量的海外站点

如果你准备运行大型数据库、Java 应用、编译任务、图片处理、视频转码或多个高占用 Docker 容器，1 GB 内存很容易成为限制。增加 Swap 可以缓解偶发的内存峰值，但不能把 1 GB VPS 变成 4 GB VPS。对配置要求较高的应用，应该直接看 4 GB 或 8 GB 以上的方案。

## 网络线路是这个套餐的重点

The Amsterdam Plan 的卖点主要是阿姆斯特丹节点和面向中国大陆的线路优化。公开资料中列出的网络包括：

- 中国电信 CTGNet / CN2 GIA
- 中国联通 Premium AS10099 或 AS9929
- 中国移动 CMIN2

不同页面对联通线路的具体标注并不完全一致，早期产品介绍也曾出现“后续加入”的描述。因此，购买前更应该以结账页和实际分配到的 IP 测试结果为准，不要只根据套餐名称判断三网表现。

阿姆斯特丹节点更适合以下场景：

- 欧洲用户访问的网站
- 需要欧洲 IP 的轻量应用
- 欧洲到亚洲之间的中转服务
- 对荷兰地区内容可用性有需求的项目
- 希望以较低成本测试欧洲线路的用户

但它不一定适合所有中国大陆用户。欧洲到中国的物理距离更远，基础延迟通常高于香港、日本和美国洛杉矶节点。即使线路属于优化网络，晚高峰、运营商和具体 IP 仍然会影响实际体验。

简单说，The Amsterdam Plan 是“低价欧洲优化线路”，不是“低延迟中国节点”。如果你的访客主要在华东、华南，并且对交互延迟非常敏感，香港或日本方案更值得比较；如果访客主要在欧洲，阿姆斯特丹的地理位置反而更合理。

## 与普通 Basic VPS 的区别

BandwagonHost 的 Basic VPS 是常规产品线，官网当前公开的基础方案包括 20G、40G、80G、160G、320G 和 480G 等配置。它们可以选择部分基础机房，强调低成本和本地互联，不以高级中国线路为主要卖点。

The Amsterdam Plan 与 Basic 20G 的差别主要在三个地方：

1. **价格结构不同**
   Basic 20G 目前公开价格为 $49.99/年，The Amsterdam Plan 为 $39/年。

2. **机房定位不同**
   Basic 20G 是多机房基础产品，具体可选位置取决于库存；The Amsterdam Plan 绑定阿姆斯特丹 DC1。

3. **网络卖点不同**
   Amsterdam Plan 面向中国大陆的线路描述更突出，而 Basic 系列更偏向普通 VPS 和本地互联。

如果你只需要一个便宜的 Linux 服务器，Basic 20G 的供应通常更容易理解；如果你明确需要阿姆斯特丹节点，同时希望测试优化线路，The Amsterdam Plan 的价格更有吸引力。

## 搬瓦工当前公开方案对比

下面整理的是官网当前公开可见的主要常规 VPS 配置。价格会根据机房、计费周期和库存变化，表格中的价格以近期官网页面显示为准。The Amsterdam Plan 属于限量方案，单独列出。

### Basic VPS

| 套餐 | CPU | 内存 | SSD | 月流量 | 端口 | 价格 | 购买 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| 20G KVM | 2 核 | 1 GB | 20 GB | 1 TB | 1 Gbps | $49.99/年 | [ 查看 20G Basic](https://bit.ly/BandwaGon) |
| 40G KVM | 3 核 | 2 GB | 40 GB | 2 TB | 1 Gbps | $52.99/半年 | [ 查看 40G Basic](https://bit.ly/BandwaGon) |
| 80G KVM | 4 核 | 4 GB | 80 GB | 3 TB | 1 Gbps | $19.99/月起 | [ 查看 80G Basic](https://bit.ly/BandwaGon) |
| 160G KVM | 5 核 | 8 GB | 160 GB | 4 TB | 1 Gbps | $39.99/月起 | [ 查看 160G Basic](https://bit.ly/BandwaGon) |
| 320G KVM | 6 核 | 16 GB | 320 GB | 5 TB | 1 Gbps | $79.99/月起 | [ 查看 320G Basic](https://bit.ly/BandwaGon) |
| 480G KVM | 7 核 | 24 GB | 480 GB | 6 TB | 1 Gbps | $119.99/月起 | [ 查看 480G Basic](https://bit.ly/BandwaGon) |

Basic 20G 是 The Amsterdam Plan 最直接的替代品。它的 CPU、内存、硬盘和流量接近，但网络侧重点不同，价格也略高。

### E-Commerce VPS

E-Commerce 系列面向需要更好国际互联和中国方向网络质量的用户。官网公开的配置从 20 GB 到 1 TB，端口速率最高可到 10 Gbps。

| 套餐 | CPU | 内存 | SSD | 月流量 | 端口 | 公开价格 | 购买 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| 20G E-Commerce | 2 核 | 1 GB | 20 GB | 1 TB | 2.5 Gbps | $49.99/季 | [ 查看 E-Commerce 20G](https://bit.ly/BandwaGon) |
| 40G E-Commerce | 3 核 | 2 GB | 40 GB | 2 TB | 2.5 Gbps | $89.99/季 | [ 查看 E-Commerce 40G](https://bit.ly/BandwaGon) |
| 80G E-Commerce | 4 核 | 4 GB | 80 GB | 3 TB | 2.5 Gbps | $56.99/月 | [ 查看 E-Commerce 80G](https://bit.ly/BandwaGon) |
| 160G E-Commerce | 6 核 | 8 GB | 160 GB | 5 TB | 5 Gbps | $86.99/月 | [ 查看 E-Commerce 160G](https://bit.ly/BandwaGon) |
| 320G E-Commerce | 8 核 | 16 GB | 320 GB | 8 TB | 5 Gbps | $159.99/月 | [ 查看 E-Commerce 320G](https://bit.ly/BandwaGon) |
| 640G E-Commerce | 10 核 | 32 GB | 640 GB | 10 TB | 10 Gbps | $289.99/月 | [ 查看 E-Commerce 640G](https://bit.ly/BandwaGon) |
| 1TB E-Commerce | 12 核 | 64 GB | 1 TB | 12 TB | 10 Gbps | $549.99/月 | [ 查看 E-Commerce 1TB](https://bit.ly/BandwaGon) |
| 1TB E-Commerce | 12 核 | 64 GB | 1 TB | 15 TB | 10 Gbps | $679/月 | [ 查看 E-Commerce 15TB](https://bit.ly/BandwaGon) |
| 1TB E-Commerce | 12 核 | 64 GB | 1 TB | 20 TB | 10 Gbps | $899/月 | [ 查看 E-Commerce 20TB](https://bit.ly/BandwaGon) |

与 The Amsterdam Plan 相比，E-Commerce 20G 的资源配置相近，但价格明显更高。它适合对跨境网络和机房迁移更看重的用户，不适合只想用最低预算运行个人服务的人。

### E-Commerce+SLA VPS

E-Commerce+SLA 目前主要提供美国洛杉矶 USCA_5 机房。官网说明该系列提供 99.99% SLA，但这项 SLA 并非所有机房都适用，目前公开说明中只有 USCA_5 支持该承诺。

| 套餐 | CPU | 内存 | SSD | 月流量 | 端口 | 价格 | 购买 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| 20G SLA | 2 核 | 1 GB ECC | 20 GB NVMe | 1 TB | 2.5 Gbps | $65.89/季 | [ 查看 SLA 20G](https://bit.ly/BandwaGon) |
| 40G SLA | 3 核 | 2 GB | 40 GB | 2 TB | 2.5 Gbps | $116.99/季 | [ 查看 SLA 40G](https://bit.ly/BandwaGon) |
| 80G SLA | 4 核 | 4 GB | 80 GB | 3 TB | 2.5 Gbps | $69.99/月 | [ 查看 SLA 80G](https://bit.ly/BandwaGon) |
| 160G SLA | 6 核 | 8 GB | 160 GB | 5 TB | 5 Gbps | $109.99/月 | [ 查看 SLA 160G](https://bit.ly/BandwaGon) |
| 320G SLA | 8 核 | 16 GB | 320 GB | 8 TB | 5 Gbps | $199.99/月 | [ 查看 SLA 320G](https://bit.ly/BandwaGon) |
| 640G SLA | 10 核 | 32 GB | 640 GB | 10 TB | 10 Gbps | $369.99/月 | [ 查看 SLA 640G](https://bit.ly/BandwaGon) |
| 1TB SLA | 12 核 | 64 GB | 1 TB | 12 TB | 10 Gbps | $699.99/月 | [ 查看 SLA 1TB](https://bit.ly/BandwaGon) |

SLA 方案面向对业务连续性有明确要求的团队或企业。个人博客和测试项目通常没有必要为 99.99% SLA 支付额外费用。

### Ultra VPS

Ultra VPS 目前集中在香港、日本、大阪和新加坡等面向中国大陆的低延迟区域。官网公开配置从 40 GB 到 1 TB，网络和机房定位明显高于普通 Basic。

| 套餐 | CPU | 内存 | SSD | 月流量 | 端口 | 价格 | 购买 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | --- |
| 40G Ultra | 2 核 | 2 GB | 40 GB | 500 GB | 1.5 Gbps | $49.99/月 | [ 查看 Ultra 40G](https://bit.ly/BandwaGon) |
| 80G Ultra | 4 核 | 4 GB | 80 GB | 1 TB | 1.5 Gbps | $86.99/月 | [ 查看 Ultra 80G](https://bit.ly/BandwaGon) |
| 160G Ultra | 6 核 | 8 GB | 160 GB | 2 TB | 2.5 Gbps | $165.99/月 | [ 查看 Ultra 160G](https://bit.ly/BandwaGon) |
| 320G Ultra | 8 核 | 16 GB | 320 GB | 4 TB | 2.5 Gbps | $329.99/月 | [ 查看 Ultra 320G](https://bit.ly/BandwaGon) |
| 640G Ultra | 10 核 | 32 GB | 640 GB | 6 TB | 5 Gbps | $549.99/月 | [ 查看 Ultra 640G](https://bit.ly/BandwaGon) |
| 1TB Ultra | 12 核 | 64 GB | 1 TB | 8 TB | 5 Gbps | $1,059.99/月 | [ 查看 Ultra 1TB](https://bit.ly/BandwaGon) |

Ultra 方案的优势是更靠近亚洲用户和高级网络，但价格已经不是 The Amsterdam Plan 的竞争范围。

## 购买 The Amsterdam Plan 前要注意什么

### 1. 库存可能随时变化

The Amsterdam Plan 的官方描述包含“Limited availability”，说明它不是长期保证供应的标准套餐。近期补货信息显示，该产品曾以 $39/年重新出现，但限量方案的库存、产品 ID 和可选机房都可能变化。

如果购买页面没有显示该产品，不建议用普通 Basic 套餐页面替代。那两个产品的机房和网络定位并不完全相同。

### 2. 这是自管 VPS

BandwagonHost 官方说明其 VPS 使用 KiwiVM 控制面板，支持开关机、重装系统、紧急控制台、rDNS、机房迁移、快照、用量统计和 API 等功能。但“自管”意味着用户需要自己维护服务器，官方不会替你安装应用或处理系统内部配置。

至少需要具备以下基础能力：

- 使用 SSH 登录服务器
- 配置 SSH 密钥和防火墙
- 更新 Linux 系统
- 设置 Nginx 或 Caddy
- 配置域名和 HTTPS
- 查看 CPU、内存和磁盘占用
- 处理服务崩溃和日志问题

如果只想购买后直接使用、并且不愿意维护 Linux 环境，The Amsterdam Plan 并不适合。

### 3. CPU 资源不是无限使用

BandwagonHost 的服务条款对部分限量套餐设置了 CPU 使用限制。条款中列出 The Amsterdam Plan 的 CPU 限制为 **1 个核心的 30%**；当 VPS 的小时平均使用量超过限制时，系统会自动限制可用 CPU 周期。

这也是它能维持低价的重要原因之一。对静态博客、代理转发、监控和轻量 API 来说通常够用，但不适合持续编译、视频转码、批量爬取或高并发计算。

## The Amsterdam Plan 适合哪些人

它更适合以下用户：

- 想低成本测试阿姆斯特丹节点
- 需要欧洲 IPv4 的个人项目
- 想搭建低流量博客或展示站
- 需要运行轻量级网络服务
- 熟悉 Linux，能够自行维护服务器
- 希望尝试中国方向优化线路，但预算有限

以下情况不建议优先选择：

- 需要大量内存或持续计算能力
- 需要官方托管运维
- 需要固定 99.99% SLA
- 主要服务中国大陆用户且要求极低延迟
- 需要稳定库存和长期可购买的标准套餐
- 准备运行大型数据库或多个重型容器

## 最终判断：$39/年值得买吗？

如果你的目标是购买一台便宜的阿姆斯特丹 VPS，The Amsterdam Plan 的价格确实很有吸引力。1 核、1 GB 内存、20 GB SSD 和 1 TB 月流量足够覆盖不少个人项目，2.5 Gbps 端口也比普通入门 VPS 的 1 Gbps 更高。

但它的价值主要来自三个条件：

1. 你确实需要阿姆斯特丹节点；
2. 你的应用属于轻量负载；
3. 你能接受自主管理和限量库存。

如果只是想要最便宜的 VPS，Basic 20G 可能更容易买到；如果想要中国大陆低延迟，香港、日本或新加坡的 Ultra 方案更直接；如果需要业务级稳定性，则应考虑 E-Commerce+SLA。

The Amsterdam Plan 更像一台低价、特定线路和特定地区的工具型 VPS。用途匹配时，$39/年的成本很低；用途不匹配时，再便宜的套餐也只是把问题延后一年。

👉 [进入搬瓦工 The Amsterdam Plan 购买页面](https://bandwagonhost.com/aff.php?aff=74518&pid=159)
