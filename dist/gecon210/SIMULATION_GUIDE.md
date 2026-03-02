# Solow Growth Model Dashboard — A Layman's Guide

## What is this dashboard about?

This dashboard helps explain **why some countries are richer than others** and **why growth rates change over time**, using the Durabuild case study (France vs the United States, 1950–2000). It uses the **Solow Growth Model** — one of the most important frameworks in economics for understanding long-run growth.

The core idea is simple: **an economy's output depends on three things — technology, capital (machines/factories), and labor (people working)**. The model shows how these interact over time.

---

## Tab-by-Tab Guide

### 1. Solow Model Simulation

**What it does:** An interactive playground where you can adjust a country's economic conditions and watch how GDP per capita evolves over 100 years.

**The key equation:** Output = Technology × Capital × Labor, or:

> Y = A × K^α × N^(1-α)

In plain English: GDP depends on how good your technology is (A), how many machines and factories you have (K), and how many people are working (N).

**The sliders:**
- **Savings Rate (s):** What fraction of GDP gets reinvested into new machines/factories. Higher savings → more capital → richer in the long run. But there are diminishing returns — doubling your savings doesn't double your income.
- **Depreciation (δ):** How fast existing capital wears out. Machines break, buildings crumble. Higher depreciation means you need more investment just to stay in place.
- **Population Growth (n):** How fast the workforce is growing. More workers means capital gets spread thinner — each person has fewer machines to work with.
- **Technology Growth (g):** How fast technology and efficiency improve. This is the **only source of permanent growth** in the Solow model. Everything else eventually levels off.
- **Capital Share (α):** What fraction of income goes to capital owners vs workers. Typically around 30%.
- **Initial TFP (A₀):** Starting level of technology/efficiency.
- **Initial k̃:** Starting capital per worker (adjusted for technology).
- **Labor Participation (N/POP):** What fraction of the population is actually working.

**The charts:**
- **GDP per Capita Path:** Shows where the economy is heading. The red line is the actual path; the gold dashed line is the "steady state" — the long-run destination.
- **Capital per Worker:** Shows capital building up over time until it plateaus.
- **Solow Diagram:** The classic textbook diagram. Where the green curve (investment) crosses the red line (break-even), that's your steady state.
- **Growth Rate:** Growth starts high when you're poor (lots of room to grow) and gradually slows as you approach steady state.

**Case Presets:** Click these to load real-world parameters:
- **US 1950:** Already near steady state, growing steadily at ~2%.
- **France 1950:** Low capital after WWII, rapid catch-up growth (this is the Durabuild story).
- **France 1980:** Approaching steady state, growth slowing. Grandpa Frank should have noticed this.
- **China 2000:** Very high savings (45%), rapid industrialization.
- **Philippines scenarios:** Different hypothetical paths for the PH economy.

**Key takeaway:** Countries that are far below their steady state grow fast (catch-up growth). But this growth is temporary — it slows down as you approach the steady state. Only technology improvement (g) drives permanent growth.

---

### 2. Case Exhibits

**What it does:** Reproduces the key exhibits from the Durabuild case using actual Penn World Table (PWT) 11.0 data.

**Exhibit 1 — GDP per Capita Chart:**
Shows France rapidly converging toward the US from 1950 to the mid-1970s, then the gap stabilizing. This is the central puzzle of the case: why did France stop catching up?

**Exhibit 2 — GDP Decomposition:**
This is the most important table. It breaks down the France/US GDP gap into three components:

> GDP per capita = Technology × Capital per Worker × Labor Participation

Or: Y/POP = A × (K/N)^0.3 × N/POP

All numbers are France ÷ US ratios. A value of 1.00 means France equals the US.

| Year | Y/POP | Technology (A) | Capital (K/N)^0.3 | Labor (N/POP) |
|-|-|-|-|-|
| 1950 | 0.57 | 0.61 | 0.82 | 1.14 |
| 1980 | 0.88 | 0.95 | 1.02 | 0.91 |
| 2000 | 0.79 | 0.99 | 0.93 | 0.86 |

**How to read this:**
- In **1950**, France was at 57% of US GDP per capita. The main reason? Technology (A = 0.61) — France was far behind. But France actually had *more* people working relative to population (1.14).
- By **1980**, France jumped to 88%. Technology nearly caught up (0.95). Capital matched the US (1.02). But labor started falling (0.91) — fewer French people were working.
- By **2000**, France fell back to 79%. Technology fully caught up (0.99). But labor dropped further (0.86) — the 35-hour work week, long vacations, early retirement, and high unemployment pulled France back.

**The verification trick:** Multiply the three components: 0.61 × 0.82 × 1.14 = 0.57. It checks out!

**What Changed (PWT 7.1 vs 11.0):**
The case was originally written with older data (PWT 7.1). With updated PWT 11.0 data, the story is broadly the same but the numbers shift slightly. The dashboard shows both versions side by side.

---

### 3. Case Projections (Historical Data)

**What it does:** Shows the full year-by-year actual data from 1950 to 2023 for both the US and France.

