# How to Read the Solow Model Dashboard

A panel-by-panel guide for LT5 | EMBA2027 | Brizuela, Magbitang, Pascua, Valencia

---

## Tab 1: Solow Model

This is the core simulation. Everything here is driven by the **two equations** at the top:

- **Production function**: Y = A · K^α · L^(1-α) — total output is a function of technology (A), capital (K), and labor (L)
- **Capital accumulation**: Δk̃ = s·f(k̃) - (n+g+δ)·k̃ — how capital per effective worker changes each period

### Left Panel: Parameters

Each slider controls one variable in the model. Drag any slider and all four charts update instantly.

| Parameter | What it means | Key intuition |
|-|-|-|
| **s** (Savings Rate) | Fraction of output invested in new capital | Higher s → more investment → higher steady-state k* and y* |
| **δ** (Depreciation) | Fraction of capital that wears out each year | Higher δ → more replacement needed → lower k* |
| **n** (Population Growth) | Annual growth rate of the workforce | Higher n → capital spread thinner across more workers → lower k* per worker |
| **g** (Technology Growth) | Annual TFP growth rate | The ONLY source of permanent growth in the Solow model. This is the single most important parameter. |
| **α** (Capital Share) | Output elasticity of capital (typically 0.30) | How much of national income goes to capital vs labor. α < 1 is what creates diminishing returns. |
| **A₀** (Initial TFP) | Starting technology level relative to the US | France 1950 ≈ 0.99 (nearly equal tech); China 2000 ≈ 0.40 (far behind) |
| **k̃₀** (Initial capital/eff. worker) | Where the economy starts on the transition path | Low k̃₀ = far from steady state = fast growth (this is the catch-up story) |
| **N/POP** (Labor Participation) | Persons engaged per capita (employment-to-population ratio) | Not in the Solow equation directly, but multiplies output per capita. France's decline from 1.14 to 0.86 is why it fell behind. |

### Left Panel: Case Presets

Pre-loaded parameter sets calibrated to real countries and time periods. Click one and the simulation resets with those values. Use these to demonstrate specific points:

- **France 1950** → Shows rapid catch-up growth (low initial k̃, far from steady state)
- **France 1980** → Near steady state, growth has slowed — this is the punchline of the case
- **US 1950** → Already near steady state, stable ~2% growth
- **China 2000** → High savings (35%), rapid industrialization — the question Lisa faces
- **PH Baseline** → Low everything — shows the potential but also the structural barriers

### Left Panel: Steady State Box

Four computed values that summarize the long-run outcome:

- **k̃\*** — The steady-state capital per effective worker. Where the economy is heading.
- **ỹ\*** — The steady-state output per effective worker.
- **SS Growth** — The steady-state GDP per capita growth rate. Always equals g (technology growth). This is the key Solow insight: only technology drives permanent growth.
- **Yrs to 90%** — How many years until the economy reaches 90% of steady state. This measures transition speed.

### Right Panel: Four Charts

#### 1. GDP per Capita Path (top, large)
- **Red line**: Actual GDP per capita over time, starting from the initial conditions
- **Gold dashed line**: The steady-state path (what GDP would be if already at k̃*)
- **How to read it**: The gap between red and gold shows how far the economy is from steady state. When they converge, transition growth is over and only g remains.
- **Key demo**: Load France 1950 — see the red line climb rapidly toward the gold line. Load France 1980 — they're almost touching, meaning growth has already slowed to g.

#### 2. Capital per Effective Worker (bottom-left)
- **Red line**: k̃ over time
- **Gold dashed line**: k̃* (the target)
- **How to read it**: This is the core Solow mechanism. Capital per effective worker rises when investment exceeds break-even, and stops at k̃*. The concave path reflects diminishing returns — each additional unit of k adds less and less.

#### 3. Solow Diagram (bottom-right)
This is the textbook diagram that shows WHY there's a steady state and WHY there are diminishing returns.

