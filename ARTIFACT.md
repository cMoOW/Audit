
# A Goodhart audit for AI infrastructure (notes for the future me)
**Audience:** me, a few years from now, when I am deep in a spreadsheet and starting to trust the columns more than the mess behind them.

**What is the purpose of this:** As my time at Brandeis winds down, I can see how much the curriculum I engaged with shaped how I think. A lot of what we learn is a technique: how to interview, how to build a portfolio, how to optimize a schedule, and how to translate course material into solvable problem structures. Those frameworks are useful, but they rarely ask, "Is this what I actually want?". It assumes the question has already been answered and doesn't revisit it again. The same tension shows up in supply chains and fabs. People converge on legible numbers because coordination is hard, but the numbers are not the full system. This document is a pause. What I can put in a model, what I compress it into, and what gets dropped, what does Elul teach us and how does it apply here.  

Nothing here is investment advice. These are illustrative indicator types from public reporting.

---

## How to read this (how the parts connect)

| Part | What I am doing | Course concept connection |
|------|------------------|---------------------------|
| **1** | List the public, repeatable inputs that fit cleanly in a spreadsheet across the AI supply chain. | **Measurement and legibility**: what gets counted because it can be counted. |
| **2** | Show how those inputs get compressed into one storyline. | **Goodhart / optimization pressure**: the map starts steering the system. |
| **3** | Name what still matters but does not survive the scoreboard cleanly. | **Ellul's technique**: efficiency decides what gets first-class attention. |
| **4** | Reflect on where Brandeis CS habits help me and where they mislead me in this domain. | **Course tie in**: correctness vs. partial observability and ambiguity. |
| **Closing** | Just an honesty check; something more than just being self aware in my work.

**My main point:** I and many others cannot work without metrics, but metrics steer what I see, and this doc I hope highlights how it does so by drawing from what we learned in class but in a way that doesn't stretch anything. 

---

## Part 1 — What I can put in the spreadsheet (legible inputs)
These are signals that show up in public channels: earnings, trade press, vendor commentary, analysts, and sometimes government filings. I group them across the chain so I do not treat "AI" as one node.
**Demand / pull (downstream of silicon)**  
- Stated hyperscaler capex and segment revenue growth (cloud + "AI" line items where broken out)  
- Order patterns for AI servers and racks (lead times, backlog language, allocation language)  
- Power: announced MW, region 
**Compute and memory**  
- Accelerator attach rates and generation cadence (what class of module ships, and in what volume band)  
- HBM capacity adds, stack complexity, and packaging-related constraints  
- High-bandwidth link budgets inside the rack (what has to keep scaling for next-gen topologies)  
**Packaging and assembly**  
- Advanced packaging capacity (interposer / 2.5D-style flows): tool adds, cycle time, yield  
- Substrate supply: glass vs. organic, supplier concentration, and allocation signals  
- OSAT bottlenecks where front-end supply exists but back-end packaging and test slow delivery  
**Silicon manufacturing**  
- Leading-edge ramp commentary, utilization changes, and yield hints  
- Photomask cycle times and specialty chemical lead times as early warning signals  
**Photonics and interconnect (when the bottleneck moves off the die)**  
- Optical transceiver generation mix (speed class, DSP, power draw)  
- Co-packaged or near-package optics progress (increasingly relevant)  
- Fiber plant and physical layer buildout between campuses (load-bearing)  
**Energy**  
- Interconnect queue depth and expected timeline for new generation and transmission  
- PPA price bands and curtailment risk: cheap on paper vs. usable in practice  
- On-site backup, storage, cooling, and water constraints  
**Upstream materials**  
- Wafer supply, specialty gases, and CMP consumables  
- Specialty chemistry and metals exposure in bonding and plating paths  

These are the cells I can fill each quarter with public, repeatable signals. That is the point of this section. This is what is legible and socially acceptable in a serious memo. It is useful, but it is not the whole system. Once I collect these inputs, I still have to compress them into a single decision story. That compression is where Goodhart pressure starts.

---

## Part 2 — The compression (what I optimize the story into)

