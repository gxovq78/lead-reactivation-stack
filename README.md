# real estate lead reactivation software: how to wake up a dead database and book appointments without hiring another ISA

Every agent and team has one: a CRM full of people who raised a hand at some point, then went quiet. Zillow leads from two springs ago. A seller who asked about a valuation and never answered the follow-up. Facebook leads that got three drips and a "just checking in."

Most of those contacts aren't dead. The conversation is. And that distinction is the entire reason the phrase "real estate lead reactivation software" gets typed into Google every day — people are sitting on lists they already paid for and want to know if a tool can squeeze appointments out of them.

Short answer: sometimes yes, but not by doing what most people assume. Here's how the category actually works, where CloseBot fits, and what it costs.

## The list isn't the problem. Follow-up decay is.

Run through the last five transactions your team closed. In almost every case, someone replied at least once — then the thread stopped for a boring reason. A task got marked complete. The agent got busy. The lead said "not right now" and nobody ever re-opened it.

That's why lead age matters less than people think. A 2023 Zillow opt-in who never got a call back after their second showing request is not a bad lead. They're an interrupted conversation.

There's a legal boundary sitting right next to that, and it isn't optional. You can text people who opted in and gave you a phone number. Old purchased lists, scraped numbers, or leads whose consent you can't document are a different category entirely, and TCPA penalties are not a rounding error. [CallAction's Revive](https://callaction.co/revive/) product page draws the same line: opt-in leads only, known litigators excluded, opt-outs honored immediately. Treat that as the floor, not a nice-to-have.

## What "reactivation software" actually covers

The category is messier than the search term suggests. Four types of tools get filed under it, and they do very different jobs:

1. **Bulk SMS platforms.** Cheap, fast, and the reason so many reactivation campaigns burn a database. You blast, a few people reply angry, opt-outs spike.
2. **Voice AI dialers.** Outbound calling agents that work through a list and try to book. Several vendors in this space price per connected call or per minute.
3. **Done-for-you sprints.** Agencies that run a controlled SMS campaign on your opted-in leads with human replies. CallAction publishes a result of 1,229 conversations from 2,920 old Zillow opt-in leads over 30 days (~42% response) for one campaign, with roughly 50 contacts messaged per day.
4. **Conversational AI that answers and books.** The lead texts back, and an AI agent qualifies them, handles objections, and drops an appointment on a calendar.

Pricing models swing wildly across those four groups. One vendor's breakdown puts reactivation pricing between $0.40 and $1.20 per attempted contact, or $8 to $22 per qualified live conversation. Others charge a flat monthly platform fee. That range is why two quotes for "lead reactivation" can differ by 10x — they're describing different products.

## The bottleneck nobody prices in: response capacity

Here's the part that decides whether a campaign works, and it has nothing to do with how many messages you send.

CallAction's FAQ makes the point bluntly: most agents can actively manage conversations with roughly **300–500 leads at a time**, and reactivation campaigns usually fail because replies arrive faster than anyone can answer them. The outreach volume wasn't the constraint. The reply handling was.

Which is exactly the constraint an AI responder removes. If 80 people text back on a Tuesday and four of them are ready to talk this week, that's a good problem — until nobody answers within ten minutes and the interest evaporates.

## Where CloseBot sits in this stack

CloseBot is agentic conversational AI for lead qualification, follow-up, and appointment booking. It works natively with HighLevel, HubSpot, and LeadConnector, and can run standalone through a chat widget or tie into a custom CRM via API.

One thing to get straight before you buy, because it changes your whole campaign plan: **CloseBot does not send the first message.** Its own documentation says it plainly — the product is responsive. It handles follow-up, but the initial outbound text has to come from you or from a workflow inside your CRM.

That's not a flaw, it's an architecture choice. It also means your reactivation campaign is really two systems holding hands: your CRM drips the opener, and CloseBot takes over the second someone replies.

For real estate specifically, the product ships with tools that other conversational AI platforms make you build from scratch. Agents can pull live property values, owner names, and property specs — CloseBot cites access to **100M+ US property data points** — negotiate, verify ownership, and send property images mid-conversation. Those data tools are US-only. Everything else (qualification, booking, follow-up) works internationally and in 40+ languages.

What it isn't: voice. CloseBot takes over text-based channels inside your CRM. If you want AI cold-calling your database, that's a different vendor category.

## What a real reactivation campaign looks like, step by step

CloseBot published the exact setup they used on 15,000 of their own old leads. It's worth copying because the mechanics are boring in the right way.

- Contacts get tagged `dbr` in the CRM, which triggers the reactivation workflow.
- The workflow **drips out 50 contacts per day** — a deliberate cap so replies stay answerable.
- Messages only go out during business hours (for them, 9am–5pm, Monday through Saturday).
- Sends are spaced out, **one message every two minutes**, to avoid looking like a blast.
- The opener is a text that identifies who's reaching out and asks a question. Questions get replies; announcements don't.
- No answer? Two more messages follow, one per day.
- **The moment a contact replies, they exit the workflow and the AI agent takes over.**

From there, the agent tags the contact `ai responded`, updates the opportunity to Engaged, qualifies conversationally, collects the details it needs, books on the calendar, and moves the stage to Demo Booked. If someone gets irritated or sends STOP, a scenario fires, tags them `ai off` / `not interested`, and the agent stops responding entirely. CloseBot's docs describe a dedicated "aggression detected" scenario for exactly this, and you should have one configured before you send anything.

Two details worth stealing from that playbook: build in a hard daily cap you can actually keep up with, and write the opener around the first question you want answered. If the text is "Are you still looking to sell this year?", your agent's first objective should be handling the answer.

## Sizing the bill before you commit

CloseBot's metered unit is the **AI reply**, not the outbound send. The plan slider on their pricing page is labeled "Monthly AI Replies," which matters for budgeting: your blast costs come from your CRM's SMS fees, not from CloseBot.

Rough example. You drip 1,000 contacts three times. Sixty reply. Say the average thread takes five AI replies to qualify and book. That's about 300 metered replies — inside the 500 included on a paid business plan, with the rest of the month to spare. Change those assumptions and the math moves, so run your own numbers with your actual reply rate.

Two things to verify directly with CloseBot before you build a margin model, because their own pages don't fully agree:

- The pricing page FAQ quotes agencies $0.012 per message, while the help center documents **$0.006 per message**.
- The help center says V2 agents run on your own AI provider API keys (token costs on you), while the pricing FAQ says bring-your-own-key isn't allowed for security reasons.

Neither is a dealbreaker. Both affect your cost math, so ask before you quote a client.

## Every plan CloseBot currently lists

| Plan | Built for | Key limits and extras | Price | Billing | Get it |
| --- | --- | --- | --- | --- | --- |
| **Free** | Testing the platform, or low-volume use | 100 AI replies/month, 1 agent, 1 user seat, 1 MB storage, unlimited account connections | $0 | Month to month, free indefinitely at 100 replies or fewer | [ Start on the free plan](https://app.closebot.com/register?fpr=li87) |
| **Core** (business plans) | Running your own pipeline | 1 job flow at the base tier, 500 AI replies included, 15+ templates (50+ on annual plans), human support, extra seats $5/user | $64/month; $53/month billed annually as $640/yr | Monthly or annual | [ Pick the Core plan](https://app.closebot.com/settings?tab=subscription&plan=business&toggle=monthly&fpr=li87) |
| **Agency** | Agencies reselling AI setters to clients | Unlimited agents across unlimited sources, white-label client portal, rebill all costs, 15+ templates | $397/month | Monthly | [ Set up an Agency account](https://app.closebot.com/settings?tab=subscription&plan=agency&toggle=monthly&fpr=li87) |
| **Growth** | High volume, SLAs, regulated industries | HIPAA compliance, quarterly audits, 99.99% priority uptime, priority support, custom volume | Custom | Talk to sales | [ Request Growth pricing](https://app.closebot.com/a?fpr=li87) |

The help center still breaks the business side into job-flow tiers: $197/month for 3 job flows, $297/month for 10, and $397/month for unlimited. Agency at $397/month covers unlimited agents and sources rather than job flows.

### Usage costs that sit on top of the base price

| Item | Free | Business (Core) | Agency |
| --- | --- | --- | --- |
| AI replies beyond your allowance | $0.08 each | Overage billed at 2x rate from your wallet | Per message, rebillable to clients |
| Knowledge library storage | 1 MB, can't be expanded | First 1 MB included; add-ons $0.10–$3.00 per MB/month | $0.006 per MB per day |
| Extra user seats | Not available (1 seat) | $5 per user | $5 per user, markable up |
| AI provider token costs | Not covered | Not covered | Not covered |

Property data tools cost nothing extra on any plan, including Free.

## What users actually report

Third-party feedback is mixed, and it's worth reading before you migrate a client's pipeline.

G2's reviewer summary highlights ease of use and fast setup. Its pros-and-cons breakdown also lists recurring complaints about occasional irrelevant answers, limited bot functionality, and the absence of native voice.

The r/automation thread "Closebot yes or no" is more granular. One user reports conversational booking and rescheduling that works "way better than GHL chat AI." Others describe unreliability, blaming prompts one week and CRM webhooks the next, and one longtime user says the team ships new features faster than it fixes basics. CloseBot's account replied in that thread that the team spent 12 weeks post-launch on bug fixes and that a testing portal overhaul had shipped.

The practical takeaway: the free plan exists, the paid plans carry a 7-day trial, and there are no refunds. Build your actual reactivation job flow on your own data during that window rather than judging it from a demo video.

## Which plan fits which situation

**Solo agent with 400 old leads.** Free plan, one agent, one CRM connection. Run a capped drip against your opted-in contacts and see whether the reply rate justifies anything more. If you cross 100 AI replies in a month, you've found your answer.

**Team with a shared database and a real pipeline.** Core. The 500 included replies cover a meaningful reactivation wave, extra seats are $5, and you can raise the ceiling instead of hitting overage.

**Agency selling AI setters.** Agency at $397/month is the only tier with rebilling and a white-label client portal — the two features that turn CloseBot from an expense line into a revenue line. If you're building a DBR offer for real estate clients, that's the whole business model in one plan.

**Regulated or high-volume operations.** Growth, mostly for HIPAA compliance and priority uptime.

**When to skip it.** If you have no documented opt-in consent, no capacity to handle replies, or you want AI voice calling rather than text, this isn't the tool for that job.

## Questions people ask before buying

**Does CloseBot text my old leads for me?** No. It responds, follows up, and books. The first outbound message comes from you or your CRM workflow.

**Is it legal to text old real estate leads?** Only with documented opt-in consent, honored opt-outs, and sane sending hours. CloseBot gives you the tools to stop responding and tag people out, but consent is your responsibility.

**Will it work with my CRM?** Native integrations cover HighLevel, HubSpot, and LeadConnector. Custom CRMs connect through the API, and anything else can use the chat widget with a webhook to push qualified leads across.

**Does it work outside the US?** Conversations do, in 40+ languages. The property value, owner name, and specs tools are US-only.

**How long does setup take?** CloseBot's docs advertise a 48-second starter setup, and the site claims most teams take their first agent live the same day. Realistically, a reactivation flow with a booking objective and an aggression scenario takes longer than that — but not weeks.

## The bottom line

Reactivating a database isn't a blasting problem, it's a reply-handling problem. Pick software by asking one question: when 60 people text back this week, what happens in the next ten minutes? If the answer is "whoever's free gets to it," you've found the leak.

CloseBot answers that question with a conversational agent that qualifies and books on the spot, backed by US property data that most competitors would make you build. Its limits are just as clear: it won't send the first message, it doesn't do voice, and the property tools stop at the US border.

If you're sitting on a list you already paid for, the cheapest test is also the obvious one: [👉 open a free CloseBot account](https://app.closebot.com/register?fpr=li87), build one agent around your actual reactivation script, and point it at a few hundred opted-in contacts. You'll know inside a week whether your database was dead or just unread.