- **Green curve** — s·f(k̃) = s·k̃^α: The savings/investment curve. It's **concave** (curves downward) because of diminishing returns to capital. Each extra unit of k̃ produces less additional output, so less additional investment.
- **Red line** — (n+g+δ)·k̃: The break-even line. This is **linear** (straight). It shows how much investment is needed just to keep k̃ constant — replacing depreciated capital (δ), equipping new workers (n), and keeping up with technology (g).
- **Gold dot** — Current k̃ position on the diagram.
- **How to read it**: Where the green curve is ABOVE the red line, k̃ is growing (investment > break-even). Where they CROSS is k̃* — the steady state. Where the red line is above, k̃ is shrinking.
- **Diminishing returns**: The green curve flattens out as k̃ increases. This is why growth slows down — you need more and more capital to generate the same incremental output. Eventually the concave curve can't stay above the straight line, and growth stops at k̃*.
- **Key demo**: Increase s — the green curve shifts UP, creating a new (higher) intersection. But notice the gain gets smaller each time you increase s. That's diminishing returns to savings.

#### 4. GDP per Capita Growth Rate (bottom)
- **Red line**: Growth rate over time
- **Gold dashed line**: Steady-state growth rate (= g)
- **How to read it**: Growth starts high when far from steady state (transition growth + g), then decays toward g. This is the most direct visualization of the Solow prediction: growth is temporary from capital accumulation, permanent only from technology.
- **Key demo**: Load China 2000 — see the very high initial growth that gradually declines. This is exactly the pattern Lisa should expect for China.

---

## Tab 2: Growth Accounting

This tab decomposes the France/US GDP per capita gap using the identity:

**Y/POP = A · (K/N)^α · (N/POP)**

All values are **France/USA ratios** from Penn World Table 11.0. A value of 1.00 means France equals the US; below 1.00 means France is behind.

### France/US Ratios Table

| Column | What it measures | Example: 1950 value of 0.57 means... |
|-|-|-|
| **Y/POP** | GDP per capita ratio | France produced 57% of US GDP per person |
| **A (TFP)** | Total factor productivity ratio | France's technology/efficiency was 61% of the US |
| **(K/N)^0.3** | Capital intensity ratio (raised to α) | France's capital per worker, adjusted for diminishing returns, was 82% of the US |
| **N/POP** | Labor utilization ratio | France had 14% MORE persons employed per capita than the US |

The verification row confirms: A × (K/N)^α × N/POP = Y/POP (the decomposition is exact).

### Three Period Cards (1950 / 1980 / 2000)

Each card shows a horizontal bar decomposition — which factor contributed most to the gap in that year.

- **1950**: The gap (Y/POP = 0.57) was driven by lower TFP (A = 0.61) and capital (0.82). Post-war France hadn't yet adopted US production methods. Labor was slightly ABOVE the US (1.14) — more of the population was working.
- **1980**: Convergence peaked (Y/POP = 0.88). TFP nearly closed (0.95). Capital at near-parity (1.02). But labor started falling (0.91) as welfare state policies reduced participation.
- **2000**: Reversal (Y/POP = 0.79). TFP at parity (0.99), capital slightly below (0.93). The primary drag is labor (0.86) — lower employment rates, high unemployment (11%).

### Growth Rate Decomposition Chart

Stacked bar chart showing France's GDP-per-worker growth by decade, split into:
- **Capital deepening** (dark red): Growth from accumulating more capital per worker
- **TFP** (light red): Growth from becoming more efficient (Solow residual)
- **US total growth** (blue): Benchmark for comparison

**Key pattern**: France grew faster than the US in the 1950s-60s (catch-up), then growth collapsed in the 1980s-90s. TFP was the main driver of France's high growth, not just capital accumulation.

---

## Tab 3: Game Theory

This tab applies strategic decision-making frameworks to Lisa's China entry question from the case.

### Panel 1: Decision Under Uncertainty

A single-player expected value calculation. Durabuild faces two scenarios:
- **High growth continues** (with probability P) → entering China pays off
- **Growth slows** (with probability 1-P) → entering China loses money

