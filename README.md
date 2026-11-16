# Best Unmanaged VPS: Why $5.95 Turns Into $7.99 at Renewal, What 99.9% Uptime Costs You, and How to Size the Box You Need

Across 329 ranked unmanaged plans, the median sign-up rate is $5.95/mo. Among the 41 hosts that publish a renewal rate, the median is $7.99/mo, and only 16 never raise the price. That spread sets what you pay in year two, and it matters more than the core count on the landing page.

Vultr makes a clean reference point because it publishes one monthly rate per plan and no renewal rate at all. $6.00/mo buys 1 vCPU, 1 GB RAM and 25 GB NVMe, in any of 32 locations, with no term to sign. Below: the plans, the renewal jumps worth walking away from, how to read an uptime SLA, and the support hours that never make it onto a pricing page.

> **The short answer:** Vultr High Performance AMD, 1 vCPU / 1 GB / 25 GB NVMe at $6.00/mo, billed monthly with no renewal step. It covers a single site, a small API, a VPN node or a staging box, and it's the cheapest route to NVMe plus a real choice of regions. New accounts can enter **FLY300VULTR** for $300 in credit. 👉 [Check the $6.00/mo plan and current pricing](https://www.vultr.com/pricing/?ref=9738262-9J)

## What Vultr charges across its VPS range

Vultr's VPS range runs from $6.00/mo to $216.00/mo across 16 plans, all billed monthly.

