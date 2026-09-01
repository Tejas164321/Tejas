# @tejas164321 — DEV.to Positioning & Community Strategy

*Researched 1 September 2026. Evidence base: your DEV profile and post list, two posts read in full (Turing's Mirror, npmx.dev cache bug), your GitHub profile and README, the DEV homepage feed and trending list as of 31 Aug 2026, the DEV challenge calendar, and current reporting on WebMCP, agent security, and AI-content fatigue. Note: view counts and follower counts aren't public on a logged-out profile, so all engagement analysis below is based on reactions and comments.*

---

## 1. Audit: what your profile actually is right now

### The single most important pattern

**Every one of your ten posts is a DEV Challenge submission.** Not most. All of them.

| Post | Date | Reactions | Comments | Challenge |
|---|---|---|---|---|
| Pawscript | Aug 17 | 12 | 1 | Weekend: Dog Days |
| I Chased a Data Bug for an Afternoon | Aug 12 | 7 | 1 | Summer Bug Smash |
| Vada Pav landing page | Aug 11 | 17 | 11 | Frontend: Comfort Food |
| Fixing a Silent Cache Bug in npmx.dev | Aug 10 | 16 | 8 | Summer Bug Smash |
| FinPal | Jul 10 | 18 | 3 | Weekend: Passion |
| Turing's Mirror | Jun 21 | 50 | 16 | June Solstice Game Jam |
| Hermes Agent vs LangChain | May 26 | 10 | 2 | Hermes Agent |
| How I Finally Shipped FinPal | May 25 | 10 | 2 | GitHub Finish-Up-A-Thon |
| Gemma 4 multi-token prediction | May 24 | 7 | 1 | Gemma 4 |
| WebMCP at I/O 2026 | May 23 | 11 | 1 | Google I/O Writing |

This explains almost everything else about your numbers, and it's the thing to fix first.

Challenge posts have a specific failure mode. The traffic arrives from the challenge landing page, not from you. The reader came for the challenge — to see what other people built, or to scout the competition — and then they leave. There is no reason for them to follow you, because the next thing you publish will be about a completely unrelated sponsor product. Your feed reads as: game jam → GitHub Copilot → Gemma → Hermes → finance app → landing page → npm bug → dog letters. A person who liked one of those has no basis for predicting whether they'll like the next.

You are also writing inside someone else's template. "This is a submission for X / What I Built / Demo / How I Built It / What I Learned." That structure is designed to make submissions comparable to a judge. It is actively hostile to building a recognizable voice, because it forces every post into the same shape regardless of what the post is actually about.

Five and a half months in, you have 10 posts, a decent badge collection, and no editorial identity. That's not a writing problem. It's a sourcing problem: your topics are chosen by DEV's sponsor calendar.

### What you're actually good at (and it's not what you think)

Read the two comment threads that contain real engagement, and a pattern appears.

**Turing's Mirror** got 50 reactions, but be careful with that number. Several of the commenters — Bhushan Patil, Divesh Patil, Harsh Saurangpate, Shakib S. — created their DEV accounts on 21 June 2026, the day you posted. That's your local network showing up, which is fine and normal, but it isn't market signal. Strip that out and the real signal is two comments: Nazar Boyko (backend/AI engineer, Austin) and Mudassir Khan (CTO, writes about LLM-facing content). Both of them ignored the game entirely and engaged with **one observation buried in the middle of the post**:

> "The scariest moment in playtesting was when someone pointed at a human message and said 'that sounds so AI.' We've started writing like the models we trained."

Boyko's reply asked which tells stopped working by Round 5. Khan's reply connected it to what he sees in content evals. Your answer — that "too tidy" grammar died first and hedging survived longest — is genuinely more interesting than the game. It's a small empirical finding about how humans now fail a test they designed.

**The npmx.dev post** is the best technical writing on your profile by a wide margin, and it has zero of the padding that makes DEV posts skippable. You traced a stale version number through `usePackageComparison` → `$npmRegistry` → `useCachedFetch`, found a `_ttl` parameter that was accepted and never used, found the hardcoded `cache: 'force-cache'` that had quietly replaced it, checked what the registry actually sends (`max-age=300` plus an ETag), and shipped a two-word fix. Then you closed with:

> "Dead parameters are worth pausing on — they're often a fossil record of intent the code no longer honors."

That is a memorable, transferable, quotable idea, derived from a real investigation, that a reader can use tomorrow in their own codebase. It's the single most brandable sentence you've written.

**So: the two moments where you produced something nobody else had were both cases of looking closely at a real system and reporting a finding.** Neither was a build. Neither was a tutorial. Neither was an analysis of an announcement.

### What's underperforming and why

Three of your posts — Gemma 4 (7 reactions), Hermes vs LangChain (10), WebMCP (11) — are your longest and most effortful (5–7 min reads) and your weakest performers. They share a format: *a well-organized analysis of something that was announced, written shortly after it was announced, without the author having run it.*

The Hermes post is titled "Why Hermes Agent Compounds While LangChain Stays Flat — A Deep Architectural Breakdown." That's a strong claim about runtime behaviour over time. To earn it you'd need to have run both for a while and measured something. Read as an architecture argument it's fine; read as a claim about compounding it's unfalsifiable, and experienced readers can feel that. Same with Gemma 4 "changes the economics of running AI locally" — the economics claim wants a table of tokens/sec and memory on hardware you actually have.

This matters more in 2026 than it would have in 2023, for reasons covered in the next section.

### The credibility leak nobody will tell you about

On your best-performing post, your own comments are:

> "Thank You , Play the Game on provided link and visite repo on Github (Tejas164321) and star repos ......."

> "If Guys has Any Suggesion Please Comment......."

Your articles are polished. Your comments read like a different person — one asking for stars. Senior developers read comment threads, and this is the kind of thing that makes them decide you're farming rather than building. Nazar Boyko asked you a sharp technical question on that same thread and you gave a genuinely good answer; the star-begging comment sits four replies away from it.

Related: **12 comments written in five and a half months.** You consume DEV. You don't participate in it. On a platform where the follow graph is built almost entirely through comment threads, that's the largest single lever you're not pulling.

### Voice: a real strength with a 2026 liability

Your prose is good. "Dark = the machine's world. Cold, clean, perfect. That's what early AI sounds like: polished in the wrong way, like someone who memorised manners without understanding them." That's a real sentence by a real writer.

The liability: em-dashes, tricolons, aphoristic closers, and clean parallel structure are now, fairly or not, read as AI-writing tells on DEV specifically. One widely-shared DEV post this year explicitly lists the em dash and phrases like "here is what I learned" as heuristics for sloppy writing assistance. You have both.

Do not flatten your voice to avoid this. Instead, load your posts with things that cannot be generated: PR links, DevTools screenshots, raw numbers, the specific wrong turn you took, the thing you got wrong when you re-read it a day later. The npmx post does this and is immune. The Gemma post doesn't and isn't.

### Audit summary

| | |
|---|---|
| **Stop** | Letting DEV's challenge calendar pick your topics. Star-begging in comments. Writing analyses of announcements you haven't run. |
| **Improve** | Comment volume (12 → ~40/month). Titles that make a checkable claim. Always publishing the raw data. |
| **Double down** | Root-cause debugging narratives. Empirical findings pulled out of builds. The closing transferable-lesson move. |

---

## 2. The DEV.to ecosystem as it stands right now

DEV is at just over 4 million registered members. Here's what the front page and trending list looked like on 31 August 2026.

### What's oversaturated

Looking at DEV's own trending guides sidebar, these clusters dominate:

**AI coding-agent tooling comparisons.** "Superpowers vs Agent Skills vs Pocock: Three Philosophies of AI Coding Workflows," "I Spent a Day With Kiro Crew. Here's What It Actually Does," "Ponytail: The AI Coding Skill Taking GitHub by Storm," "Stop Making Your AI Coding Agent Grep Your Whole Repo — Try codebase-memory-mcp". There is a new agent-workflow tool every week and a dozen people writing the same first-impressions post about it.

**Local model economics and hardware math.** "Mac Studio M5 Ultra vs NVIDIA DGX Spark: The $5,500 Local AI Bet," "The M5 Ultra Mac Studio: I Did the Math So You Don't Have To," "Run Qwen 3.8 27B Locally: Real GGUF Sizes, the KV Cache Trick, and the Template Trap," "Qwen 3.8 27B vs Qwen 3.6 27B". Four posts, one week, one topic. This is where your Gemma 4 post landed, and it's now a hardware-owners' game.

**Web platform news restated.** Two separate trending posts about the same HTTP QUERY method: "The new HTTP method : QUERY" and "HTTP Just Got Its First New Method in 20 Years. Here's Why You Should Care." When something is announced, forty people write the explainer within 72 hours.

**Model-opinion posts, listicles, MCP vendor roundups.** "It's not just you, Opus 5 is a 'Jargon Douche' - but there's a fix," "10 Git Commands You'll Wish You Knew Earlier," "The AI Engineer's Reading List for 2026," "Best Enterprise MCP Gateway for Your AI Agents in 2026".

### The fatigue is real and it's specific

This is the most important context for your strategy. DEV's own community has been openly revolting against AI-generated content all year. One widely-read post describes the problem as low-effort AI-generated posts with titles like "10 AI Tools That Will 10x Your Productivity in 2026" followed by the same generic list every other post has, and singles out "endless AI agents vs agents comparisons, Claude Code this, Gemma 4 that, I built X with AI in 47 seconds" as mostly indistinguishable from each other. The same piece points to a burnout thread with 119 reactions and 81 comments where the top comment chain blames AI-generated content as the primary trigger.

Read that list again. "Gemma 4 that." You published a Gemma 4 post.

The broader picture matches: moderators across many communities report spending 2–4x more time on moderation than in 2023, largely due to AI-generated spam and low-quality AI posts from users trying to build reputation.

**What this means for you:** the bar for "AI content" on DEV has moved. Explaining a model or a protocol is now a negative signal by default — it's the exact shape slop takes. The only AI content that still earns attention is content that could only exist because a specific human did a specific thing and reported what happened.

### What still makes developers stop scrolling

From the same feed, the posts pulling disproportionate engagement:

- **Failure taxonomies with specifics.** "9 Ways Your AI Agent Silently Fails (and How to Catch Each)" — 27 reactions, 19 comments. Enumerated, concrete, actionable, about things going wrong.
- **Real debugging narratives.** DEV's own team published "Fixing Delicate Cache Mismatches in a Brownfield SPA: A Pragmatic Solution" — same genre as your npmx post. When the platform's founder writes in your genre, that genre is safe.
- **Deep, narrow, unfashionable engineering.** "Delta encoding multiplayer game state," "Sessions vs JWTs: you are choosing how often you pay for state," "True Randomness in Laravel with Lararand". Small audiences, high-quality readers.
- **Discussion posts.** "Tell Me About You" — 48 reactions and 48 comments; "How long does it take for you to write a dev.to article?" — 32 reactions, 44 comments. Near-zero production cost, enormous comment volume. You have published exactly zero of these.
- **Unhinged-but-real experiments.** "I Built an Office Full of AI Developers. They Started Opening Pull Requests," "Badger: An E-Ink Badge I Use For Conferences," "I Tried to Beat Peter Norvig and Accidentally Became Ryan Gosling".

### The challenge calendar (useful, but as a tool, not a strategy)

Upcoming: DEV Weekend Challenge v26.09.03 (Sept 3), Sanity Challenge (Sept 16), Kaggle Challenge (Sept 23). Hacktoberfest writing challenges have run in October each of the last two years and will almost certainly return.

Challenges are a good distribution channel and a bad identity. Keep using them — but as a place to publish an episode of *your* series, not as the reason a post exists.

---

## 3. Positioning: five directions, and the one to take

Each scored on fit with your actual skills, current demand, and saturation.

**A. The Agent-Ready Web — adversarial.**
WebMCP, browser agents, and what happens when agent-facing interfaces meet reality. Requires: shipping real web apps (you do), reading specs early (you do), willingness to publish things breaking (you have). Demand is climbing fast. Saturation is high for explainers and near-zero for hands-on adversarial work. **Strongest.**

**B. The root-cause debugger.**
"I chased this bug through someone else's codebase and here's the tell I'll never miss again." Proven by your npmx post, genuinely rare, immune to slop accusations. Weakness: it's a *method*, not a *topic* — hard to build a following around because readers can't predict what the next post is about. Best used as your craft rather than your banner.

**C. AI agent reliability engineering.**
Failure modes, evals, observability. Demand is high but this is filling up fast with vendor content, and the "9 ways your agent fails" post is already occupying the listicle slot.

**D. AI-native product builder / build-in-public.**
FinPal, AI Recruiter, Dairy Nine. Extremely saturated, and as a final-year student you can't win on scale or revenue screenshots against people posting MRR charts.

**E. Local AI economics.**
Your Gemma post's lane. Four competing posts appeared in a single week and the good ones require $3,000–$5,500 of hardware. Skip.

### Recommendation: A, executed with B's method

> **@tejas164321 is the developer who points agents at real systems, breaks them, and shows you exactly where they fall apart.**

Not "explains AI agents." Not "builds with AI." **Tests, breaks, and reports.**

### Why this specific bet is timed correctly

WebMCP is at the exact stage where hands-on work is possible and nobody has done it yet:

- It entered origin trials in Chrome 149, and Google announced it alongside broader browser AI work at I/O 2026. You can actually run it today.
- Since August 2026 it is default-on across Shopify storefronts and Cloudflare-fronted websites. That means there is now a live population of agent-callable sites in the wild to point things at.
- Expedia, Booking.com, Shopify, Credit Karma, TurboTax, Redfin, Etsy, Instacart and Target are experimenting with it in the origin trial phase.
- The API is unstable in a documentable way: the specification has already evolved across versions, including the removal of the provideContext and clearContext methods in March 2026.
- And critically: security concerns like prompt injection and data exfiltration through tool chaining are acknowledged in the spec but not fully resolved.

That last line is your entire content moat in one sentence. A major browser standard is shipping with a known, acknowledged, unsolved security hole, and the DEV coverage of it consists entirely of "what is WebMCP" explainers.

Meanwhile the underlying problem is confirmed unsolved by everyone qualified to say so. At Infosecurity Europe 2026, OWASP contributor Ariel Fogel called prompt injection an unresolved problem, because LLMs process inputs as a single token sequence with no reliable way to enforce privilege boundaries between system prompts, user queries, and content an agent retrieves — and warned it has become more dangerous as agents gain tools and the ability to act. At Black Hat USA 2026, Brave security engineer Artem Chaikin presented on attacking and defending AI browsers, concluding the threat isn't going anywhere despite added guardrails. In May 2026 the Five Eyes agencies issued joint guidance on agentic AI naming prompt injection as a core attack path and stressing that no single safeguard is enough.

You already wrote the "WebMCP matters" post in May. You were early and you were right. Now the thing has shipped into origin trial and gone default-on at two major hosting layers, and you're positioned to be the person who tests it rather than the person who announced it.

### Who you're attracting

Be specific, because it changes how you write:

- **Primary:** mid-level to senior full-stack and backend engineers now being asked to make their product "agent-ready" and quietly unsure what that means or whether it's safe.
- **Secondary:** AI engineers building agents who need to know what breaks on the other side of the wire.
- **Tertiary:** application security people who are watching agentic browsing arrive and want practitioner evidence, not vendor whitepapers.

Notably **not**: beginners, bootcamp students, tutorial-seekers. That's a deliberate trade. It's a smaller audience with far more valuable members, and it's the audience that comments.

---

## 4. Your content moat

A moat isn't a topic. It's something that's expensive for others to copy. Here are the specific ones available to you, in order of defensibility.

**1. You run the thing.** The single scarcest resource on DEV in 2026 is someone who actually executed the experiment. Almost all AI content is now a summary of a summary. "I registered a WebMCP tool with a deliberately misleading description and watched three agents call it anyway" cannot be produced by prompting. It requires a day of work. That day of work is the moat.

**2. You publish raw data.** Every experiment post ships with a public repo: the harness, the prompts, the transcripts, the failures. This does two things — it makes the claim checkable, and it invites people to rerun it and disagree, which is the highest-value comment you can receive.

**3. You publish failures at full detail.** Your instinct here is already good. In Turing's Mirror you wrote that you got your own Round 5 question wrong re-reading it a day later. That's the sentence readers remember. Most people write around their failures; you can write straight through them.

**4. Adversarial framing.** Almost nobody on DEV attacks the thing they're writing about. "Here's how to use X" is infinite. "Here's what X does when I lie to it" is rare, harder to fake, and much more interesting.

**5. The transferable tell.** Your closing move — "dead parameters are a fossil record of intent the code no longer honors" — is a genuine differentiator. Every post should end with one heuristic a reader can carry into a codebase they've never seen. Do it consistently and people will start recognizing the shape.

**6. The forensic build.** Turing's Mirror worked because it wasn't really a game, it was an instrument for producing an observation about people. Keep building small things whose purpose is to *generate a finding*, not to be a product.

The target reaction is: *"This looks like something Tejas would build"* → **a small, precise, slightly adversarial experiment against a system everyone else is only talking about, with the raw data attached and one sentence at the end you'll remember next time you're debugging.**

### What to explicitly avoid

Do not become the WebMCP tutorial guy. The API surface is still shifting and readers are told to check the changelog before starting. Tutorials rot; findings don't. "What happened when I did X" ages into a useful historical data point. "How to do X" ages into a bug report.

---
## 5. Recurring series

Six series. Two are load-bearing (Agent vs. The Web, The Fossil Record), one is the community engine (Break My Implementation), three are rotation.

---

### Series 1 — **Agent vs. The Web**

**Concept.** Point a real agent at a real web surface, give it a real task, and publish the full transcript of what happened. No summaries, no vendor claims. Every episode has a task, a target, a result, and a failure.

**Example.** *"I gave three browser agents the same checkout task on a WebMCP-enabled store. Two of them bought the wrong thing."* Same task, same site, three agents, transcripts and screenshots for all of them, plus the specific point in each run where the agent's model of the page diverged from the page.

**Why it works.** WebMCP is default-on across Shopify storefronts and Cloudflare-fronted sites since August 2026, so real targets exist. Nobody is testing them. Every episode produces a claim that can be argued with, which is what generates comments. And the format is infinitely renewable — new agent, new site, new task.

**Audience.** Full-stack engineers whose employer is about to ask them about agent readiness; AI engineers who only see their side of the interaction.

**Frequency.** Every two weeks. This is your flagship.

---

### Series 2 — **The Fossil Record**

**Concept.** One real bug in a real open-source codebase, traced from symptom to root cause, ending with the generalizable tell. Named after your own line about dead parameters. The rule: it must be a bug you actually found and fixed, with the PR linked.

**Example.** *"A component's cleanup function was correct. It ran at the wrong time. Nobody noticed for eight months."* — trace, wrong assumption, real cause, PR, and the tell: what shape of code should have made you suspicious three steps earlier.

**Why it works.** It's the genre your best post is already in, it's the genre DEV's own team publishes in, and it's structurally impossible to fake — the PR link is the proof. It also builds real open-source credibility, which compounds outside DEV.

**Audience.** Working engineers of every stripe. This is your broadest-reach series.

**Frequency.** Monthly. Sourced from Hacktoberfest in October, then from issues in repos you actually use.

---

### Series 3 — **Break My Implementation**

**Concept.** You ship something small and genuinely functional, publish it with the source, and explicitly invite readers to break it. Two weeks later you publish every successful break, credited by name, with your fix or your concession that you can't fix it.

**Example.** *"I built a WebMCP tool with what I think is a safe permission boundary. Break it."* → two weeks → *"Eleven of you broke it. Four ways I hadn't considered. One I still can't fix."*

**Why it works.** This is the single strongest community mechanism available to you. It converts readers into contributors, gives them a reason to return on a known date, and the follow-up post writes itself out of their work. Being publicly beaten by your readers is also the fastest credibility-building move there is — it signals you care about the truth more than about looking good.

**Audience.** Security-minded developers, and the exact senior readers who never comment on tutorials.

**Frequency.** Every six weeks — a challenge post and a results post each cycle.

---

### Series 4 — **Nobody Asked For This**

**Concept.** Build a deliberately absurd thing that is technically real, where the absurdity is the instrument for exposing a genuine limit in a system.

**Example.** *"I gave an AI agent a credit card with a ₹500 limit and told it to buy me lunch. It spent 40 minutes arguing with a captcha."* Or: *"I made my portfolio site lie to AI agents about what it does, to see whether anything checks."*

**Why it works.** This is Turing's Mirror's actual DNA — a small strange thing that produces a real observation. It's the most shareable format you have, it travels off-platform better than anything else, and the genre performs on DEV right now. The discipline: the joke is the delivery vehicle, the finding is the payload. If there's no finding, don't publish.

**Audience.** Everyone. This is your top-of-funnel.

**Frequency.** Every 4–6 weeks.

---

### Series 5 — **Receipts**

**Concept.** Small, honest, narrow benchmarks with the methodology stated up front and the harness in a public repo. Explicitly not hardware reviews — behavioural benchmarks.

**Example.** *"How many turns before an agent forgets its own constraint? I measured it across four models."* Or: *"I measured how much of an agent's context window is spent re-reading files it already read."*

**Why it works.** Benchmarks are the most linkable content type — people cite them for months. And behavioural benchmarks need no hardware, which is the entry barrier that locks you out of the local-model lane. State limitations honestly and small-n benchmarks are respected; overclaim and you get destroyed in the comments.

**Audience.** AI engineers, tech leads making tooling decisions.

**Frequency.** Monthly.

---

### Series 6 — **The Spec Is Lying To You**

**Concept.** Read a spec closely against its shipped implementation and document the gap. Not criticism for its own sake — the goal is the gap between what a document promises and what actually happens when you call the API.

**Example.** *"WebMCP's spec says agents 'may' request confirmation for destructive tools. I checked what 'may' means in practice."* Or: *"The removal of provideContext in March 2026 broke a pattern the docs still recommend."*

**Why it works.** Requires patience most people don't have, produces claims nobody else can produce, and puts you in conversation with the people writing the specs — which is a much better outcome than another 50 reactions. The WebMCP spec has already changed materially across versions, so material exists.

**Audience.** Spec-adjacent developers, standards people, senior engineers.

**Frequency.** Every 6–8 weeks.

---

## 6. Hooks

Twenty patterns that create curiosity through specificity rather than exaggeration. The distinction that matters: clickbait promises a feeling; a good technical hook promises a *checkable fact*.

**Result-first (the finding is the headline)**
1. *[Specific action]. [Surprising outcome].* → "I gave three agents the same checkout task. Two bought the wrong thing."
2. *[N] of [M] [things] failed [specific check].* → "17 of 25 WebMCP-enabled sites expose a tool that can spend money without confirmation."
3. *The number that changed everything: [figure].* → "One agent used 74% of its context window re-reading the same file."

**Wrong-assumption**
4. *I assumed [X]. I was wrong, and why is the whole story.* → your npmx opening, which is already your best hook.
5. *Everyone says [X]. I measured it. [Contradiction].*
6. *[Thing] isn't [obvious cause]. It's [actual cause].* → "It Was Never About the Data" — you've used this and it works.

**Adversarial**
7. *I lied to [system]. Here's what it did.* → "I lied to an AI agent about what my site does. It never checked."
8. *Break my [thing].* → the invitation as headline.
9. *[N] of you broke it. [M] ways I hadn't considered.*
10. *I tried to make [system] do [forbidden thing]. It took [duration].*

**Forensic**
11. *I chased [symptom] for [duration]. The cause was [one line].*
12. *[Innocuous artifact] was the only clue.* → "An unused parameter was the entire bug."
13. *This code was correct. It ran at the wrong time.*

**Contrarian, earned**
14. *[Popular thing] solves a problem you don't have.*
15. *Stop [common practice]. Here's what to do instead — with numbers.*
16. *[Widely praised feature] is the most dangerous part of [system].*

**Stakes and timing**
17. *[Standard] shipped with a known [problem]. Nobody's talking about it.* → you've run this once already, correctly.
18. *In [timeframe], [specific change] happens. Most codebases aren't ready.*

**Absurd-but-real**
19. *I built [ridiculous thing]. It found a real problem.*
20. *Nobody asked for this. [Result] anyway.*

### Applied to your material

| Weak version | Stronger version |
|---|---|
| "Understanding WebMCP Security" | "I registered a WebMCP tool that lies about what it does. Three agents called it anyway." |
| "Gemma 4's Multi-Token Prediction Changes the Economics" | "I ran Gemma 4 on a laptop for a week. The economics claim only holds in one specific case." |
| "Why Hermes Compounds While LangChain Stays Flat" | "I ran the same agent task 200 times on Hermes and LangChain. Only one of them got worse." |
| "How AI Agents Handle Forms" | "I put a hidden instruction in a form label. Two agents obeyed it." |
| "Building With WebMCP" | "Shopify turned WebMCP on by default in August. I checked what that actually exposed." |

**The rule for every title:** it must contain something falsifiable. If a reader can't imagine disagreeing with your title, it isn't a hook — it's a topic label.

---

## 7. Turning readers into participants

Fifteen mechanisms, roughly ordered by how much participation they generate per unit of your effort.

**1. Break My Implementation.** Covered above. Highest-value mechanism you have. It gives readers permission to be adversarial toward you, which is exactly what senior developers enjoy and rarely get invited to do.

**2. Credit contributors in the post body, by name and by finding.** Not a thanks list at the bottom — a section per person, describing what they found, with their profile linked. People return to a place where their name appears. This one habit does more than any CTA.

**3. Reproduce-and-disagree.** Every experiment ships a repo with a one-command harness and an explicit line: *"Run this on your setup and tell me if you get different numbers — I'll add your results to the post."* Then actually update the post and say who changed it.

**4. Predictions with a scheduled scoring date.** "Five predictions about agent-ready web adoption. I'm scoring these on 1 December — put yours in the comments." The scoring post is guaranteed content and guaranteed return traffic. Publicly getting a prediction wrong is worth more than getting one right.

**5. Choose the next target.** End each *Agent vs. The Web* episode with a genuine vote on the next target: which agent, which site, which task. Readers who pick the target come back to see the result. Costs you nothing — you had to choose anyway.

**6. Bug hunts on your own live projects.** FinPal, AI Recruiter and your portfolio are all deployed. Publish a scoped bug bounty with no money and a lot of credit: "Find a way to make FinPal's classifier mislabel a transaction. Best three get a section in the follow-up." This is where your existing projects become community assets instead of resume entries.

**7. Reader submissions with a fixed format.** "Send me the weirdest tool description you've written for an agent." A structured, low-effort ask with a visible payoff — inclusion in a post — is far more effective than "what do you think?"

**8. Adversarial challenges with a scoreboard.** "Here's a WebMCP tool with a permission check. First person to bypass it gets top billing." A scoreboard, even a plain markdown table, turns readers into competitors.

**9. Steal-my-harness.** Publish your test rigs as standalone repos so other people run *your* experiment on *their* systems and write it up. Their post links back. This is how a method spreads beyond your own posting cadence.

**10. Architecture teardowns with a real open question.** Post a design and end with a decision you genuinely haven't made, with the tradeoff laid out. Engineers cannot resist an unresolved architecture question. The key is that it must actually be unresolved — a fake question reads as a fake question.

**11. The failure thread.** A recurring low-effort discussion post: "What's the strangest way an agent has failed on you this month?" Discussion posts on DEV routinely pull 40+ comments for almost no production cost. You have published zero. Start.

**12. Reply to every substantive comment within 24 hours, at technical depth.** Your reply to Nazar Boyko — that "too tidy" died first and hedging survived longest — was better than half the post. That's the standard. Non-substantive comments get a short warm reply; substantive ones get a real answer.

**13. Comment on other people's posts as your primary growth channel.** Target: 8–10 substantive comments a week on posts in your lane. Not "great post" — a specific technical addition or a respectful disagreement. This is how you get discovered by the exact people you want. It is also the thing you are currently doing least.

**14. A public running experiment log.** A single pinned repo or page listing every experiment: hypothesis, status, result, link. Makes the body of work legible as a project rather than a series of posts, and gives people something to watch.

**15. Collaborative episodes.** Invite a reader who broke something to co-write the follow-up. Their audience becomes aware of you, and one genuine collaborator is worth several hundred passive followers.

---

## 8. Where the technology opportunities actually are

Filtered for: technology is becoming important, developers are curious, and the content isn't saturated. Saturated areas are listed at the end so you know what to skip.

### Tier 1 — take these now

**Agent-facing interface security.** The gap here is enormous. WebMCP's own spec acknowledges prompt injection and data exfiltration through tool chaining without resolving them, OWASP calls prompt injection architecturally unresolved, and Black Hat 2026 concluded AI browsers remain vulnerable despite guardrails. Meanwhile DEV's coverage is explainers. Angles: what a malicious tool description does to a real agent; whether "destructive" tool annotations are honoured; whether a page can influence an agent through content it merely renders; what happens when two tools on the same page contradict each other.

**Auditing the newly agent-enabled web.** Since WebMCP went default-on across Shopify and Cloudflare-fronted sites in August 2026, thousands of sites became agent-callable without their owners deciding to. Build a crawler, survey what's exposed, publish the aggregate. Nobody has done this. It's the highest-impact single post available to you right now.

**Agent memory and context corruption.** Under-covered relative to its importance. Research shows web agents are vulnerable to context manipulation, with strawman injections via a public paste achieving prompt leakage, private-information exfiltration and goal hijacking. Practitioner-level treatment of this barely exists. Angles: how many turns before an agent forgets a constraint; whether a poisoned memory entry survives a session reset; what a "sticky" bad memory costs in tokens.

**The AI-PR review burden as an engineering problem.** Real, measured, and widely felt: Sonar's 2026 State of Code found 96% of developers don't fully trust AI-generated code and 38% say reviewing it takes more effort than reviewing human-written code; LinearB's 2026 benchmarks found AI PRs wait 4.6x longer for review and are rejected more often. Most writing on this is complaint. Almost none is tooling or measurement. Build something that measures review burden in a repo and publish the numbers.

### Tier 2 — good, slightly more competitive

**Plan-then-execute and other agent architecture patterns** — actively researched, thinly covered for practitioners. Implement one, benchmark it against a naive loop, publish.

**Progressive enhancement for agent-readability.** Real engineering question with no established answer: how do you build a site that serves humans and agents without maintaining two things? Genuinely in your Next.js/React wheelhouse.

**Spec-drift documentation.** provideContext and clearContext were removed in March 2026; more will change. Being the person who tracks what broke is a durable, low-competition position.

### Tier 3 — skip

Local model hardware economics (four competing posts in one week). Agent framework comparisons. MCP server roundups. "What is MCP/WebMCP." First-impressions posts on new coding agents. Model release reactions.

---

## 9. Turning one project into a content ecosystem

The failure mode you named — build → one post → move on — is exactly what happened to FinPal. You published *FinPal* (18 reactions) and *How I Finally Shipped FinPal* (10). Two posts, no arc, no reason to follow the story.

The fix is to treat a project as a **series of questions you answer in public**, where each post creates the reason for the next.

### The arc, applied to your existing work

**FinPal** — an AI expense classifier that has processed 1000+ real financial transactions from PhonePe, GPay and bank statements. That corpus is an asset nobody else on DEV has.

1. *"I have 1,000 real UPI transactions. Here's what my classifier gets wrong."* — a genuine error analysis with the confusion categories, not the launch post.
2. *"Break my classifier"* — invite readers to submit merchant strings that fool it. Publish an anonymised sample set.
3. *"Twelve of you broke it. The failure modes clustered into three shapes."*
4. *"I gave an agent access to FinPal's tools. It categorised my rent as entertainment and then acted on it."* — the agent-safety episode, connecting FinPal into your main lane.
5. *"What I'd change about the architecture after 1,000 transactions"* — the honest retrospective, including the thing you'd tear out.

Five posts, one project, a through-line, and a reason to return. Same project, ten times the value.

**Turing's Mirror.** You have an unpublished finding sitting in a comment reply. Write *"'Too tidy' was the first tell to die: what 300 people got wrong about spotting AI text."* Add scoring to the game, gather data from readers, publish the aggregate. That's a real, small, original dataset — the sort of thing that gets cited.

**Pawscript and the Vada Pav page** are challenge one-offs. That's fine. Not everything needs an arc; know which ones do.

### The template for anything you build from here

Before you build, write down the question the build will answer. Then:

| Stage | Post | Community hook |
|---|---|---|
| Question | "Here's what I'm about to find out, and my prediction" | Readers post their predictions |
| Build | Architecture post with one genuinely open decision | Readers argue the decision |
| Result | The finding, with raw data | Readers rerun it |
| Attack | "Break my implementation" | Readers attack it |
| Reckoning | "Here's what broke, credited" | Contributors are named |
| Retrospective | "What I'd do differently" | Closes the loop, seeds the next question |

Six posts, one build, and every stage produces the audience for the next. Note that only two of the six require building anything.

---

## 10. The 90-day plan (September – November 2026)

**Cadence: one substantial post per week, plus one low-effort discussion post per week.** Not more. Fifty-two good posts a year beats two hundred forgettable ones, and at your current stage consistency of *identity* matters more than volume.

Non-negotiable weekly baseline, regardless of what you publish:
- **8–10 substantive comments** on other people's posts in your lane
- **Reply to every comment on your posts within 24 hours**
- One **#discuss** post (15 minutes of work)

### Month 1 (September) — Establish the lane

The goal is that by 30 September, someone scrolling your profile can state what you're about in one sentence.

| Week | Publish |
|---|---|
| 1 (Sep 1–7) | **Series launch: Agent vs. The Web, episode 1.** Audit what WebMCP actually exposes on the newly default-on sites. This is your strongest available post — lead with it. Optionally also enter the Sept 3 Weekend Challenge, but only if you can make it an episode of a series. |
| 2 (Sep 8–14) | **The Fossil Record, episode 1.** A real bug in a real repo, PR linked. Re-run the npmx formula on a fresh target. |
| 3 (Sep 15–21) | **Break My Implementation, round 1 opens.** Ship a small WebMCP tool with a permission boundary and invite attacks. Two-week window. |
| 4 (Sep 22–30) | **Receipts, episode 1.** A narrow behavioural benchmark — turns-until-constraint-forgotten, or context spent on re-reads. Harness in a public repo. |

Also in month 1: rewrite your DEV bio (it currently says "Software Developer," which says nothing). Something like *"I point agents at real systems and publish what breaks. Full-stack, Next.js, Pune."* Pin your two strongest posts. Delete or replace the star-begging comments.

### Month 2 (October) — Prove the series repeat

October has Hacktoberfest, which is a free content supply for The Fossil Record. Use it.

| Week | Publish |
|---|---|
| 5 | **Break My Implementation, round 1 results.** Every break credited by name. If nobody broke it, publish that honestly and say what that does and doesn't prove. |
| 6 | **Agent vs. The Web, episode 2.** Reader-chosen target from episode 1's vote. |
| 7 | **The Fossil Record, episode 2** — Hacktoberfest bug, real PR. Tag it into whatever Hacktoberfest writing challenge runs. |
| 8 | **Nobody Asked For This, episode 1.** The absurd build with a real payload. This is your reach post; time it for a Tuesday or Wednesday. |

Also in month 2: publish the FinPal error-analysis post as a bonus if you have capacity. Start the public experiment log repo.

### Month 3 (November) — Compound and consolidate

| Week | Publish |
|---|---|
| 9 | **The Spec Is Lying To You, episode 1.** Spec vs. shipped behaviour. |
| 10 | **Agent vs. The Web, episode 3.** By now the format should be recognizable without the series name. |
| 11 | **Break My Implementation, round 2** — harder target, informed by what round 1 taught you. |
| 12 | **Predictions post with a scoring date**, plus a quarter-in-review: what you tested, what you got wrong, what you're doing next. |

### What to measure

Ignore reactions. They're the least informative number DEV gives you and the easiest to inflate with friends.

**Primary (leading indicators of a community):**
- **Substantive comments per post** — comments containing a technical claim, question, or disagreement. Target: 1–2 by month 1, 4–6 by month 3.
- **Returning commenters** — people who comment on more than one post. This is the single truest measure of a community. Target: 5+ distinct repeat commenters by day 90.
- **Contributions** — people who ran your harness, broke your implementation, or submitted data. Target: 10+ across the quarter.

**Secondary:**
- Followers gained per post, and specifically followers gained on non-challenge posts (challenge followers are low-quality).
- Repo stars and forks on experiment repos — forks matter far more than stars.
- Inbound links and citations from outside DEV.

**Diagnostic:**
- Ratio of self-initiated to challenge-driven posts. Target by day 90: **at least 9 of 12 self-initiated.** Right now it's 0 of 10.

### Cross-platform

Keep this light — it's leverage, not a second job.

- **DEV is home.** Everything originates here.
- **GitHub is the proof layer.** Every experiment gets a repo. Your profile currently peaks at 7 stars and 5 followers; the harness repos are what change that, because tools get forked.
- **LinkedIn** (you have a real presence there and it's the right platform for Pune's engineering market) — one post per experiment, framed as the finding, linking back.
- **X/Bluesky** — the finding as a short thread. Agent security researchers are concentrated there and this is the fastest route to being read by people who write specs.
- **Medium** — you have an account. Either canonical-repost your best 3–4 posts or ignore it. Don't split effort.
- **Comment on the source.** When you test something, tell the people who built it — a Chromium bug, a GitHub issue, a WebMCP explainer discussion. Chrome explicitly invites feedback and Chromium bug reports on the WebMCP implementation. One good bug report gets you further with that audience than fifty DEV posts.

---

## 11. Your first 26 content ideas

Ordered roughly by when to publish. Each: what it is, the hook, the series, and why it earns attention.

---

**1. "Shopify Turned On WebMCP By Default in August. I Checked What That Exposed."**
Crawl a sample of newly agent-enabled storefronts, catalogue the tools each exposes, and report the aggregate — how many expose write actions, how many expose anything that costs money.
*Hook:* a number nobody has. *Series:* Agent vs. The Web. *Why:* The default-on change happened in August 2026 and nobody has surveyed the result. Highest-impact single post available to you.

**2. "I Wrote a WebMCP Tool Description That Lies. Three Agents Called It Anyway."**
Register a tool whose description doesn't match its behaviour. Point three agents at it. Publish the transcripts.
*Hook:* adversarial + concrete outcome. *Series:* Agent vs. The Web. *Why:* The spec acknowledges prompt injection and tool-chaining exfiltration without resolving them. This is the demonstration of that gap.

**3. "The Fossil Record #1: [bug title]"**
A real bug in a real OSS repo, symptom to root cause, PR linked, ending with the transferable tell.
*Hook:* forensic, wrong-assumption opener. *Series:* The Fossil Record. *Why:* Your proven format, and DEV's own team publishes in this genre.

**4. "Break My WebMCP Permission Boundary"**
Ship a small tool with a confirmation gate you believe is safe. Publish the source. Two-week window.
*Hook:* the invitation. *Series:* Break My Implementation. *Why:* Converts readers into participants in one step.

**5. "How Many Turns Before an Agent Forgets Its Own Constraint?"**
Give an agent one hard rule, then a long task. Measure the turn at which the rule stops being honoured, across models.
*Hook:* a number that doesn't exist yet. *Series:* Receipts. *Why:* Universally relevant to anyone building agents, needs no hardware.

**6. "[N] of You Broke It. [M] Ways I Hadn't Considered. One I Still Can't Fix."**
The results post. Every contributor named, every break explained, one honest unsolved case.
*Hook:* public defeat. *Series:* Break My Implementation. *Why:* The credibility move. Being beaten in public and saying so is rare and memorable.

**7. "I Put a Hidden Instruction in a Form Label. Two Agents Obeyed It."**
Indirect injection through ordinary page content that a human never sees but an agent reads.
*Hook:* small action, alarming result. *Series:* Agent vs. The Web. *Why:* Indirect injection through content an agent retrieves is the central unsolved attack pattern, and almost nobody demonstrates it on the open web.

**8. "'Too Tidy' Was the First Tell to Die"**
Publish the actual finding from Turing's Mirror playtesting — which heuristics for spotting AI text collapsed first, and which survived longest. Add scoring, gather reader data, publish the aggregate.
*Hook:* an original small dataset about something everyone argues about. *Series:* Receipts. *Why:* This is already the most interesting thing you've said and it's buried in a comment reply.

**9. "I Have 1,000 Real UPI Transactions. Here's What My Classifier Gets Wrong."**
Honest error analysis of FinPal, organised by failure shape, not by accuracy percentage.
*Hook:* the failure, not the launch. *Series:* Receipts. *Why:* You have a real corpus of 1000+ transactions from PhonePe, GPay and bank statements — a genuine asset nobody else has, currently being used as a résumé bullet instead of as evidence.

**10. "I Gave an AI Agent a ₹500 Budget and Told It to Buy Me Lunch"**
Real task, real money, real constraint, full transcript including everything stupid.
*Hook:* absurd-but-real. *Series:* Nobody Asked For This. *Why:* Maximum shareability with a real finding about how agents handle irreversible actions and hard limits.

**11. "The Spec Says Agents 'May' Ask for Confirmation. I Checked What 'May' Means."**
Trace one modal verb in the WebMCP spec through to actual agent behaviour on destructive tools.
*Hook:* pedantry with stakes. *Series:* The Spec Is Lying To You. *Why:* This is exactly the gap between standards text and shipped behaviour that nobody documents.

**12. "provideContext Was Removed in March. The Tutorials Still Recommend It."**
Document the spec's evolution and what silently broke, with a compatibility table.
*Hook:* the thing that's quietly wrong. *Series:* The Spec Is Lying To You. *Why:* The removal is documented and the API surface keeps shifting; being the person who tracks the drift is a durable, uncontested position.

**13. "Your Site Is Now an API and You Didn't Approve It"**
The engineering and consent question raised by agent-readability arriving by default via hosting layers.
*Hook:* stakes-first, mildly alarming, true. *Series:* standalone / discussion. *Why:* Structurally a discussion post with a technical spine — the kind that draws 40+ comments.

**14. "Two Tools on the Same Page Contradicted Each Other. Here's What the Agent Did."**
A deliberate conflict between two registered tools, and how different agents resolve it.
*Hook:* engineered edge case. *Series:* Agent vs. The Web. *Why:* Nobody has tested tool-set consistency. It's the kind of failure that will bite real teams in six months.

**15. "I Made My Portfolio Lie to Agents. Nothing Checked."**
Your own site as the test subject — declare capabilities you don't have and see whether any verification exists anywhere in the chain.
*Hook:* self-implicating. *Series:* Nobody Asked For This. *Why:* Uses a site you already control, costs almost nothing, and the finding is about trust infrastructure that doesn't exist.

**16. "How Much of Your Agent's Context Window Is Spent Re-Reading?"**
Instrument an agent loop and measure token spend on redundant reads.
*Hook:* a wasteful number. *Series:* Receipts. *Why:* Directly connects to a live tooling trend — "Stop Making Your AI Coding Agent Grep Your Whole Repo" is currently trending — but with measurement instead of a recommendation.

**17. "The Fossil Record #2: Hacktoberfest Edition"**
A bug found and fixed during Hacktoberfest, same forensic treatment.
*Hook:* forensic. *Series:* The Fossil Record. *Why:* October gives you a free supply of real bugs in real repos, and the writeup is worth more than the PR.

**18. "Progressive Enhancement for Agents: One Site, Two Audiences, No Duplicate Logic"**
The actual architecture problem of serving humans and agents from one codebase, with the tradeoffs you hit.
*Hook:* a real unsolved design question. *Series:* standalone architecture post. *Why:* Squarely in your Next.js/React expertise, genuinely unanswered, and the format invites architecture argument in the comments.

**19. "I Poisoned an Agent's Memory Once. It Stayed Poisoned."**
Whether a bad memory entry survives resets, and what it costs.
*Hook:* persistence is the scary part. *Series:* Agent vs. The Web. *Why:* Research shows web agents are susceptible to corrupted memory, with injections achieving prompt leakage, exfiltration and goal hijacking, but practitioner demonstrations barely exist.

**20. "Plan-Then-Execute vs. the Naive Loop: I Ran Both 200 Times"**
Implement both patterns on one task, measure failure rates and token cost.
*Hook:* a head-to-head with a real n. *Series:* Receipts. *Why:* This is the benchmark your Hermes-vs-LangChain post should have been. Same instinct, now with evidence.

**21. "What's the Strangest Way an Agent Has Failed on You?"**
A pure discussion post. Seed it with your three best failures.
*Hook:* invitation. *Series:* recurring #discuss. *Why:* Discussion posts routinely pull 40+ comments on DEV for minimal effort, and this one doubles as research for future episodes.

**22. "Five Predictions About the Agent-Ready Web. I'm Scoring These on 1 March."**
Specific, falsifiable, dated predictions with your reasoning.
*Hook:* a commitment with a deadline. *Series:* standalone, recurring annually. *Why:* Guarantees a return-traffic post, and readers who post their own predictions have a reason to come back.

**23. "I Measured How Long AI-Generated PRs Actually Sit in Review"**
Instrument a repo, or analyse public repos, and produce your own numbers on review burden.
*Hook:* independent measurement of a widely-repeated claim. *Series:* Receipts. *Why:* LinearB found AI PRs wait 4.6x longer and Sonar found 96% of developers don't fully trust AI-generated code — everyone cites these; nobody replicates them.

**24. "Break My Classifier: Send Me a Merchant String That Fools FinPal"**
Community bug hunt on your own deployed project.
*Hook:* an easy, fun, concrete ask. *Series:* Break My Implementation. *Why:* Low barrier to participate — a reader can contribute in ten seconds — and it converts an old project into a live community asset.

**25. "The Agent Bought the Wrong Thing. The Site Did Nothing Wrong."**
A case where both the agent and the site behaved correctly and the outcome was still wrong — the interface contract as the failure point.
*Hook:* nobody's at fault and it still broke. *Series:* Agent vs. The Web. *Why:* The most sophisticated framing available in this space, and it's the one that gets you read by people building the standards.

**26. "Ninety Days of Breaking Things: What I Got Wrong"**
Quarterly retrospective. Every prediction you missed, every experiment that produced nothing, every reader who corrected you.
*Hook:* audited self-assessment. *Series:* standalone quarterly. *Why:* Closes the loop, names contributors, and is the post that makes the whole body of work legible as a project.

---

## 12. Stop, reduce, double down, experiment

### Stop

**Stop letting the challenge calendar choose your topics.** This is the whole diagnosis. Ten for ten. Enter challenges when a challenge happens to fit an episode you were going to write anyway — never the reverse.

**Stop asking for stars and reactions in comments.** "visite repo on Github and star repos ......." on your best post, four replies from a genuinely good technical exchange. It costs you the exact readers you want. Delete those comments.

**Stop writing analyses of things you haven't run.** Gemma 4, Hermes vs LangChain, and the WebMCP explainer were your longest posts and your weakest results. In 2026 on DEV, a well-organized explanation of an announcement is indistinguishable from generated content, and readers have explicitly named "Gemma 4 that" and "AI agents vs agents comparisons" as the pattern they're exhausted by.

**Stop using the challenge template as your article structure.** "What I Built / Demo / How I Built It / What I Learned" is a judging rubric. It is not a voice.

**Stop making unfalsifiable claims in titles.** "Compounds while X stays flat," "changes the economics" — if you can't point at the measurement, don't put it in the headline. Either measure it or claim something smaller.

### Reduce

**Reduce showcase posts.** FinPal, Pawscript and the Vada Pav page are "here's a thing I made." Cap these at one per quarter, and only when the build produced a finding.

**Reduce post length where it isn't load-bearing.** Your 7-minute posts underperform your 4-minute posts. The npmx post is 4 minutes and it's the best thing on your profile. Length should come from evidence, not from framing.

**Reduce breadth.** Games, landing pages, finance apps, npm internals, local models, agent frameworks — in five months. Pick the lane and let the rest go, at least until the lane is established.

### Double down

**Root-cause debugging narratives.** Your differentiated skill. Nobody can fake the PR link.

**The transferable closing line.** "Dead parameters are a fossil record of intent the code no longer honors." Every post ends with one heuristic. This is how a voice becomes recognizable.

**Findings extracted from builds.** The playtesting observation in Turing's Mirror is the most interesting thing on your profile and it's a subordinate clause. When a build produces a finding, the finding is the post.

**Real open-source contribution.** The npmx PR is worth more to your credibility than any three showcase posts. Keep shipping fixes to projects you actually use, and write up the ones with a lesson.

**Publishing your own errors.** "I got this one wrong myself, re-reading it cold a day later." That sentence is why people trust you. More of it.

### Experiment

**Discussion posts.** Zero so far. One per week. Lowest effort-to-engagement ratio on the platform.

**Public adversarial challenges.** Break My Implementation is untested for you and has the highest ceiling of anything here.

**Behavioural benchmarks with published harnesses.** Nobody on DEV is doing agent-behaviour benchmarks that don't require expensive hardware. That gap is yours to take.

**Follow-up posts.** You've never written one. "I said X three weeks ago. Here's what actually happened." Follow-ups build the sense of a continuing story, which is the actual mechanism behind people returning.

**Being wrong in public on purpose.** Predictions with a scoring date. Nothing else buys credibility faster.

---

# Final strategy

### Positioning

**The developer who points agents at real systems, breaks them, and shows you exactly where they fall apart.**

Not an AI explainer, not a tutorial writer, not a build-in-public founder. Someone who runs the experiment everyone else is only discussing, publishes the raw data, and names the person who proves him wrong.

### Audience

Mid-to-senior full-stack and backend engineers who are being asked to make their product "agent-ready" and aren't sure what that means or whether it's safe — plus the AI engineers on the other side of that wire, plus the appsec people watching agentic browsing arrive. Deliberately not beginners. Smaller audience, far more valuable, and the one that actually comments.

### Content pillars

1. Agent-facing interfaces and what breaks in them (WebMCP, browser agents, tool contracts)
2. Adversarial testing and agent security in practice
3. Root-cause debugging in real codebases
4. Behavioural measurement — small honest benchmarks with public harnesses
5. Building for two audiences at once: humans and agents

### Signature series

**Agent vs. The Web** (biweekly, flagship) · **The Fossil Record** (monthly) · **Break My Implementation** (six-weekly, community engine) · **Nobody Asked For This** (monthly, reach) · **Receipts** (monthly) · **The Spec Is Lying To You** (six-to-eight weekly)

### Community concept

**People participate when they can beat you, and when being right about it is visible.**

Every post ships a repo they can run, an implementation they can break, or a claim they can disprove — and every contribution gets named in the follow-up, with a link to their profile. Not "thanks for reading." Not "what do you think?" A specific, adversarial, credited invitation. Passive readers become contributors in one step, and contributors come back because their name is in the next post.

### Content style

Short. Evidence-dense. Adversarial but not cynical. Written in first person about a specific thing that happened on a specific day, with the wrong turns left in.

Every post contains at least one artifact that cannot be generated — a PR link, a DevTools screenshot, a raw number, a transcript, an admission of error. Every post ends with one heuristic a reader can carry into a codebase they've never seen. Four to six minutes, never seven-minute framing. Keep the voice you have; anchor it in evidence so nobody can mistake it for a machine's.

### 90-day plan

One substantial post weekly, one discussion post weekly, 8–10 substantive comments weekly on other people's work, replies to every comment within 24 hours.

- **September** — launch Agent vs. The Web with the Shopify/Cloudflare exposure audit; Fossil Record #1; open Break My Implementation round 1; Receipts #1. Rewrite the bio, pin the two strongest posts.
- **October** — publish Break My Implementation results with every contributor named; Agent vs. The Web #2 on a reader-chosen target; Fossil Record #2 via Hacktoberfest; Nobody Asked For This #1.
- **November** — The Spec Is Lying To You #1; Agent vs. The Web #3; Break My Implementation round 2; predictions with a scoring date plus the quarterly retrospective.

Measure returning commenters, substantive comments, and contributions. Ignore reactions. Target by day 90: at least 9 of 12 posts self-initiated rather than challenge-driven.

### Biggest opportunity

**A major browser standard is shipping with an acknowledged, unresolved security hole, it went default-on across two large hosting layers in August, and the entire developer-facing coverage of it is explainers.**

WebMCP went default-on across Shopify storefronts and Cloudflare-fronted websites in August 2026. Its own specification acknowledges prompt injection and data exfiltration through tool chaining as unresolved. OWASP calls prompt injection architecturally unsolved and Black Hat 2026 concluded AI browsers remain vulnerable despite guardrails. Thousands of sites became agent-callable without their owners choosing it, and nobody has surveyed what that exposed.

You wrote in May that WebMCP was the most important thing announced at I/O and almost nobody was talking about it. You were right, and the window is still open — but it's now open for the person who *tests* it, not the person who announces it. That's a six-to-twelve month window before either the tooling matures or the coverage saturates.

### Biggest mistake to avoid

**Publishing before you've run the experiment.**

The entire strategy rests on one thing being true: that when you claim something, you actually did it. The moment you publish an "I tested X" post where you didn't really test X — or where the test was thin and the conclusion was borrowed — the position collapses, and it collapses permanently, because the whole value proposition was that you're the one who checks.

This will be tempting, because running real experiments is slow and the DEV challenge calendar will keep offering you easy posts with guaranteed traffic. Two posts a month that you genuinely ran will build something. Eight posts a month where half are reheated announcements will build nothing, and will make you exactly the thing the community is currently revolting against.

The secondary mistake, closely related: **staying a reader instead of becoming a participant.** Twelve comments in five and a half months is the real constraint on your growth right now, not your writing. The writing is already good enough. Nobody knows you exist.
