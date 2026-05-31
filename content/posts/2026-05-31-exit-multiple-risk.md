---
title: "Growth Is the Pie. The Exit Multiple Is What Someone Pays for It."
description: "Your return decomposes into two factors. One you can analyze. One you're essentially guessing — and at high entry multiples, it's already working against you."
date: 2026-05-31T00:00:00Z
draft: false
tags:
    - investing
    - valuation
    - frameworks
    - mental models
categories: ["Investing"]
---

Most investors who study a business focus almost entirely on growth — TAM, reinvestment runway, ROIC, moat durability. That work is real and valuable. But there's a second factor embedded in every return that rarely gets the same rigour, and over the 3–10 year windows most people actually hold, it moves outcomes at least as much as the growth rate does.

That factor is the exit multiple.

---

## The identity

Ignoring dividends, your annualised price return over N years decomposes cleanly into two multiplicative terms:

```
Price CAGR = (1 + g) × (Exit PE / Entry PE)^(1/N) − 1
```

Where `g` is earnings CAGR. In log form, it's additive:

```
Annual return ≈ ln(1 + g)  +  (1/N) × ln(Exit PE / Entry PE)
       ↑ growth term              ↑ re-rating term
```

Two factors. One you can underwrite. One you are, in large part, guessing.

---

## See the leverage

Entry PE of 100×, 10-year hold. Each cell is your price CAGR:

| Exit PE | 20% growth | 30% growth | 40% growth | 50% growth |
|---|---|---|---|---|
| **100× (no re-rating)** | 20.0% | 30.0% | 40.0% | 50.0% |
| **50×** | 12.0% | 21.3% | 30.6% | 40.0% |
| **25×** | 4.5% | 13.2% | 21.9% | 30.6% |
| **10×** | −4.7% | 3.3% | 11.2% | 19.1% |

Read the table two ways.

**Across a row — fix the multiple, vary growth from 20% to 50%:** roughly a 26-point swing. You get what you paid for in growth.

**Down a column — fix growth at 40%, vary the exit multiple from 100× to 10×:** you go from 40% CAGR to 11%. A 29-point swing. The multiple you exit at moves outcomes at least as much as the growth rate.

That single observation refutes the instinct that *"if I get the growth right, I win."*

---

## Why the multiple is the riskier variable

Magnitude isn't even the main argument. The risk concentrates in the exit multiple for four distinct reasons.

**1. Forecastability**

Growth you can underwrite — unit economics, TAM, reinvestment runway, the moat protecting ROIC. You can build a defensible estimate with error bars you roughly understand.

The terminal multiple a decade out is a function of future interest rates, future market sentiment, and the mood of participants on one specific day. Nobody forecasts that reliably. So even where the magnitudes match, the growth term is *estimable risk* and the exit multiple term is *pure uncertainty*. The unhedgeable part of your return concentrates there.

**2. The base rate is one-directional from high entry**

High multiples mean-revert. A company trading at 100× almost certainly won't be at 100× in ten years — not because the business fails, but because growth decelerates as the business matures, and the market re-rates maturing businesses toward the broader market multiple. From a high entry, the re-rating term isn't symmetric risk; it's a near-certain drag you're fighting.

The top row of the grid (no re-rating from 100×) is a near-fantasy you're implicitly betting on when you buy.

**3. Entry multiple asymmetry — and this is why entry price is the most controllable variable**

The re-rating term `(Exit PE / Entry PE)^(1/N)` is **below 1 whenever you start high** and **above or near 1 when you start low**. Buy at 10× and the multiple is far more likely a tailwind or neutral. Buy at 100× and you've signed up for a structural headwind that only ferocious, sustained growth can overcome.

The entry multiple is the one variable in this equation you fully control and know with certainty at the moment of investment. It determines which side of the asymmetry you're on before a single quarter of results comes in.

**4. At 100× you're barely buying earnings at all**

A 100× PE is a 1% earnings yield. Almost none of your return comes from the earnings stream during your holding window — it comes from the multiple persisting. You're not buying the business's cash generation; you're buying the market's continued willingness to pay up. That is a bet on opinion, not on operations. It is structurally different from the investment analysis that preceded the purchase.

---

## The honest caveat: the horizon effect

This is the flip side worth holding with equal clarity.

The re-rating term is `(1/N) × ln(Exit PE / Entry PE)`. As N grows large — toward 25 or 30 years — this term shrinks toward zero. The multiple you paid and the multiple you exited at wash out almost entirely over very long holds, and your compound return converges to the underlying earnings CAGR of the business.

This is what Munger means when he says *"a stock can't do much better than the business behind it over the long term."*

So there is a real and important qualifier: **the multiple dominates risk precisely over the 3–10 year windows most investors actually hold.** If you genuinely hold for decades and the compounding is real, entry multiple matters far less. The problem is that most portfolios are not held for 30 years, and the investors who say they will hold that long routinely exit within a cycle.

---

## The clean mental image

Growth determines how big the pie gets. The exit multiple determines what someone will pay you for that pie when you sell.

You can be exactly right about the pie — the business compounds exactly as you modelled — and still lose money because the market decided to pay less for pies that year. Getting the growth right protects you from one risk. It does nothing about the other. And the other is the one you can't model and that a high entry price structurally tilts against you.

---

*This post is a quantitative companion to [The Two Engine Framework](/posts/frameworks/two-engine-framework/), which covers the same decomposition from an investment positioning angle.*