**How to read**:
- E[Enter] = P × (Enter+High) + (1-P) × (Enter+Slow)
- E[Stay Out] = Stay Out payoff (regardless of what happens)
- **Optimal decision**: whichever has higher expected value
- **Break-even probability**: The exact P where E[Enter] = E[Stay Out]. Below this, don't enter.

**Key demo**: Drag P(High Growth) down until the optimal flips from ENTER to STAY OUT. That break-even is the critical threshold for Lisa's decision.

### Panel 2: Strategic Entry Game (2-Player)

A simultaneous-move game where both Durabuild and a Competitor decide whether to enter China.

**Payoff matrix**: Each cell shows (Durabuild's payoff, Competitor's payoff).
- **Green highlighted cells** = Nash Equilibrium (neither player wants to deviate)
- The analysis below the matrix explains the Nash equilibrium and whether either player has a dominant strategy.

**How to read**: If "Both Enter" payoff is low (market crowding), there may be a coordination problem — both want to enter alone, but if both enter, both suffer.

### Panel 3: Sequential Decision Tree

What if Durabuild moves first (invest in assessment), then decides?
- Shows the decision tree with expected values at each node
- Demonstrates the value of information — paying for assessment changes the optimal strategy

### Panel 4: Mixed Strategy Equilibrium

When no pure-strategy Nash exists:
- Shows the probability each player should randomize with
- The chart shows expected payoffs as a function of entry probability

### Panel 5: Sensitivity Chart

