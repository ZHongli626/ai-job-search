## One sentence about my chapters

**Chapter 1 (Data Restrictions & Software Competition):** Data privacy regulations act as both compliance costs and product attributes: firms in low-restriction regions gain cost advantages, but can lose market share when consumers value privacy, creating asymmetric equilibria where regulatory environment determines competitive outcomes.

**Chapter 2 (Service Capacity, Network Effects & Congestion):** Technologically superior ICT firms face a strategic trade-off: network effects amplify their user-base advantage, but congestion degrades service quality unless they invest sufficiently in capacity, making capacity investment essential to sustain high-price, high-profit strategies.

**Chapter 3 (Empirical Calibration of ABM):** Real telecom data (AT&T vs. T-Mobile) can partially discipline agent-based models through simulation-based moment matching, but non-stationarity, path dependence, and computational constraints limit full empirical validation: calibrated parameters reveal that firm-specific pricing and investment adjustment rules matter more than static technology gaps.

**Big Story:** Competitive advantage in ICT markets is not static. It emerges from dynamic interactions between regulation, technology, consumer networks, service quality, and adaptive firm strategies. Winning requires aligning investment, pricing, and capacity decisions with these feedback mechanisms.

## Patterns for extensions

What can we learn from my thesis? Which are solvable and which are not?

### Example 1: Kebab shops on the same street

**What transfers:**
- Spatial differentiation (location as product attribute, similar to Hotelling framework in Chapter 1)
- Heterogeneous consumer preferences (taste, price sensitivity, distance costs)
- Adaptive pricing strategies (myopic firm learning)

**What doesn't transfer:**
- No network effects (your neighbor's kebab choice doesn't affect your utility)
- No congestion in the ICT sense (waiting time is different from service quality degradation)
- No capacity-quality feedback (kitchen capacity is a production constraint, not a quality determinant)
- No regulatory asymmetry as product attribute

**Verdict:** Partially applicable—the ABM framework and adaptive competition work, but the ICT-specific mechanisms (Chapters 2-3) don't apply. This becomes a standard spatial competition model.

---

### Example 2: German car companies competing across countries

**What transfers:**
- Regulatory differences across regions (emission standards, safety regulations as both costs and product attributes)
- Technology/quality differentiation (engineering capability as vertical differentiation)
- Consumer heterogeneity in preferences (environmental concerns, brand loyalty)
- Investment in R&D affecting product quality

**What partially transfers:**
- Network effects exist but are weaker (brand reputation, service network availability)
- Capacity constraints affect delivery times but not product quality directly

**What doesn't transfer:**
- No real-time congestion degrading service quality
- Much longer decision cycles (years, not months)
- Supply chain and production complexity not captured in your model

**Verdict:** Moderately applicable—Chapter 1's regulatory mechanism transfers well, but Chapter 2's capacity-congestion-network dynamics are weaker. Would need adaptation for durable goods, longer time scales, and supply chain considerations.

---

### Example 3: OpenAI vs. Anthropic

**What transfers extremely well:**
- **Technology/capacity as quality determinant:** Model capability (parameters, training compute) directly affects service quality—this is Chapter 2's core mechanism
- **Network effects:** Developer ecosystems, API integrations, user communities create lock-in
- **Congestion:** API rate limits, response latency under load, service degradation with demand spikes
- **Regulatory environment:** AI safety regulations, data privacy laws as both compliance costs and trust signals
- **Adaptive strategies:** Pricing experiments (ChatGPT Plus, Claude Pro), rapid capability updates
- **Consumer heterogeneity:** Developers, enterprises, consumers with different use cases and price sensitivities

**What needs extension:**
- Multi-sided platform dynamics (developers + end users)
- Rapid technological change (model generations every 6-12 months)
- Open-source competition (Llama, Mistral) as outside option
- Complementary products (plugins, integrations, enterprise features)

**Verdict:** Highly applicable—this is arguably the *best* modern example of your thesis mechanisms. All three chapters' insights transfer: regulatory positioning (safety vs. capability trade-offs), capacity-network-congestion dynamics, and the calibration challenge of matching real market evolution. Your ABM framework could model this with minimal adaptation.

---

### Summary: Applicability Hierarchy

1. **ICT platforms/services** (AI, telecom, cloud, social media): 90%+ applicable—all core mechanisms present
2. **Technology products with network effects** (software, hardware ecosystems): 70% applicable—regulatory and network mechanisms transfer, congestion less relevant
3. **Differentiated products with regulatory variation** (automotive, pharma): 50% applicable—Chapter 1 mechanisms work, Chapter 2 mechanisms weak
4. **Standard spatial competition** (retail, restaurants): 30% applicable—only basic competition framework, no ICT-specific dynamics