Over time, the stack gets flattened. Not because people are lazy and want to do less work, but because people need one representation to act on.
Typical compressions:
1. **Single bottleneck of the quarter** — Calling one thing "the bottleneck" helps people align fast. In reality, bottlenecks are linked, and fixing one layer can move pressure somewhere else in the chain.  
2. **Capacity vs. price** — The sharpest line on the chart often gets treated as the true constraint. That can miss constraints that do not show up cleanly in price, especially policy, permitting, and contract structure.  
3. **Vendor share shifts** — Share changes are easy to measure and easy to debate, so they dominate discussion. Sometimes that is valid; sometimes it distracts from physics and execution bottlenecks.  
4. **A one page timeline** — Build dates, ramp targets, and tool installs make execution look linear. In practice, dependencies slip and uncertainty is usually larger than the timeline suggests.  
5. **A scoreboard** — Announced MW, capex raises, and memory pre-buys are easy to rank. Ranking can replace reasoning, and strategy turns into a leaderboard.  

“This is Goodhart in practice: a simplified model starts as a coordination tool, then becomes the thing everyone optimizes, even when it no longer matches the full system.”“At first the map is just a tool for alignment. Then it becomes the target, and whatever the map leaves out gets treated as secondary.”

---

## Part 3 — What this scoreboard cannot see 
Once the story is compressed into a scoreboard, there are still other constraints that matter. I am not saying they are automatically more important but I am saying they do not survive spreadsheet translation cleanly, even though they still shape outcomes.
- **Yield learning curves inside one line** — nonlinear and mostly proprietary, so public views get smoothed.  
- **Tool matching problems** — nominal capacity exists, but the wrong chamber mix blocks the needed recipe.  
- **Human capital in maintenance and field service** — throughput often breaks here before design capacity is the issue.  
- **Permitting and local politics** — same MW target, completely different calendar depending on location.   
- **Trust and contract behavior under stress** — who ships to whom when allocation gets tight.  
- **Export controls and policy path dependence** — rules move the feasible set faster than most models update.  
- **Photonics integration risk** — interoperability and field reliability lag demos by years.  
- **Second-order herding effects** — everyone rushing the same fix often creates the next bottleneck.  
- **Qualitative field checks** — conference chatter, engineering hiring signals, supplier responsiveness; messy, but sometimes early.  
- **What I avoid because it is cognitively expensive** — labor conditions, environmental externalities, community impact.  

In Ellul’s terms, efficiency decides what gets treated as primary. What gets dropped is still real, it just falls outside the frame I use to make decisions.

---

## Part 4 — The clash in mindset, what Brandeis taught me, what industry values(where they meet and where they diverge)

**Where they meet**  
- Both value clarity: state assumptions, define constraints, separate knowns from inferences.  
- Both rely on abstraction to handle complexity without drowning in detail.  
**Where they diverge**  
- CS assignments often have a concrete spec and a right shaped answer. Create a program that produces this solution and output, or complete this problem set using tools and techniques taught in class. Supply chains are partially observable and strategically opaque by design.  
- Classes reward correctness and elegance. Industry often rewards being early enough, robust enough, and not wrong in expensive ways.  
- In class, closing the loop is usually success. In this domain, closing the measurable loop can still be self-deception.  
So future me: keep what Brandeis taught you about precision, structure, and being explicit about assumptions. That discipline matters. But do not confuse formal clarity with completeness. If something cannot be cleanly formalized, that does not make it irrelevant. It usually means the system is more complex than the model you are using.

---

## How to revisit this doc
- If I only revisit parts 1 and 2 and 3 as a simple disclaimer, skipping over the point then this document failed.  
- If Part 3 actually changes what I do next, who I call, what I re-check, what I delay, and what I think about twice rather than mindelessly oversimplify then it did its job.  
- If I end up making the same decisions in the same way, then this is just moral flourish, and I failed to make reflection as practice.  
- I wrote this because I know I need metrics, and I will keep using them. The point is not to reject measurement. The point is to stay honest about what measurement leaves out, and to make decisions with that gap in view instead of pretending it is not there.
