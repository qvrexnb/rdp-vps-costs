# RDP VPS: What It Costs, How Much RAM You Need, and Where the Windows License Fee Hides (All Plans Compared)

Entry-level Windows RDP VPS plans cluster between $6 and $9 a month. LightNode publishes $7.71/month for 1 vCPU and 2 GB RAM; Infrawire charges €8.30/month for 2 cores and 4 GB. Everything above that band buys more RAM, a bundled Windows license, or US hardware on a 1 Gbps port. Three things decide what you actually pay: the spec you need, the costs the price tag leaves out, and how far the data center is from you.

> **Quick pick:** if you want a US box with headroom rather than a $7 desktop, SpinServers lists its 8 vCPU / 8 GB / 160 GB RAID-10 plan from **$45.00/month**, with 10 TB of monthly traffic, a 1 Gbps port and one IPv4 plus one IPv6 address. 👉 [See SpinServers' current VPS plans and pricing](https://bit.ly/Spinservers)

## What an RDP VPS is, and why not just put xrdp on Linux

RDP is Microsoft's Remote Desktop Protocol. Windows Server and the Pro/Enterprise editions of Windows ship with a full RDP server already installed, so a "Windows RDP VPS" is a Windows machine with a desktop, an administrator account, and port 3389 listening.

Linux can serve RDP too, through third-party software such as xrdp. That route works, and it saves money, but you end up maintaining a translation layer on an OS that was never built around the protocol, and every Windows-only application stays out of reach. If the reason you want a remote desktop is a Windows program, buy Windows.

Clients are free on every platform: `mstsc` on Windows, Microsoft's Windows App on macOS, iOS and Android, Remmina or FreeRDP on Linux.

## SpinServers' VPS lineup, every plan on the page

SpinServers operates data centers in San Jose, California and Dallas, Texas, and its catalog is centered on dedicated servers and private cloud. The VPS line is a smaller set of fixed KVM configurations sold as Simple and Advanced Application Servers. Every plan carries a 1 Gbps port, RAID-10 SSD storage, one IPv4 and one IPv6 address, and monthly traffic counted per tier.

| Plan (vCPU · RAM) | Storage | Traffic / port | Price (USD) | Order |
| --- | --- | --- | --- | --- |
| 2 vCPU · 2 GB DDR4 | 40 GB RAID-10 SSD | 4 TB · 1 Gbps | Not printed on the page | [Check the 2 vCPU plan](https://bit.ly/Spinservers) |
| 4 vCPU · 4 GB DDR4 | 80 GB RAID-10 SSD | 8 TB · 1 Gbps | Not printed on the page | [Check the 4 vCPU plan](https://bit.ly/Spinservers) |
| 6 vCPU · 8 GB DDR4 | 120 GB RAID-10 SSD | 8 TB · 1 Gbps | Not printed on the page | [Check the 6 vCPU plan](https://bit.ly/Spinservers) |
| 8 vCPU · 8 GB DDR4 | 160 GB RAID-10 SSD | 10 TB · 1 Gbps | **from $45.00/month** | [Check the 8 vCPU plan](https://bit.ly/Spinservers) |
| 12 vCPU · 12 GB DDR4 | 160 GB RAID-10 SSD | 10 TB · 1 Gbps | Not printed on the page | [Check the 12 vCPU plan](https://bit.ly/Spinservers) |
| 16 vCPU · 16 GB DDR4 | 320 GB RAID-10 SSD | 15 TB · 1 Gbps | Not printed on the page | [Check the 16 vCPU plan](https://bit.ly/Spinservers) |
| 32 vCPU · 32 GB (Advanced) | 500 GB SSD | 20 TB · 1 Gbps | Not printed on the page | [Check the 32 vCPU plan](https://bit.ly/Spinservers) |

Three details from the same page matter more than the spec sheet:

- **Port 25 is closed by default** on every VPS. You can request it open via ticket with a justification, and the request can be refused. If part of your plan involves sending mail from the box, that's a support conversation, not a configuration toggle.
- **The 8 vCPU / 8 GB tier is the only one with a public price.** The rest are quoted at checkout, so the per-plan links above are where you get a real number rather than my guess.
- **Configurations are fixed steps.** SpinServers' custom-build option lives in the dedicated server line, not in VPS.

Windows deserves its own note. SpinServers' published licensing model for Windows servers is BYOL, bring your own license: you supply the Windows license and the monthly price doesn't include a license fee. Their Windows documentation covers Windows 10 and Windows Server 2008 through 2019, which is dated material, and it was written around dedicated servers. Before ordering a VPS for remote desktop use, ask support two questions in writing: which Windows images the VPS line supports, and whether you supply the license or they do. If you already hold Windows Server licensing through work or a volume agreement, BYOL is the cheapest structure available anywhere. If you don't, price a license before you compare monthly totals. 👉 [See SpinServers' current VPS plans and pricing](https://bit.ly/Spinservers)

## The four costs that aren't in the price tag

**1. The Windows license itself.** A widely circulated third-party buying guide states that many Windows VPS providers add $10 to $20 per month for the Windows license on top of the plan price. That's $120 to $240 in year one, and it's frequently missing from the headline number on a pricing page. Ask whether the quoted price includes Windows, and which edition.

**2. Windows 10 is out of support.** Microsoft ended support for Windows 10 on 14 October 2025, a date Infrawire prints on its own Windows 10 RDP page while still selling that image for compatibility reasons. If a provider's default image is Windows 10, ask whether Server 2022 or 2025 is available and what breaks if you switch.

**3. Fixed configurations.** HOSTKEY states plainly that its instant Windows RDP VPS come in a set configuration, and custom builds require a dedicated server instead. Many buyers assume they can dial in 3 GB of RAM or a 90 GB disk. Check the step sizes before you plan around a configuration that doesn't exist.

**4. Uptime wording.** LightNode, Infrawire and HOSTKEY all advertise 99.9%. RDP.net advertises 99%, with the remaining 1% reserved for maintenance and upgrades. At 99%, a month allows roughly seven hours offline. Fine for a hobby desktop, less fine for a machine running a trading terminal or an automation job that has to stay up.

## How much RAM does an RDP VPS need?

2 GB is the floor for Windows. Below that, Windows Server won't install usefully, so the 512 MB and 1 GB tiers you see advertised are Linux-only in practice.

- **2 GB:** one browser with a handful of tabs, or a single trading terminal, or remote access to a lightweight Windows application. Workable, not comfortable.
- **4 GB:** a browser plus one or two resident programs, which is where most people actually land.
- **8 GB and up:** several always-on applications, browser automation, builds, or anything you'd notice a stall on.

Price checkpoints on that ladder: LightNode's 8 GB / 4 vCPU tier is $27.70/month, and Infrawire's 16 GB / 8-core Silver plan is €27.60/month. Per gigabyte, the mid tiers are far cheaper than the entry tier, so buying the smallest plan and upgrading in three months usually costs more than starting one step up, unless your provider allows live upgrades without a reinstall (HOSTKEY and Infrawire both say they do).

## When it won't connect, or feels slow

Work through these in order before opening a support ticket.

1. **Confirm the address and port.** Default RDP port is 3389. If your provider gave you a non-standard port, the field takes `IP:port`, not the IP alone.
2. **Check the firewall.** Port 3389 needs an inbound rule. A wrong rule is the most common cause of a connection that worked yesterday.
3. **Reboot from the control panel.** A hung Windows session often accepts a reboot before it accepts a login.
4. **If RDP was never enabled**, log in through the provider's VNC or HTML5 console, open System Properties → Remote, tick "Allow remote connections to this computer", enable Network Level Authentication, then confirm the 3389 inbound rule in Windows Firewall. Retry `mstsc`.
5. **If it connects but stutters**, drop the color depth and turn off wallpaper and visual effects in the Experience tab of the client. This buys a surprising amount on a distant server.

Step 5 has a hard ceiling. The fix that actually works is a data center closer to you: a Paris or Frankfurt node for Europe, Los Angeles or Chicago for the US west and midwest, London or Amsterdam for the UK and Benelux. No amount of client tuning beats geography.

## What the $6 to $9 entry tier actually buys

For reference, without steering you anywhere:

| Provider | Entry price | Entry spec | Uptime claim | Delivery |
| --- | --- | --- | --- | --- |
| LightNode | $7.71/mo | 1 vCPU, 2 GB, 50 GB NVMe, 1 TB traffic | 99.9% | 1–2 minutes |
| Infrawire | €8.30/mo | 2 cores, 4 GB DDR4, 40 GB NVMe, 2.5 Gbps, unlimited traffic | 99.9% | about 5 minutes |
| RDP.net | not published | private RDP, no shared server | 99% | under 5 minutes |

Infrawire publishes a 7-day money-back guarantee and deploys from Paris or Frankfurt. RDP.net lists Los Angeles, Chicago, London and Amsterdam. Neither figure includes a Windows license question answered, so ask it in both cases.

## Which plan fits your case

- **One terminal or one browser, lowest spend:** the $6 to $9 entry tier is enough, and paying more buys nothing you'll feel.
- **Several resident programs, or automation that must stay up:** 8 GB. SpinServers' 8 vCPU / 8 GB plan at $45/month is priced for that job, and its 10 TB traffic allowance is far above what a desktop workload consumes.
- **US users who want IPv6, a 1 Gbps port and RAID-10 storage:** SpinServers is built for this, and the fixed tiers make the choice simple.
- **European latency priority:** pick a Paris, Frankfurt, London or Amsterdam node and skip the US entirely.

## Two questions to settle before you pay

Whether the monthly price includes a Windows license, and which Windows version ships. Then the renewal price and the refund window. Infrawire states 7 days in writing; SpinServers' VPS page doesn't publish a refund period, so get it confirmed by support before you enter card details rather than after.

If the answers suit you and you need a US KVM box with real memory and a 1 Gbps port, the 8 vCPU tier is the one with a published price and the least guesswork. 👉 [Check SpinServers' current VPS plans and pricing](https://bit.ly/Spinservers)