| Plan | vCPU / RAM / NVMe | Price | Billing | Order |
| --- | --- | --- | --- | --- |
| High Performance AMD, entry | 1 / 1 GB / 25 GB | $6.00/mo | Monthly, no renewal rate | [See the 1 GB plan](https://www.vultr.com/pricing/?ref=9738262-9J) |
| High Performance, largest standard VPS | 12 / 24 GB / — | $216.00/mo | Monthly, no renewal rate | [See the top VPS tier](https://www.vultr.com/pricing/?ref=9738262-9J) |

Those are the two ends of the range. The middle configurations carry the same monthly terms, and the live pricing page is the only place to confirm a specific combination on the day you buy.

A few things stay constant, and they matter more than the per-plan deltas:

| Item | Detail |
| --- | --- |
| Billing | One monthly rate per plan; no separate renewal price is published |
| Storage | NVMe on every plan |
| Bandwidth | Metered, with 2 TB included on the $6.00 plan |
| Regions | 32, from Atlanta and Silicon Valley to Amsterdam, Tokyo, Seoul and Sydney |
| Regional pricing | São Paulo costs roughly 50% more for the same plan |
| Ceiling | 24 GB RAM / 12 vCPU on standard VPS; GPUs (an L40S from $1.67/hr) and bare metal are separate product lines |

Two practical consequences. If your traffic comes mostly from Europe or Asia, you can put the box next to those users instead of defaulting to a US region and paying for the latency. If you're serving Brazil, price the São Paulo region before you commit, because the same plan is not the same number there.

## The renewal price decides year two

HostArmada's Spark plan is the clearest example of how a cheap first year works out. It runs $3.69/mo on a one-year term and renews at $8.20/mo, a 122% jump, for 1 vCPU and 1 GB. Year one costs $44. Years two and three cost $197. The three-year total is $241, and you're still on a 1 GB box.

Arsys goes further: $6.84/mo on a one-year term renewing at $18.24/mo, up 167%, or $520 across three years. Bluehost's NVMe 8 moves from $12.99 to $28.99 (+123%). DreamHost's Stack 4 starts at $8.99 on a three-month term and renews at $15.99 (+78%); if you want 2 vCPU, 4 GB and 75 GB NVMe, that's the price of getting it.

| Plan | Sign-up | Term | Renewal | Jump | 3-year cost |
| --- | --- | --- | --- | --- | --- |
| Arsys VPS 120GB | $6.84/mo | 1 year | $18.24/mo | +167% | $520 |
| Bluehost NVMe 8 | $12.99/mo | — | $28.99/mo | +123% | — |
| HostArmada Spark | $3.69/mo | 1 year | $8.20/mo | +122% | $241 |
| DreamHost Stack 4 | $8.99/mo | 3 months | $15.99/mo | +78% | — |
| Heart Internet Linux Lite | $10.73/mo | — | $11.91/mo | +11% | — |
| DigitalOcean Basic 1 GiB | $6.00/mo | Monthly | $6.00/mo | 0% | $216 |
| Vultr HP AMD 1 GB | $6.00/mo | Monthly | $6.00/mo | 0% | $216 |

The 3-year column is where the marketing breaks down. A $3.69 headline and a $6.00 headline look far apart until you run 36 months: $241 versus $216, and the $216 option lets you leave in any given month.

Vultr sits in the no-step-up group, which is why comparisons against a discounted host flip somewhere around month 12. DigitalOcean's Basic droplets behave the same way: $4/mo for 512 MiB, $6 for 1 GiB, $12 for 2 GiB with 1 vCPU, month to month, unchanged in year three. 👉 [Compare the $6.00 plan against the rest of Vultr's range](https://www.vultr.com/pricing/?ref=9738262-9J)

There's a second cost multiplier most people skip: the term. A two-year prepay at Time4VPS doubles at renewal, from $2.86 to $5.72 on the C2 plan, and from $200.98 to $401.96 on the 64 GB plan. On a 24-month term that's a long commitment to a price you haven't tested yet.

## Who actually does what on an unmanaged box

The split happens at the operating system. You get root and a blank disk; the provider keeps everything underneath.

- **You:** the OS and its updates, kernel and package patches, firewall rules, your app stack, monitoring and alerting, and your own backups unless you buy theirs.
- **Provider:** the physical host, RAID storage, dual power and network uplinks, the datacenter, and an SLA that covers power and network only.

That last line is worth reading twice. hosting.com runs a 99.9% hardware and network SLA on unmanaged VPS and 99.95%+ on managed, and the managed side adds OS and panel updates, monitoring, security patching, daily backups and proactive SRE support. On the unmanaged side you get root, your choice of Ubuntu 22.04, Debian 12 or AlmaLinux 9, and the ability to reinstall or switch distributions whenever you want. No one is watching your MySQL.

Uptime percentages hide the real difference until you convert them. 99.9% allows about 86 seconds of downtime a day, or 43 minutes a month. 99.99% allows about 9 seconds a day. 99.999% allows less than one second. The gap between a 99.9% and a 99.99% host is roughly 40 minutes of permitted outage every month, which is the difference between a blip and a lost afternoon.

None of that protects you from a misconfiguration, a full disk or a bad deploy, because those sit above the line the SLA covers. Liquid Web cites Pingdom's estimate of $9,000 lost per minute of downtime, and that figure is a reason to care about your own monitoring whether or not your host promises five nines.

## Support hours are part of the price

Contabo's support team answers 365 days a year from 8 am to 11 pm Germany time, and the company states plainly that it doesn't manage your VPS. Hostwinds goes further in the other direction: unmanaged plans get infrastructure-level support for power, connection and networking, with no technical, management or administrative help, while its managed VPS gets 24/7 coverage. One provider reviewed in Liquid Web's roundup offers support to standard and premium customers only during working hours.

A $5 box with 15 hours of ticket coverage and a $12 box with 24/7 coverage are different products, even when the specs match. If your server goes down at 2 am your time and support opens at 8 am Frankfurt time, you're the on-call engineer. Budget for that, or pick a host whose window overlaps your worst hours. Liquid Web's own unmanaged tier advertises a first response under a minute with 24/7 coverage, which is the other end of the spectrum.

## How the alternatives compare

No links here, just verified specs and terms to weigh against the plan you're considering.

| Provider | What you get | Billing | Stated SLA | Locations |
| --- | --- | --- | --- | --- |
| Contabo | Cloud VPS 16: 16 vCPU, 64 GB RAM, 500 GB SSD or 250 GB NVMe, 1 Gbit/s port, unlimited traffic, 2–3 snapshots | Discounted rate advertised for the first 24 months; check the post-term price on the order page | Not stated on the page reviewed | 9 regions, 11 locations |
| hosting.com | AMD EPYC, NVMe, full root, Ubuntu/Debian/AlmaLinux, scale individual resources without rebuild | Monthly | 99.9% hardware and network | 10 |
| Liquid Web | 2–16 vCPU, 2–16 GB RAM, 40–200 GB SSD, 10 TB bandwidth, InterWorx free (Plesk/cPanel extra), DDoS protection, up to 50 GB Acronis backups | Monthly | 100% network uptime, as claimed by the provider | Michigan, Arizona, Amsterdam |
| Hostwinds | 1–16 vCPU, 1–96 GB RAM, 30–750 GB storage, nightly backups, enterprise firewall, infrastructure-only support | Monthly | 99.9999%, as claimed by the provider | Multiple, unspecified |
| DigitalOcean | Basic droplets at 512 MiB/$4, 1 GiB/$6, 2 GiB with 1 vCPU/$12 | Monthly, no renewal jump | Not stated on the page reviewed | Multiple |

If you want to dial CPU and RAM independently for an odd workload, Kamatera sells configurable instances on hourly or monthly billing across 20+ locations, which helps when none of the fixed plans fit.

## Sizing rules that hold up

- **Static site, bot, VPN endpoint, staging box:** 1 vCPU / 1 GB / 25 GB. This is the $6.00 tier, and it's enough.
- **WordPress with page caching and a small database:** 1 vCPU / 2 GB is comfortable. 1 GB runs with swap, and you'll notice it during plugin updates.
- **Docker with Postgres, an app server and Redis on one host:** 2 vCPU / 4 GB. Anything less and the OOM killer becomes a recurring character.
- **JVM apps, Elasticsearch, game servers:** 8 GB and up, which pushes against Vultr's 24 GB / 12 vCPU ceiling on standard VPS. Past that, the answer is bare metal or a dedicated box, not a bigger VPS.
- **cPanel or a control panel with managed patching:** unmanaged is the wrong shelf. cPanel licenses cost extra at most providers (Liquid Web includes InterWorx free and charges monthly for Plesk and cPanel), and the panel doesn't patch your kernel for you.

Bandwidth belongs in the sizing decision too. Vultr meters it, starting at 2 TB on the cheapest plan. Contabo advertises unlimited traffic. If you're pushing large media or serving as a mirror, that difference outweighs a couple of CPU cores.

## Before you pay

1. **Confirm the credit landed.** Vultr's $300 offer runs through code FLY300VULTR and is limited to new customers, applies to select products, and can't be combined with other offers; the coupons page also lists $200, $250 and a deposit-match option. Check the Billing section before you deploy anything. 👉 [See the current Vultr credit terms](https://www.vultr.com/coupons/?ref=9738262-9J)
2. **Check the region's price and distance.** São Paulo costs about 50% more for the same plan. Pick the location nearest your users rather than the default.
3. **Check what's included in backups.** Contabo includes 2–3 snapshots, Liquid Web bundles up to 50 GB of Acronis backups, and hosting.com lists backups as optional on unmanaged VPS.
4. **Check the support window against your own hours,** not against the marketing copy.

For a single box that doesn't move in price, starts at $6.00 with NVMe, and lets you pick from 32 regions, Vultr's 1 GB plan is the place to start. Move to 2 or 4 GB when the swap file starts earning its keep. 👉 [Start on the 1 vCPU / 1 GB plan at $6.00/mo](https://www.vultr.com/pricing/?ref=9738262-9J)