- **X-axis**: P(growth continues) from 0% to 100%
- **Red line**: E[Enter] as P changes — slopes upward
- **Blue dashed line**: E[Stay Out] — flat (doesn't depend on P)
- **Gold vertical line**: Break-even probability
- **How to read**: Everything to the RIGHT of the gold line = enter. Left = stay out.

---

## Tab 4: Convergence

This tab shows the Solow model's predictions about whether poor countries catch up to rich ones.

### Comparative GDP per Capita (Index = 100)

All four countries start at 100 (their own starting GDP). The chart shows relative growth trajectories.
- **Steeper curve** = faster growth
- **Flattening curve** = approaching steady state
- **Key insight**: China and Philippines grow faster than US/France because they start further from steady state (higher marginal product of capital)

### Growth Rate Convergence

Shows growth rates over time for all four countries.
- **All lines converge toward their respective g** — this IS the Solow prediction
- Countries with low initial k̃ start with high growth (transition) then slow down
- The US line is nearly flat — already at steady state

### Capital-to-Labor Ratio Convergence

Shows k̃ paths — how capital per effective worker evolves.
- France converges toward the same k̃* as the US (conditional convergence)
- China rises rapidly from a low base
- Philippines rises slowly (low savings rate)

### Conditional vs Absolute Convergence (Big Numbers Panel)

Three key 2000 ratios that tell the France story:
- **(K/N)^0.3 = 0.93** (yellow) — France slightly below US capital intensity.
- **TFP = 0.99** (green) — Technology fully converged. France adopted US methods.
- **N/POP = 0.86** (red) — Labor DIVERGED. This is the gap.

**Punchline**: The Solow model predicted capital and technology convergence correctly. But France's steady state is LOWER than the US because of institutional differences (labor market regulations). This is CONDITIONAL convergence — same model, different steady states.

### Philippines Panel

Shows why the Philippines hasn't converged despite Solow predicting it should:
- GDP per capita only 14% of US
- Low TFP (~0.35), low capital, moderate LFPR (64%)
- Has initial conditions for catch-up but lacks structural conditions (savings, TFP growth, human capital retention)
- Brain drain via OFW exports productive workers; remittances go to consumption not investment

---

## Tab 5: Policy Analysis & China Application

This tab connects the Solow framework to Lisa's decision about China.

### Policy Lever: Savings Rate

- **Chart**: Steady-state y* as a function of savings rate
- **Blue dot**: US (s = 20%)
- **Green dot**: China (s = 45%)
- **How to read**: The curve is concave — doubling s does NOT double y*. This is diminishing returns to savings. China's unprecedented 45% rate creates high k* but with diminishing payoff per additional percentage point.

### Policy Lever: Labor Participation

- **Chart**: GDP per capita as a function of N/POP
- **Red dot**: France 2000 (0.86)
- **Blue dot**: US (1.0)
- **How to read**: This is LINEAR — unlike savings, labor participation has a direct proportional effect. France's 14% labor gap translates directly to 14% lower GDP per capita. No diminishing returns here.

### China Scenario Builder

Six sliders that let you project China's GDP path under different assumptions:

| Slider | What to adjust | Why it matters |
|-|-|-|
| **China Savings Rate** | Currently 45%, historically unprecedented | What if it falls as China develops? |
| **China TFP Growth** | Currently 3.5% | Can China keep innovating, or will it plateau like France? |
| **China Pop Growth** | Currently 0.5%, declining | One-child policy aftermath — workforce is shrinking |
| **Regulatory Friction** | 0-1 scale (1 = no friction) | Difficult regulatory environment mentioned in case |
| **Technology Adoption** | 0-1 scale (1 = full frontier adoption) | How quickly China absorbs global best practices |
| **One-Child Pop Effect** | Years until demographic impact hits | When the aging workforce starts dragging growth |

**Three output boxes**:
- **China Projected k*** — Where China's capital per effective worker is heading
- **China Projected y*** — Steady-state output per effective worker
- **Peak Growth Rate** — Maximum growth rate during transition (before diminishing returns kick in)

**Key demo for the group**: Start with defaults (optimistic), then reduce TFP growth to 1.5% and increase regulatory friction to 0.50 — watch how dramatically the projection changes. This shows the uncertainty Lisa faces.

---

## Tab 6: References & PWT Guide

This tab is the data methodology appendix. Key sections:

### Parameter Sources
Lists where each model parameter comes from (PWT, World Bank, national census, etc.)

### Penn World Table 11.0
- Access links: GGDC website, FRED, and the query tool
- Citation requirement (Feenstra, Inklaar & Timmer 2015)
- What changed from PWT 7.1 (used in the original case) — PPP benchmarks, capital stock revisions, data extended to 2023

### Key PWT Variables
Table mapping PWT variable codes to economic concepts:
- `rgdpna` → Y (real GDP at constant national prices)
- `cn` → K (capital stock at current PPPs — used for cross-country comparison)
- `rnna` → K (capital stock at constant national prices — used for time-series within a country)
- `emp` → N (persons engaged)
- `pop` → population
- `hc` → human capital index
- `labsh` → labor share (alternative to assuming α = 0.3)

### How to Replicate Exhibit 2
Step-by-step instructions for computing the France/US decomposition from raw PWT data.

### Growth Accounting (Solow Residual)
Shows the formula: TFP growth = GDP growth - α × Capital growth - (1-α) × Labor growth

---

## Quick Reference: Key Takeaways to Hit With Your Group

1. **Diminishing returns** are visible in the Solow Diagram (Tab 1) — the concave green curve is WHY growth slows down as capital accumulates.

2. **Steady state** is the intersection point — WHERE growth stops depending on capital, and the economy grows only at rate g from technology.

3. **France caught up via TFP** (Tab 2) — PWT 11.0 shows TFP was the main convergence driver (0.61 → 0.99), not capital deepening.

4. **France fell back because of labor** (Tab 4) — N/POP dropped from 1.14 to 0.86. Institutional choices (lower labor force participation, high unemployment) created a LOWER steady state.

5. **China's growth is transitional** (Tab 5) — High savings drive fast capital accumulation, but this is temporary. The question is whether g (TFP growth) can be sustained, or whether China will hit the same plateau France did.

6. **The Philippines paradox** (Tab 4) — Low k means high MPK means high growth potential... but only if structural conditions (savings, TFP, human capital) support it. Having the right initial conditions is necessary but not sufficient.
