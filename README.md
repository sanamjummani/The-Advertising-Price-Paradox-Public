# Why Advertising Changes What You Should Charge

**Pricing strategy analysis using the Tropicana OJ retail scanner dataset — 9,649 weekly store-level observations**

```
Python · OLS Regression · Price Elasticity · Psychological Pricing · Dominick's Finer Foods
```

---

## The Question

Conventional wisdom says advertising drives demand, so you can charge more when you advertise. This project tests that assumption with real retail data — and the answer turns out to be the opposite of what most people expect.

Three questions sit at the center of this analysis. Does advertising actually move sales, and by how much? Does it change how price-sensitive consumers become? And given those answers, what price should a brand actually charge in advertised versus non-advertised weeks?

The findings have direct implications for anyone whose job involves coordinating media and pricing — account teams, brand strategists, media planners. Pricing and advertising decisions are not independent, and this data makes that concrete.

---

## What the Data Showed

<table>
<tr>
<td width="60px" align="center">
<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M4 28 L10 18 L16 22 L22 10 L28 14" stroke="#C9A84C" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
<circle cx="28" cy="14" r="2.5" fill="#C9A84C"/>
</svg>
</td>
<td><strong>555% sales lift from advertising</strong><br><span style="color:#666">Statistically significant at 99.9% confidence. When Tropicana ran a featured ad, weekly sales were on average 6.5× higher than non-advertised weeks.</span></td>
</tr>
<tr><td colspan="2"><br></td></tr>
<tr>
<td align="center">
<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M6 8 Q16 8 16 16 Q16 24 26 24" stroke="#C9A84C" stroke-width="1.6" stroke-linecap="round" fill="none"/>
<line x1="6" y1="24" x2="26" y2="8" stroke="#8A94A6" stroke-width="1" stroke-dasharray="2 2"/>
</svg>
</td>
<td><strong>Elasticity shifts from −2.04 to −3.50 when featured</strong><br><span style="color:#666">Advertising makes buyers more price-sensitive, not less. Consumers who arrive via ads are comparison shoppers — they respond more strongly to price changes.</span></td>
</tr>
<tr><td colspan="2"><br></td></tr>
<tr>
<td align="center">
<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
<rect x="6" y="20" width="4" height="8" rx="0.5" fill="#C9A84C" opacity="0.4"/>
<rect x="12" y="14" width="4" height="14" rx="0.5" fill="#C9A84C" opacity="0.6"/>
<rect x="18" y="8" width="4" height="20" rx="0.5" fill="#C9A84C" opacity="0.8"/>
<rect x="24" y="4" width="4" height="24" rx="0.5" fill="#C9A84C"/>
</svg>
</td>
<td><strong>Optimal price drops from 2× cost to 1.4× cost when advertising</strong><br><span style="color:#666">The profit-maximising formula applied to both elasticity values shows that ad weeks demand a lower markup — sharper prices capture the higher-volume, price-sensitive audience.</span></td>
</tr>
<tr><td colspan="2"><br></td></tr>
<tr>
<td align="center">
<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="16" cy="16" r="11" stroke="#C9A84C" stroke-width="1.4"/>
<line x1="16" y1="5" x2="16" y2="16" stroke="#C9A84C" stroke-width="1.4" stroke-linecap="round"/>
<line x1="16" y1="16" x2="22" y2="20" stroke="#C9A84C" stroke-width="1.4" stroke-linecap="round"/>
<circle cx="16" cy="16" r="1.5" fill="#C9A84C"/>
</svg>
</td>
<td><strong>74% of prices end in .09</strong><br><span style="color:#666">Price digit decomposition reveals systematic charm pricing. The second decimal digit spikes at 9 overwhelmingly — this is not coincidence, it is a structural retail strategy that brands must account for in any pricing recommendation.</span></td>
</tr>
<tr><td colspan="2"><br></td></tr>
<tr>
<td align="center">
<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
<rect x="5" y="5" width="10" height="10" rx="1" stroke="#C9A84C" stroke-width="1.4"/>
<rect x="17" y="5" width="10" height="10" rx="1" stroke="#C9A84C" stroke-width="1.4" stroke-dasharray="2 1.5"/>
<path d="M10 15 L10 22 L22 22" stroke="#C9A84C" stroke-width="1.2" stroke-linecap="round"/>
<circle cx="22" cy="22" r="2" fill="#C9A84C" opacity="0.6"/>
</svg>
</td>
<td><strong>In-sample R² = 0.415 · Out-of-sample R² = 0.438 — model generalises</strong><br><span style="color:#666">The model performs equally well on data it has never seen, which means the pricing strategy derived from it is not just pattern-matching. The findings hold beyond the training sample.</span></td>
</tr>
</table>

---

## What Is in This Repository

**`Project_1_Notebook.ipynb`**
The full analysis in ten steps. Log-log regression, elasticity calculation, optimal pricing derivation, price digit decomposition, and out-of-sample validation. Each section answers a specific business question before it shows any code.

**`Project_1_Presentation.pptx`**
Ten slides translating the statistical findings into strategic recommendations. Built for an account team audience — the emphasis is on what to do with the findings, not how the regression was specified.

**`data/`**
The dataset used is the Tropicana subset of Dominick's Finer Foods retail scanner data — a standard academic marketing dataset covering 9,649 weekly store-level observations. Not included in this repository due to academic data policy.

---

## How the Analysis Was Done

The core model is a log-log OLS regression of sales on price and advertising, with an interaction term between the two. The log-log specification means coefficients read directly as elasticities — a one percent price change causes a fixed percentage change in demand, and that relationship is what the model estimates.

From there, the analysis splits into three parts. The first estimates the advertising effect and how it shifts price sensitivity. The second decomposes prices into integer, first decimal, and second decimal components to surface the charm pricing pattern that shows up in the retail data. The third validates the model out-of-sample to confirm the findings are not overfitted to the training data.

All code is in a single notebook. All findings are explained in plain English before the code that produces them.

---

## Where This Applies

Any brand that runs advertising faces this tradeoff. Campaign weeks are not the right time to hold or raise price — consumers who arrive through ads are comparison shoppers with higher price sensitivity, and the optimal price formula confirms this mathematically. The practical implication is that pricing recommendations and media plans need to be built together, not handed off separately.

This analysis is directly relevant to brand teams, account managers at agencies, and any strategy function that advises clients on how to coordinate advertising and pricing decisions.

---

## Methods and Tools

| | |
|---|---|
| Language | Python 3 |
| Regression | `statsmodels` OLS with log-log specification |
| Data handling | `pandas`, `numpy` |
| Visualisation | `matplotlib`, `seaborn` |
| Validation | `scikit-learn` train-test split |
| Dataset | Dominick's Finer Foods scanner data — Tropicana subset |

---

## About

**Sana Majeed** · MS Business Analytics, Purdue University  
[LinkedIn](https://linkedin.com/in/sanamjumani) · [GitHub](https://github.com/sanamjummani)

> *Part of a portfolio of data-driven marketing strategy projects built during the MS BAIM program at Purdue.*