**The columns explained:**
- **Population:** Total population in millions.
- **Labor (N):** Persons engaged — how many people are actually working, in millions.
- **Capital (K):** Total value of a country's machines, buildings, roads, and infrastructure. Measured at current purchasing power parities (PPPs) so you can compare across countries.
- **K/N:** Capital per worker — how much capital each worker has. More capital per worker generally means higher productivity.
- **TFP (A):** Total Factor Productivity — a catch-all measure of efficiency. Includes technology, management quality, institutions, rule of law, education quality, etc. Computed as: A = GDP ÷ (K^0.3 × N^0.7). It's everything that affects output beyond just having more capital and labor.
- **GDP (Y):** Real GDP — total economic output at constant prices.
- **Investment (I):** How much of GDP was spent on new capital (savings rate × GDP).
- **Depreciation:** How much existing capital wore out that year.
- **Y/Pop:** GDP per capita — output per person. The standard measure of living standards.
- **Growth:** Annual growth rate of GDP per capita.

**France/US Ratios table:** Shows France as a fraction of the US for each component, year by year. Watch how the ratio changes over time — this tells the convergence story in detail.

---

### 4. Growth Accounting

**What it does:** Visualizes the Exhibit 2 decomposition with charts and year-by-year interpretation.

**The three bar charts (1950, 1980, 2000):**
Each bar shows how far France is from the US on each component. Bars above 1.0 mean France is ahead; below 1.0 means France is behind.

**The story in three acts:**

**Act 1 — 1950 (France at 57%):** France is recovering from WWII. Technology is the big gap (0.61). Capital is also below the US (0.82). But more French people are working relative to population (1.14) — this partly offsets the other gaps.

**Act 2 — 1980 (France at 88%):** The golden age of catch-up. Technology nearly closed the gap (0.95). Capital investment paid off — France now has MORE capital per worker than the US (1.02). But warning signs: labor participation dropped to 0.91. Fewer French people are working.

**Act 3 — 2000 (France at 79%):** Technology fully caught up (0.99) — France is just as efficient as the US. But GDP per capita fell back because of labor (0.86). The 35-hour work week, mandatory 5-week vacation, generous unemployment benefits, strict firing laws, and high minimum wage all reduced how many people were working. Capital also dipped slightly below the US (0.93).

---

### 5. Convergence Analysis

**What it does:** Explains *why* the Solow model predicts that poorer countries should grow faster, and why France's convergence stopped.

**Two types of convergence:**
- **Absolute convergence:** The naive idea that ALL poor countries will catch up to rich ones. The Solow model does NOT guarantee this.
- **Conditional convergence:** Countries will converge IF they have similar economic fundamentals (savings rates, institutions, policies). This is what the Solow model actually predicts.

**The France case proves conditional convergence:**
- Capital per worker? **Converged.** France matched the US by 1980.
- Technology? **Converged.** France reached 99% of US TFP by 2000.
- GDP per capita? **Did NOT converge.** Because the "conditions" diverged — France chose different labor market institutions than the US.

**The three big numbers for 2000:**
- **(K/N)^0.3 = 0.93** — Capital: slightly below the US
- **TFP = 0.99** — Technology: fully converged
- **N/POP = 0.86** — Labor: diverged (this is the problem)

**Philippines section:** Applies the same framework to the Philippines. The PH has the *initial conditions* for catch-up growth (low capital, high potential returns) but lacks the *structural conditions* — savings rate is only 23% of GDP (vs China's 43%), TFP growth has been weak historically, and brain drain exports productive workers.

---

### 6. Policy Analysis & China

**What it does:** Applies the Solow model to evaluate Lisa's question from the case: will China's high growth persist?

**The key insight:** Growth from capital accumulation is **temporary**. Only technology growth (g) is **permanent**. China's 45% savings rate drives incredibly fast capital accumulation, but eventually diminishing returns will kick in — just like they did for France.

**Two policy levers illustrated:**
- **Savings Rate:** Higher savings → higher steady state → richer long-run. But diminishing returns mean going from 20% to 40% doesn't double your income.
- **Labor Participation:** This is a direct multiplier on GDP per capita. France lost 28% of its GDP gap to the US from labor alone.

**China Scenario Builder:** Adjust China's parameters and see projected outcomes. The one-child policy effect is modeled: after a certain number of years, population growth turns negative, which actually *raises* capital per worker (fewer people to share capital with).

---

## The Big Takeaways for Your Group

1. **Capital accumulation has diminishing returns.** Building more factories helps, but each additional factory adds less output than the last. This is why fast-growing countries eventually slow down.

2. **Technology (TFP) is the only source of permanent growth.** In the long run, the only way to keep getting richer is to keep getting more efficient — better technology, better management, better institutions.

3. **Labor policies matter more than you think.** France's technology and capital fully caught up to the US. But France still fell behind because fewer people were working. The 35-hour work week and generous social policies had real economic costs.

4. **Convergence is conditional, not automatic.** Poor countries CAN catch up to rich ones — but only if they have the right institutions and policies. Simply being poor doesn't guarantee fast growth.

5. **China's growth will slow.** The Solow model predicts it clearly. The question is not *whether* but *when* and *to what level*. The answer depends on technology growth and what happens with the aging population (one-child policy effects).

6. **For Grandpa Frank:** The Solow model would have told him in the 1980s that France's catch-up growth was ending. Capital had converged, TFP had converged, and labor was declining. He should have expected growth to slow — and adjusted his business strategy accordingly.
