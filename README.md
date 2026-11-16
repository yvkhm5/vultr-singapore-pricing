# Vultr Singapore: Which Plan You Actually Need, What 9% GST Adds, and Why Those $62.45 "Vultr Singapore" Plans Aren't Vultr's Prices (Full Plan Table)

Singapore is one of Vultr's nine Asia-Pacific locations, part of a 32-city network, and it has been online since September 2016. Deploy there and the meter runs hourly, with 9% GST added to the invoice unless your account carries a GST ID. Worth settling first: the "$62.45/month Vultr Singapore" plans ranking in search are reseller listings. Vultr's own 1 GB plan lists at $5/month.

What follows is the plan table, the billing rules that decide your real monthly figure, the tax line most write-ups skip, and the one thing the Singapore location can't do for you.

> **Quick pick:** A Singapore IP for a small site, a cron box, or a VPN endpoint — Cloud Compute Regular Performance 1 GB at **$5/mo** (1 vCPU, 1 GB RAM, 25 GB SSD). Serving WordPress, Docker, or a small database where disk I/O shows — High Frequency 1 GB at **$6/mo** buys NVMe and a 3 GHz+ Xeon for one dollar more. 👉 [Check current Singapore pricing and start a 1 GB instance](https://www.vultr.com/pricing/?ref=9738262-9J)

## Vultr Singapore plans and prices

Nearly everyone lands on the shared-CPU Cloud Compute line first, so that's the table worth reading closely. Prices are Vultr's published list rates for these configurations; availability and the exact figure for the Singapore location are shown on the deploy screen before you confirm.

| Plan | vCPU · RAM · Storage | Hourly | Monthly | Deploy |
| --- | --- | --- | --- | --- |
| Regular Performance, IPv6-only | 1 vCPU · 0.5 GB · 10 GB SSD | $0.004 | $2.50 | [Start the 0.5 GB IPv6 plan](https://www.vultr.com/pricing/?ref=9738262-9J) |
| Regular Performance 0.5 GB | 1 vCPU · 0.5 GB · 10 GB SSD | $0.005 | $3.50 | [Start the 0.5 GB plan with IPv4](https://www.vultr.com/pricing/?ref=9738262-9J) |
| Regular Performance 1 GB | 1 vCPU · 1 GB · 25 GB SSD | $0.007 | $5 | [Start the 1 GB plan](https://www.vultr.com/pricing/?ref=9738262-9J) |
| Regular Performance 2 GB | 1 vCPU · 2 GB · 55 GB SSD | $0.015 | $10 | [Start the 2 GB plan](https://www.vultr.com/pricing/?ref=9738262-9J) |
| Regular Performance 2 vCPU / 2 GB | 2 vCPU · 2 GB · 65 GB SSD | — | $15 | [Start the 2 vCPU / 2 GB plan](https://www.vultr.com/pricing/?ref=9738262-9J) |
| Regular Performance 4 GB | 2 vCPU · 4 GB · 80 GB SSD | $0.030 | $20 | [Start the 4 GB plan](https://www.vultr.com/pricing/?ref=9738262-9J) |
| High Frequency 1 GB | 1 vCPU · 1 GB · 32 GB NVMe | $0.009 | $6 | [Start the High Frequency 1 GB plan](https://www.vultr.com/pricing/?ref=9738262-9J) |
| High Frequency 2 GB | 1 vCPU · 2 GB · 64 GB NVMe | — | $12 | [Start the High Frequency 2 GB plan](https://www.vultr.com/pricing/?ref=9738262-9J) |
| High Frequency 4 GB | 2 vCPU · 4 GB · 128 GB NVMe | $0.036 | $24 | [Start the High Frequency 4 GB plan](https://www.vultr.com/pricing/?ref=9738262-9J) |

Above this line sit Optimized Cloud Compute (CPU-, memory- and storage-optimized shapes) and the GPU and VX1 families, which run well past $2,000/month at the top end. Those are priced per configuration, per region, and the Singapore list doesn't carry every shape. If you need one, open the deploy screen, filter to Singapore, and read what's actually offered rather than planning around a catalogue page. 👉 [See the full plan list and per-hour rates](https://www.vultr.com/pricing/?ref=9738262-9J)

## What the Singapore location gives you, and where it stops

Vultr's launch note described Singapore as "strategically positioned for low latency in the APAC region," and that is the entire case for the location. How low the latency actually is depends on where your users sit and which network they arrive on, so measure it from your own connection instead of trusting a number from an article.

The harder boundary is redundancy. Vultr runs one facility in Singapore, and data center directories that track the company list a single Singapore entry. If your architecture assumes two availability zones in the same city, this location cannot deliver it. Surviving a Singapore outage means a second region (Tokyo or Seoul are the usual picks) and a plan for how traffic moves between them. That is more work than a second zone would be, and it is the honest cost of a single-location presence.

Compliance is better than you'd expect for the price. Third-party directories list ISO 27001, PCI DSS, SOC 1 Type 2 and SOC 2 Type 2 against the Singapore facility. Vultr doesn't surface that list on its own location page, and directories don't publish building size, colocation space, or power details for the site. If an audit or a customer questionnaire depends on those certificates, ask Vultr for the documents rather than citing a directory.

## What a Singapore bill really looks like

**GST, 9%, from 1 January 2024.** Vultr charges 9% Goods and Services Tax to any customer whose tax location is Singapore, in line with the country's rules for non-resident companies. A $5 plan invoices at $5.45. On a $20 plan that's $21.80, and on a five-instance test bench it's real money.

Registered businesses can take it off. Add your GST ID on the billing page inside the customer portal and GST stops appearing on subsequent invoices, replaced by Singapore's reverse-charge mechanism. Register for GST but forget to enter the ID, and the charge keeps coming. That single field is worth more than most coupon hunts.

**Hourly billing with a monthly ceiling.** Every started hour bills, and there is a monthly cap that stops a full month from costing more than the list monthly price. The practical consequence: spin up a 4 GB instance for a two-day migration and you pay roughly two days, not a month. Two catches. The minimum billable unit is one hour, and a stopped instance keeps billing at full rate until you destroy it, so "powered off" is not "not paying." GPU instances bill on actual hours in the month rather than the standard cap.

**The line items around the server.** Each instance includes one public IPv4; reserved IPs cost $3/month. Snapshots run $0.05/GB-month on compressed size and can be used to deploy an instance in any region, which is the cheapest cross-region backup Vultr offers. Outbound transfer starts with 2 TB free per account each month, pooled with each instance's own allowance, and overage is $0.01/GB. Inbound traffic is free.

## The reseller markup, in numbers

Search "Vultr Singapore" and you'll hit pages selling "Vultr Datacenter / Singapore location" VPS at prices that have nothing to do with Vultr's. One reseller's April 2025 listing, still the clearest example:

| Reseller listing | Sold as | Reseller price | Vultr's list price at that size |
| --- | --- | --- | --- |
| RVSS1 | 1 core @ 3.2 GHz · 1 GB RAM · 25 GB NVMe | $62.45/mo | $5/mo (1 GB, 25 GB SSD) |
| RVSS2 | 1 core @ 3.2 GHz · 2 GB RAM · 50 GB NVMe | $99.95/mo | $10/mo (2 GB, 55 GB SSD) |
| RVSS3 | 2 cores @ 3.2 GHz · 4 GB RAM · 80 GB NVMe | $199.95/mo | $20/mo (2 vCPU, 4 GB, 80 GB SSD) |

NVMe instead of SSD doesn't close a gap that size. The reseller's own FAQ promises a 1 Gbps shared port (10 Gbps on some NVMe boxes), delivery in 10–30 minutes, cancellation within 3 days if a problem can't be solved, and 99.9% uptime. Those are the reseller's terms and the reseller's support queue, not a Vultr SLA. Buying direct gets you the same Singapore facility, hourly billing, and self-service rebuilds, at roughly a tenth of the price.

## GPU capacity in Singapore: what was announced, what to verify

On 19 March 2024 Vultr announced a strategic partnership with Singtel to expand NVIDIA GPU capacity in Singapore and Southeast Asia. Singtel's Paragon platform was to integrate with Vultr's NVIDIA-powered cloud GPU platform, giving customers access to H100 Tensor Core GPU capacity in Singapore, with large-scale H100 clusters in Vultr's Singapore region deployed inside Singtel data centers "starting in Q3 2024."

That is an announcement with a date attached, not a menu. Whether H100 capacity is orderable in Singapore today, in what cluster sizes, and at what rate are questions only the console or a sales conversation answers. Plan AI work around what you can actually provision, and keep a fallback region in mind.

## When Vultr Singapore is the wrong choice

- **You need two availability zones in Singapore.** One facility means one failure domain. Cross-region is the answer, and if that's unacceptable, this isn't your platform.
- **You need a locally incorporated contracting entity, on-site hands, or a colocation cage.** A public cloud region is none of those.
- **You want GPU capacity tomorrow.** The Singapore GPU story runs through a partner announcement; verify availability before you design around it.
- **Your audience is nowhere near Asia-Pacific.** Paying APAC latency for European or American visitors makes no sense when 31 other locations exist.
- **You only want the cheapest box in Singapore and nothing else.** Local hosts and the large generalist clouds are worth pricing. The reason to pick Vultr is a Singapore location sitting inside the same API and catalogue as the other 31 cities, which matters once you run more than one region.

## FAQ

**Does Vultr charge tax on Singapore servers?**
Yes. Since 1 January 2024, a 9% GST applies to customers with a Singapore tax location.

**Can I get the GST removed?**
If your business is GST-registered, add the GST ID to your account on the billing page of the customer portal. Subsequent invoices drop the GST and fall under reverse charge. Sole traders and individuals without a GST ID pay it.

**Where is the Singapore data center?**
Vultr identifies it only as a Singapore region and doesn't publish a street address. Directory entries for the facility list no building size, colocation space, or power figures.

**Is billing hourly or monthly?**
Hourly, with a monthly cap so a full month costs no more than the list monthly price. Minimum billable unit is one hour, and stopped instances bill until destroyed.

**How does the $300 credit work?**
The offer attached to this link credits your account for new signups; eligibility, validity window, and which plans it covers are confirmed during signup. Read them before you deploy, since credits that expire in weeks suit a test bench better than a production box.

**Can I get H100 GPUs in Singapore now?**
Vultr announced H100 capacity in Singapore through Singtel with availability from Q3 2024. Check the GPU list for the Singapore region in the console, or ask sales, before committing to a plan that depends on it.

## Picking in one pass

- Static site, small API, VPN endpoint, Singapore IP needed → **Regular Performance 1 GB, $5/mo**. Take the $2.50 IPv6-only variant if your traffic and tooling are IPv6-ready.
- WordPress, Docker, a database, anything waiting on disk → **High Frequency 1 GB, $6/mo**.
- A handful of small sites or a low-traffic app with a cache → **2 GB at $10/mo**, or **2 vCPU / 2 GB at $15** if PHP workers are the bottleneck.
- Staging plus production → two 1 GB instances beat one 4 GB instance. Separate boxes fail separately.
- Anything GPU-shaped → confirm Singapore availability first, then size.

Two things to settle before you click deploy: whether a GST ID belongs on your billing page, and which billing mode you're on, because an instance you stop but never destroy keeps charging.

👉 [Open a Vultr account with the $300 credit and pick Singapore as your location](https://bit.ly/VuLtr)
