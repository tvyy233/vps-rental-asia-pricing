# virtual server rental: how to choose an Asia-facing VPS, what $29–$999 actually buys, and the billing details to check first

Renting a virtual server is cheap until you need it to be reachable from mainland China at 9pm. A 2 vCPU / 4GB box costs €12 a month on a European host and $29–$59 a month on a China-optimised one, and the gap is almost entirely routing, not hardware. GoMami is firmly in the second camp: entry plans at $29/month, flagship dedicated hardware at $999/month, and a documented 24-hour refund window that only applies once.

> **Quick pick**
> Start with JPN Pulse Nano: 2 vCPU / 2GB / 40GB NVMe / 500GB traffic / 1Gbps for **$29/month**. It handles a few light sites, a reverse proxy or a jump box. If your visitors sit in Hong Kong and southern China, HKG Pulse Mini (2 cores / 4GB / 60GB / 1TB) at $59/month has the shorter round trip. No China audience at all? Then this pricing is mostly wasted on you — the comparison section below explains why.
> 👉 [Open the JPN Pulse Nano configuration page](https://gomami.io/aff.php?aff=415&pid=13)

## What you are paying for when you rent a virtual server

You are paying for three separate things: compute, network path, and what happens when something breaks. The first is transparent. The second is what separates a €4 plan from a $59 plan. The third is where most buyers forget to look.

Xserver publishes its cost structure openly through a configurator: €2/month per 3.0GHz core, RAM from €1/GB/month, SSD from €1 per 10GB. Run those numbers and a €4 Promo plan can only be 1 core, 1GB RAM, 10GB SSD. That is a genuine price-per-kilogram offer, and for a static site with European visitors it is the right answer.

GoMami's entry plan is 2 vCPU / 4GB / 40GB NVMe for $29–$49. The extra money bought no extra cores. It bought return routing: China Telecom CN2, China Unicom AS9929, China Mobile CMIN2, with the company claiming mainland RTT under 50ms. On an ordinary international route, evening peak latency from China commonly runs past 200ms and comes with packet loss. If you only SSH in to push code, you will not notice. If you run a store, an API gateway or a game server, that difference decides whether the thing works.

One caveat on the DDoS headline. Default protection is best-effort; the 600 Gbps scrubbing capacity is an optional upgrade. A $29 Nano does not come with 600 Gbps of anything.

## GoMami's full VPS lineup and prices

Four store lines are currently on sale, split by location and CPU platform. Every plan below is monthly billing in USD, and every plan includes one IPv4 address on CN2 / AS9929 / CMIN2 return routing.

| Plan | vCPU / RAM / NVMe | Monthly traffic / port | Price | Order |
| --- | --- | --- | --- | --- |
| HKG Turin Mini (EPYC 9575F) | 2 / 4GB / 100GB | 1TB / 2Gbps | $69 | [Check Turin Mini](https://gomami.io/aff.php?aff=415&pid=14) |
| HKG Turin Air | 4 / 8GB / 140GB | 2TB / 2Gbps | $129 | [See the Hong Kong Turin line](https://bit.ly/Gomami) |
| HKG Turin Pro | 6 / 16GB / 180GB | 5TB / 5Gbps | $299 | [See the Hong Kong Turin line](https://bit.ly/Gomami) |
| HKG Turin Ultra | 12 / 32GB / 220GB | 10TB / 5Gbps | $599 | [Check Turin Ultra](https://gomami.io/aff.php?aff=415&pid=22) |
| HKG Pulse Nano (EPYC 7763) | 2 / 2GB / 40GB | 500GB / 1Gbps | $49 | [Check HKG Pulse Nano](https://gomami.io/aff.php?aff=415&pid=26) |
| HKG Pulse Mini | 2 / 4GB / 60GB | 1TB / 1Gbps | $59 | [See the Hong Kong Pulse line](https://bit.ly/Gomami) |
| HKG Pulse Air | 4 / 8GB / 80GB | 2TB / 1Gbps | $119 | [See the Hong Kong Pulse line](https://bit.ly/Gomami) |
| HKG Pulse Pro | 8 / 16GB / 100GB | 5TB / 3Gbps | $269 | [See the Hong Kong Pulse line](https://bit.ly/Gomami) |
| HKG Pulse Ultra | 16 / 32GB / 300GB | 10TB / 3Gbps | $499 | [Check HKG Pulse Ultra](https://gomami.io/aff.php?aff=415&pid=25) |
| JPN Pulse Nano (EPYC 7773X) | 2 / 2GB / 40GB | 500GB / 1Gbps | $29 | [Check JPN Pulse Nano](https://gomami.io/aff.php?aff=415&pid=13) |
| JPN Pulse Mini | 2 / 4GB / 60GB | 1TB / 1.5Gbps | $49 | [Check JPN Pulse Mini](https://gomami.io/aff.php?aff=415&pid=10) |
| JPN Pulse Air | 4 / 8GB / 80GB | 2TB / 1Gbps | $89 | [Check JPN Pulse Air](https://gomami.io/aff.php?aff=415&pid=11) |
| JPN Pulse Pro | 8 / 16GB / 100GB | 5TB / 3Gbps | $169 | [Check JPN Pulse Pro](https://gomami.io/aff.php?aff=415&pid=12) |
| JPN Pulse Ultra | 12 / 32GB / 300GB | 10TB / 3Gbps | $338 | [Check JPN Pulse Ultra](https://gomami.io/aff.php?aff=415&pid=24) |
| SIN Pulse Nano (EPYC 7663) | 2 / 2GB / 40GB | 500GB / 1Gbps | $29 | [Check SIN Pulse Nano](https://gomami.io/aff.php?aff=415&pid=21) |
| SIN Pulse Mini | 2 / 4GB / 60GB | 1TB / 1Gbps | $49 | [See the Singapore line](https://bit.ly/Gomami) |
| SIN Pulse Air | 4 / 8GB / 80GB | 2TB / 1Gbps | $89 | [See the Singapore line](https://bit.ly/Gomami) |
| SIN Pulse Pro | 8 / 16GB / 100GB | 5TB / 3Gbps | $169 | [See the Singapore line](https://bit.ly/Gomami) |
| SIN Pulse Ultra | 12 / 32GB / 300GB | 10TB / 5Gbps | $338 | [Check SIN Pulse Ultra](https://gomami.io/aff.php?aff=415&pid=23) |
| LAX Pulse Nano (EPYC 7K62) | 2 / 2GB / 40GB | 1TB / 1Gbps | $29 | [Check LAX Pulse Nano](https://gomami.io/aff.php?aff=415&pid=27) |
| LAX Pulse Mini | 2 / 4GB / 60GB | 2TB / 1Gbps | $59 | [Check LAX Pulse Mini](https://gomami.io/aff.php?aff=415&pid=28) |
| LAX Pulse Air | 4 / 8GB / 80GB | 4TB / 2Gbps | $129 | [Check LAX Pulse Air](https://gomami.io/aff.php?aff=415&pid=29) |
| LAX Pulse Pro | 6 / 16GB / 100GB | 8TB / 3Gbps | $259 | [Check LAX Pulse Pro](https://gomami.io/aff.php?aff=415&pid=30) |
| LAX Pulse Ultra | 12 / 32GB / 300GB | 15TB / 5Gbps | $599 | [Check LAX Pulse Ultra](https://gomami.io/aff.php?aff=415&pid=31) |
| LAX Pulse Titan | 12 / 32GB / 600GB | 30TB / 10Gbps | $999 | [Check LAX Pulse Titan](https://gomami.io/aff.php?aff=415&pid=32) |

Hong Kong Pulse and the Japan/Singapore lines are not the same product at different prices. A Nano in Hong Kong costs $49; the identical tier in Tokyo or Singapore costs $29. You are paying $20 a month for geography, full stop. Hong Kong also runs a separate Turin series on EPYC 9575F (Zen 5, up to 5GHz), which is the newer silicon and priced accordingly.

Three details that change the decision:

- **Japan's return path runs through Hong Kong**, so single-thread throughput is a little weaker than a Hong Kong node. If your users are in northern China the difference narrows; if they are in Guangdong, Hong Kong is the safer pick.
- **Singapore matches Japan on price but not on port speed.** SIN Pulse Ultra gets 5Gbps where the Japan Ultra gets 3Gbps, making it the cheapest way into a wide pipe in this lineup.
- **Los Angeles bills outbound traffic only**, according to the launch article covering that line. Inbound traffic is not counted against the monthly allowance, which effectively doubles capacity for download mirrors and media distribution. That figure comes from a third-party write-up of the launch, not from a published pricing page, so confirm it at checkout before you build a business on it.

The homepage also showcases two other groups that do not line up cleanly with the store listing: a **Ryzen 9 9950X** line (Mini 2 cores / 4GB / 40GB / 1000GB / 2Gbps VirtIO at $59; Air 4 / 8GB / 60GB / 2000GB / 2Gbps at $99; Pro 6 / 16GB / 80GB / 5000GB / 5Gbps at $199) and a second **EPYC 7763** group at $39 / $79 / $169. The Ryzen line is the one to look at if single-core clock matters more than bandwidth — game servers, compile jobs, anything latency-sensitive per thread. The $39 EPYC figure conflicts with the $49 HKG Pulse Nano carrying near-identical specs, so treat the display price as indicative and read the configure page before paying.

Bare metal sits under the same product menu and is easy to confuse with VPS. HKG Forge uses EPYC 7663 at 56 cores / 112 threads: the Mini tier offers 128GB RAM / 960GB NVMe / 10TB traffic at 2Gbps for **$599 plus a $68 setup fee**, and the Air tier 256GB / 4TB / 20TB at 2Gbps for **$899 plus $68**. Overage runs $0.06/GB, extra IPv4 addresses are $10 each with a maximum of four per machine, and provisioning is automatic after payment.

## Traffic, refunds and the billing terms that decide the deal

These are the terms that cost people money, and GoMami publishes them in more detail than most hosts its size.

**Traffic packs expire with the billing cycle.** If a plan runs dry mid-month you can buy more without upgrading: 100GB for $6, 500GB for $30, 1TB for $60, 2TB for $120, 5TB for $300, 10TB for $600, 20TB for $1,200. The rate is a flat $0.06/GB at every size, so there is no bulk discount. Purchased traffic is valid only for the current billing cycle and does not roll over to the next month. GoMami's own advice is to upgrade the plan if you keep needing more. What the public pages still do not say is whether exceeding your allowance throttles, suspends or auto-bills — the FAQ lists the question without an answer.

**The refund window is 24 hours, once.** New instances can be cancelled for a full refund within 24 hours of activation, returned to the original payment method, limited to one claim per user and to first purchases only. Renewals are excluded, as are accounts terminated for terms violations, spent account credit and IPs blackholed by DDoS attacks. Alipay refunds land in 1–3 business days, cards in 5–10, crypto in 1–3. A successful refund deletes the instance and its data immediately, so back up first. If you simply do not want to renew, the path is Services > My Services > Request Cancellation, with Immediate or End of Term as the option.

Twenty-four hours is a short trial. It is enough to run a latency test from your actual users and confirm the route behaves, and not much more. Xserver, by contrast, offers a 7-day money-back guarantee.

**The promo code field is on the Review & Checkout page**, after the configure step and after you add the cart. People hunting for it on the plan configuration screen find nothing and pay full price. Payment options there are account credit applied against the order, or Credit Card / Stripe Alipay / Crypto.

Two codes circulate in third-party write-ups: `GOMAMI365`, reported as a recurring 20% discount on annual billing, and `Hi,LAX`, a recurring 20% launch discount on the Los Angeles line that brings the $29 Nano down to $23.20. Neither has a published expiry date on GoMami's own pages, and neither is confirmed by the official price list, so test them in that checkout field before you rely on the figure.

👉 [Test whether the annual discount still applies in the cart](https://bit.ly/Gomami)

## The real annual cost, month by month

On JPN Pulse Nano, monthly billing runs $348 a year. If the reported 20% annual code holds, the same plan works out at $23.20/month, or $278.40 for the year — a saving of $69.60, roughly $5.80 per month.

Over two years the gap between $696 and $556.80 is $139.20, close to five months of Nano service. That is a real number and a modest one. Against it sits the fact that the money leaves your account up front, and the refund window on any renewal or second purchase is zero.

The rule that follows is dull but correct. If the project is already running and you know you will keep it for a year, annual billing is free money. If it is your first time on this network and you are still testing whether the route holds up from your users' locations, pay monthly for one cycle, measure, then commit. Saving $5.80 a month does not justify gambling a full year.

👉 [Start with one month on a Tokyo or Singapore Nano](https://gomami.io/aff.php?aff=415&pid=13)

## How this compares with cheaper general-purpose VPS

If nothing you serve touches China, GoMami's premium buys you latency improvements nobody will feel. Three general-purpose providers cover that ground more cheaply. All figures below come from their current public pricing; none of them appear here with a link.

| Provider | Representative plan | Monthly | Location | Billing notes |
| --- | --- | --- | --- | --- |
| Xserver | 1 core 3.0GHz / 1GB / 10GB SSD | €4 (Promo) | US and Europe (Ukraine, Poland, Bulgaria, Netherlands) | VMware, unmetered 100/1000 Mbps port, 7-day money-back |
| Xserver | 2 cores / 4GB / 40GB | €12 (Duo) | Same | Resources resizable while running, no downtime |
| KernelHost | 1 EPYC core / 2GB / 30GB NVMe | €9.99 (VPS-1) | Frankfurt, TÜV TIER3+ | KVM single-tenant, 100% prepaid, no minimum term, traffic throttled to 10 Mbps rather than suspended |
| KernelHost | 8 EPYC cores / 32GB / 200GB NVMe | €49.99 (VPS-8) | Same | 2×1Gbps uplink, 3 backup slots, 3.2 Tbps Arbor filtering, 99.99% SLA |
| A Moscow-based host | 1 Ryzen 7 5800X core / 4GB / 45GB NVMe | $11.15 | Moscow, Tier III | 250 Mbps port, 99.9% SLA, ~120s provisioning, billed in RUB |
| GoMami | 2 vCPU / 2GB / 40GB NVMe | $29 | Tokyo, Singapore, Los Angeles | China-optimised return routing, 1Gbps, extra traffic $0.06/GB |

Two things stand out.

The price gap has a precise location. Xserver's €12 Duo tier is 2 cores, 4GB and 40GB — the same shape as a $29 GoMami Nano, at roughly a third of the cost. That multiple is the routing fee. Whether it is worth paying depends entirely on where your visitors are.

The policy transparency runs the other way in places. Xserver spells out its overdue timeline: network off on day 2 with data retained, archive on day 9, and day 23 as the last day recovery from the account is guaranteed. KernelHost states that once fair-use traffic runs out, speed drops to 10 Mbps until the cycle ends and the server stays online with no surcharge. GoMami answers neither question in public, so ask support before you commit to anything that cannot be interrupted.

## Who should rent this, and who should not

This lineup is worth the money when the people using the server sit in mainland China and you have already lost patience with evening peak jitter: cross-border storefronts, API relays, remote-work gateways, game servers where per-thread speed matters. It is also the right call if you want a China-optimised edge node and are willing to pay separately for the 600 Gbps scrubbing tier.

It is the wrong call in three common situations. If your audience is European or American, Xserver's €4–€36 tiers cost less and include a 7-day refund. If your budget is capped near $10 a month, KernelHost's €9.99 VPS-1 gives 2GB RAM and 30GB NVMe and throttles rather than stops when traffic runs out. If you need large cheap storage or genuinely unmetered bandwidth, eastern European and Russian facilities get there for around $11 — with the caveat that ruble billing and a 250 Mbps port come attached.

And if the whole project is a static blog with a global readership, none of this matters. $29 a month for 500GB of traffic and an optimised port is capacity your visitors will never feel.

## Questions that keep coming up before checkout

**How long until the server is live?** Payment triggers automatic deployment, typically completing within a few minutes, followed by an email containing the IP and login credentials.

**What happens if I exceed my traffic allowance?** Not stated publicly. The traffic packs at $0.06/GB are the documented remedy, and they expire at the end of the cycle. Anything relying on uninterrupted throughput should get a written answer from support first.

**Can I get a refund?** Yes, within 24 hours of activation, on a first purchase, once per user, with the instance and data deleted on approval. Renewals do not qualify.

**Can I try before buying?** The official FAQ lists this question and shows no answer. Other directories show no trial option either. Ask support.

**Can I buy IP transit, or get a team or non-profit discount?** Both appear as unanswered questions in the official FAQ. No published terms exist for either.

**Does it support Windows?** Third-party write-ups say the Pro and Ultra tiers on the Hong Kong Turin and Pulse lines support Windows, while entry tiers do not. GoMami has not confirmed this publicly, so verify before ordering if Windows is a requirement.

**Is there an API?** Yes. GoMami documents a RESTful API for managing accounts and servers programmatically.

**Nano or Mini for a first box?** Go by RAM. 2GB runs an LNMP stack and a handful of static sites; the moment Docker, a database and a cache all want to live there, 2GB stalls under concurrency or during a compile. The $20 jump to Mini buys 2GB more memory and 20GB more storage.

## Pick by situation

Serving users outside Asia, or running a static site: go to the €4–€15 bracket and skip this entirely.

Serving mainland China on a tight budget: JPN Pulse Nano at $29/month, 2 cores / 2GB / 40GB / 500GB. It is the only entry point in this lineup where the geographic premium stays small, and the Tokyo return path through Hong Kong is a fair trade for roughly 40% less than the Hong Kong Nano.

Serving mainland China with revenue attached: HKG Pulse Mini at $59/month, 2 cores / 4GB / 60GB / 1TB. The extra $30 over Japan buys Hong Kong landing and a shorter round trip, which is usually cheaper than bolting a CDN onto a Tokyo box.

Single-thread speed above all: the Ryzen 9 9950X line, 2 cores / 4GB / 40GB at $59/month with a 5.7GHz boost ceiling.

Two checks before you pay. Type the discount code into the checkout field and watch the total change rather than trusting the advertised percentage, and get the over-allowance behaviour in writing if downtime would cost you more than the plan does.

👉 [Open GoMami's plan selector and confirm live pricing](https://bit.ly/Gomami)
