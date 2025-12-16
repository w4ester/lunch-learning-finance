# 🍕 Lunch Picker → Family Food Sovereignty Platform

> **From fighting a 3.5% fee to building a family-first food intelligence system.**

## What This Is Today

A simple, kid-friendly web app that replaces predatory school lunch ordering systems. No fees. No corporate middlemen. Just a calendar, a budget, and a text message to Dad.

### Current Features
- 📅 **Visual Calendar** - See the month's menu at a glance
- 💰 **Budget Tracking** - Kids learn money management in real-time
- 📱 **SMS Checkout** - Orders go to parents, not payment processors
- 🎉 **Kid-Friendly UI** - Confetti, colors, big buttons
- 📴 **Offline-Ready** - Works without internet after first load
- 🔒 **Privacy-First** - All data stays in browser localStorage

### The Problem We're Solving

School lunch apps like Bullfrog/MySchoolBucks charge **3.5% per transaction**.

| Scale | Annual Extraction |
|-------|-------------------|
| 1 family, $50/week | $91/year |
| 500 students | $25,200/year |
| District (10 schools) | $504,000/year |

That's teacher salaries. That's better food. That's families' money—extracted by payment processors for the "convenience" of clicking a button.

---

## What This Will Become

### Phase 1: School Lunch Liberation (Current)
- [x] Static menu calendar
- [x] Budget awareness for kids
- [x] SMS-based ordering
- [ ] Puppeteer scraper for live menu data
- [ ] ACH payments via Stripe (capped fees vs. percentage)
- [ ] Parent dashboard with spending analytics

### Phase 2: Grocery Store Integration 🛒

Connect to grocery store APIs to extend the platform beyond school lunch:

#### Planned Integrations
| Store | API/Method | Data Available |
|-------|------------|----------------|
| **Instacart** | Affiliate API | Prices, availability, delivery |
| **Kroger** | Developer API | Prices, coupons, loyalty points |
| **Walmart** | Affiliate API | Prices, pickup slots |
| **Amazon Fresh** | PA-API | Prices, Subscribe & Save |
| **Local Co-ops** | Custom scraping | Support local food systems |

#### Features
- **Price Comparison Engine** - Same item, best price across stores
- **Sale Alignment** - "Chicken thighs are $2.99/lb at Kroger this week"
- **Coupon Aggregation** - Stack manufacturer + store + app coupons
- **Loyalty Optimization** - "You're 50 points from a free item at Giant"

### Phase 3: Healthy Food Incentives 🥗

Build a family rewards system that incentivizes healthy choices:

#### The "Good Choices" Engine
```
┌─────────────────────────────────────────────────────────┐
│  CHOICE                          │  POINTS  │  WHY     │
├─────────────────────────────────────────────────────────┤
│  Picked salad over pizza         │  +10     │  Veggies │
│  Stayed under budget             │  +5      │  $$      │
│  Chose water over soda           │  +5      │  Health  │
│  Tried new vegetable             │  +15     │  Growth  │
│  Meal had 3+ colors              │  +10     │  Variety │
└─────────────────────────────────────────────────────────┘
```

#### Redemption Ideas
- Extra screen time
- Pick the weekend meal
- Special dessert
- Money toward savings goal
- Charity donation in kid's name

### Phase 4: Financial Literacy Layer 💵

Turn every food decision into a money lesson:

#### Kid-Facing Features
- **Visual Budget** - Watch the progress bar fill up
- **Opportunity Cost** - "If you skip the Gatorade, you could afford..."
- **Savings Goals** - "You saved $4 this week → $208/year"
- **Price Per Serving** - Understand unit economics early

#### Parent Dashboard
- Spending trends over time
- Category breakdown (protein, snacks, drinks)
- Waste tracking (uneaten items)
- Comparison to recommended nutrition spend

### Phase 5: Meal Planning Intelligence 🧠

#### Weekly Meal Planner
- Input: Family preferences, dietary restrictions, budget
- Output: Optimized weekly menu + shopping list
- Constraint: Minimize waste, maximize nutrition per dollar

#### Smart Shopping List
```
┌────────────────────────────────────────────────────────────┐
│  ITEM              │ NEED  │ BEST PRICE      │ SAVINGS    │
├────────────────────────────────────────────────────────────┤
│  Chicken breast    │ 3 lb  │ Costco $2.99/lb │ Save $4.50 │
│  Broccoli          │ 2 hd  │ Aldi $1.29/hd   │ Save $1.40 │
│  Brown rice        │ 2 lb  │ Walmart $1.88   │ Best price │
│  Olive oil         │ 1 bt  │ Costco $12.99   │ Buy next month │
└────────────────────────────────────────────────────────────┘
```

#### Inventory Awareness
- Track pantry staples
- "You have rice at home, skip it"
- Expiration reminders
- Recipe suggestions based on what's about to expire

### Phase 6: Data Sovereignty & Local-First Architecture 🏠

This is where the philosophy matters:

#### Principles
1. **Your data stays yours** - No cloud required, sync optional
2. **Local-first** - Works offline, syncs when connected
3. **Exportable** - JSON/CSV export of all your data
4. **No ads, no selling data** - Ever
5. **Open source** - Fork it, modify it, own it

#### Technical Architecture
```
┌─────────────────────────────────────────────────────────┐
│                    FAMILY DEVICE                        │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │
│  │   SQLite    │  │  IndexedDB  │  │  localStorage│     │
│  │  (Desktop)  │  │   (Web)     │  │   (Lite)    │     │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘     │
│         └────────────────┼────────────────┘            │
│                          ▼                              │
│                  ┌──────────────┐                       │
│                  │  Sync Layer  │ ◄── Optional!        │
│                  │   (CRDT)     │                       │
│                  └──────┬───────┘                       │
└─────────────────────────┼───────────────────────────────┘
                          ▼ (only if family opts in)
                  ┌──────────────┐
                  │ Family Sync  │
                  │   Server     │
                  │ (self-host   │
                  │  or managed) │
                  └──────────────┘
```

---

## The Bigger Picture

### Why This Matters

The food system is optimized against families:
- **School lunch apps** extract fees from captive audiences
- **Grocery stores** use psychology to increase basket size
- **Food companies** engineer products for craveability, not nutrition
- **Meal kit services** charge premium for convenience theater

We can build tools that flip the script:
- **Transparency** - See the real cost of every choice
- **Alignment** - Incentives that reward health, not consumption
- **Education** - Kids learn money + nutrition together
- **Sovereignty** - Families own their data and decisions

### Who This Is For

1. **Families** who want to eat better without spending more
2. **Parents** who want to teach kids about money and health
3. **Schools** that want to stop paying 3.5% to payment processors
4. **Communities** building local food systems

### The Anti-Pattern

This is NOT:
- A VC-backed startup optimizing for growth
- A subscription service extracting monthly fees
- A data harvester selling your eating habits
- A "disruptor" that just moves the margin to a different middleman

This IS:
- A tool families own and control
- Open source and forkable
- Designed to save money, not extract it
- Built for long-term health, not engagement metrics

---

## Technical Roadmap

### Near Term (Q1 2025)
- [ ] Puppeteer scraper for school lunch menus
- [ ] GitHub Actions for daily menu updates
- [ ] Stripe ACH integration for schools that want it
- [ ] Basic parent dashboard

### Medium Term (Q2-Q3 2025)
- [ ] Kroger API integration (price data)
- [ ] Instacart price comparison
- [ ] Healthy choice point system
- [ ] Family sync via CRDTs

### Long Term (2025+)
- [ ] Meal planning AI (local LLM, llama.cpp)
- [ ] Inventory tracking with receipt scanning
- [ ] Community recipe sharing
- [ ] School district white-label version

---

## Get Involved

### For Families
1. Use it: [yourname.github.io/lunch-picker](https://yourname.github.io/lunch-picker)
2. File issues for bugs or ideas
3. Share with other families

### For Developers
1. Fork the repo
2. Check the issues for good first contributions
3. PRs welcome for grocery API integrations

### For Schools
1. Contact us about replacing your current vendor
2. We'll help you save 80%+ on payment processing
3. White-label options available

---

## Philosophy

> "The best interface is one that disappears."

Kids shouldn't need to understand payment processing to eat lunch. Parents shouldn't pay 3.5% for the privilege of feeding their children. Families shouldn't have their food data sold to advertisers.

We build tools that:
- **Get out of the way** - Simple enough for a 7-year-old
- **Teach by doing** - Budget awareness through use, not lectures
- **Respect autonomy** - Your data, your rules
- **Compound value** - Gets more useful over time

---

## License

MIT - Do whatever you want with this. Seriously.

If you build something better, tell us about it.

---

## Credits

Built by families, for families.

Inspired by frustration with predatory EdTech and a belief that we can do better.

---

*"The goal isn't to disrupt the school lunch industry. The goal is to make the school lunch industry irrelevant."*
