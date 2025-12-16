# 🗺️ Lunch Picker Roadmap

> Clear separation of what's done, what's next, and what's possible.

---

## ✅ Phase 0: MVP (COMPLETE)

**Status:** Done — Deployed & Usable Tonight

| Feature | Status | Notes |
|---------|--------|-------|
| Static calendar UI | ✅ Done | December 2025 with real menu data |
| Budget tracker | ✅ Done | Visual progress bar, over-budget warnings |
| Meal selection modal | ✅ Done | Main courses, sides, drinks |
| Price calculations | ✅ Done | Using actual school price list |
| LocalStorage persistence | ✅ Done | Survives page refresh |
| SMS checkout | ✅ Done | "Send to Dad" opens text app |
| Mobile responsive | ✅ Done | Works on phones |
| Winter break dates | ✅ Done | Dec 22-31 blocked out |
| No CDN dependencies | ✅ Done | Production-ready, no warnings |

**Files:**
- `lunch-picker.html` — Single file, ready to deploy to GitHub Pages

---

## 🔨 Phase 1: Live Menu Data (IN PROGRESS)

**Status:** Next Up — Eliminates manual menu updates

| Feature | Status | Effort | Description |
|---------|--------|--------|-------------|
| Puppeteer scraper | 🔲 Todo | 2-3 hrs | Pull menu from Bullfrog/school site |
| JSON menu format | 🔲 Todo | 1 hr | Standardized data structure |
| GitHub Actions cron | 🔲 Todo | 1 hr | Auto-update menu nightly |
| Menu diff alerts | 🔲 Todo | 1 hr | Notify when menu changes |

**Deliverables:**
- `scraper/scrape_menu.js` — Puppeteer script
- `data/menu_december_2025.json` — Scraped menu data
- `.github/workflows/update-menu.yml` — Nightly cron job

**Dependencies:**
- Node.js
- puppeteer-extra + stealth plugin
- GitHub repo with Actions enabled

---

## 📱 Phase 2: Parent Dashboard

**Status:** Planned — Q1 2026

| Feature | Status | Effort | Description |
|---------|--------|--------|-------------|
| Order history view | 🔲 Todo | 2 hrs | See all past orders |
| Spending analytics | 🔲 Todo | 3 hrs | Charts, trends, category breakdown |
| Multi-child support | 🔲 Todo | 2 hrs | Separate budgets per kid |
| Weekly summary email | 🔲 Todo | 2 hrs | Optional digest |
| Export to CSV | 🔲 Todo | 1 hr | Download your data |

**Deliverables:**
- `parent-dashboard.html` — Separate parent view
- LocalStorage schema upgrade for multi-child

---

## 💳 Phase 3: ACH Payments (School-Ready)

**Status:** Planned — Q1 2026

| Feature | Status | Effort | Description |
|---------|--------|--------|-------------|
| Stripe ACH setup | 🔲 Todo | 4 hrs | Bank account linking |
| Plaid instant verify | 🔲 Todo | 3 hrs | Skip micro-deposits |
| Pre-funded wallets | 🔲 Todo | 4 hrs | Parents load balance, kids spend down |
| Level 3 data | 🔲 Todo | 2 hrs | Line-item details for lower fees |
| School admin portal | 🔲 Todo | 8 hrs | Manage students, view orders |

**Why This Matters:**
| Payment Method | Fee on $100 | Annual on $720K program |
|----------------|-------------|-------------------------|
| Credit Card 3.5% | $3.50 | $25,200 |
| ACH (capped) | ~$0.80 | ~$5,760 |
| **Savings** | **$2.70** | **$19,440** |

**Deliverables:**
- `server/payment.js` — Stripe integration
- `server/plaid.js` — Bank verification
- Admin dashboard for schools

**Dependencies:**
- Stripe account
- Plaid account (or Stripe Financial Connections)
- Simple backend (Node.js/Express or serverless)

---

## 🛒 Phase 4: Grocery Store Integration

**Status:** Planned — Q2 2026

| Feature | Status | Effort | Description |
|---------|--------|--------|-------------|
| Kroger API | 🔲 Todo | 4 hrs | Prices, coupons, loyalty |
| Instacart API | 🔲 Todo | 4 hrs | Multi-store comparison |
| Walmart API | 🔲 Todo | 3 hrs | Pickup/delivery prices |
| Price comparison engine | 🔲 Todo | 6 hrs | Best price routing |
| Coupon aggregator | 🔲 Todo | 4 hrs | Stack all available discounts |
| Shopping list generator | 🔲 Todo | 3 hrs | From meal plan to cart |

**API Access:**
| Store | API Type | Access |
|-------|----------|--------|
| Kroger | Developer API | Free signup |
| Instacart | Partner API | Apply for access |
| Walmart | Affiliate API | Affiliate signup |
| Amazon Fresh | PA-API | Associates account |

**Deliverables:**
- `integrations/kroger.js`
- `integrations/instacart.js`
- `integrations/walmart.js`
- `shopping-list.html` — Unified shopping view

---

## 🥗 Phase 5: Healthy Choice Incentives

**Status:** Planned — Q2 2026

| Feature | Status | Effort | Description |
|---------|--------|--------|-------------|
| Point system design | 🔲 Todo | 2 hrs | Define earning rules |
| Choice tracking | 🔲 Todo | 2 hrs | Log healthy vs. less healthy |
| Reward redemption | 🔲 Todo | 3 hrs | Family-defined rewards |
| Streak tracking | 🔲 Todo | 2 hrs | "5 days of veggies!" |
| Nutrition labels | 🔲 Todo | 4 hrs | Show protein, fiber, sugar |

**Point System Draft:**
```
+10 pts  Chose salad/veggies as main
+5 pts   Stayed under daily budget
+5 pts   Water instead of soda
+15 pts  Tried something new
+10 pts  Meal had 3+ colors
-5 pts   Added extra dessert (optional guilt mode)
```

**Deliverables:**
- Points engine in JS
- Kid-facing points display
- Parent reward configuration

---

## 🧠 Phase 6: Meal Planning Intelligence

**Status:** Planned — Q3 2026

| Feature | Status | Effort | Description |
|---------|--------|--------|-------------|
| Weekly meal planner | 🔲 Todo | 8 hrs | Input prefs → output menu |
| Recipe database | 🔲 Todo | 4 hrs | Family favorites + suggestions |
| Nutrition optimizer | 🔲 Todo | 6 hrs | Balance macros across week |
| Waste reducer | 🔲 Todo | 4 hrs | Use what's expiring first |
| Local LLM integration | 🔲 Todo | 8 hrs | llama.cpp for suggestions |

**Deliverables:**
- `planner/meal-planner.html`
- `planner/optimizer.js`
- Recipe JSON schema
- Optional: llama.cpp integration for natural language

---

## 🏠 Phase 7: Data Sovereignty

**Status:** Planned — Q3-Q4 2026

| Feature | Status | Effort | Description |
|---------|--------|--------|-------------|
| IndexedDB migration | 🔲 Todo | 4 hrs | Larger local storage |
| SQLite option | 🔲 Todo | 4 hrs | Desktop app version |
| CRDT sync layer | 🔲 Todo | 8 hrs | Multi-device without cloud |
| Self-host option | 🔲 Todo | 4 hrs | Docker container |
| Full data export | 🔲 Todo | 2 hrs | JSON + CSV everything |
| Data deletion | 🔲 Todo | 1 hr | True delete, not archive |

**Architecture:**
```
Family Device (Phone/Laptop)
    └── Local DB (IndexedDB/SQLite)
            └── [Optional] CRDT Sync
                    └── [Optional] Self-hosted server
                            OR managed sync service
```

**Deliverables:**
- Upgraded storage layer
- Sync protocol (Yjs or Automerge)
- Docker compose for self-hosting

---

## 🎯 Quick Wins (Anytime)

Low-effort improvements that can happen anytime:

| Feature | Effort | Impact |
|---------|--------|--------|
| Add more months | 30 min | January, February menus |
| Allergen filters | 1 hr | Hide items with nuts/dairy/etc |
| Favorite meals | 1 hr | Quick re-order |
| Dark mode | 1 hr | Night-friendly |
| PWA manifest | 30 min | "Add to Home Screen" |
| Print view | 30 min | Paper backup for school |

---

## 📊 Success Metrics

How we know this is working:

| Metric | Phase 0 | Phase 3 | Phase 6 |
|--------|---------|---------|---------|
| Families using | 1 (yours) | 50 | 500+ |
| Payment fees saved | $0 | $1,000/yr | $20,000/yr |
| Grocery savings/family | $0 | $20/mo | $50/mo |
| Kids making healthy choices | Baseline | +20% | +40% |
| Data owned by families | 100% | 100% | 100% |

---

## 🚀 Getting Started

**Tonight:**
1. Download `lunch-picker.html`
2. Upload to GitHub repo
3. Enable GitHub Pages
4. Send link to kids

**This Week:**
1. Test with real orders
2. Gather feedback from kids
3. File issues for bugs/ideas

**Next Sprint:**
1. Build Puppeteer scraper
2. Automate menu updates
3. Add January 2026 menu

---

## 🤝 Contributing

### Priority Order
1. **Bug fixes** in current lunch-picker
2. **Scraper** for live menu data
3. **Grocery API** integrations
4. **Everything else**

### Not Accepting (Yet)
- Backend/database PRs (staying static for now)
- Payment integration (needs careful security review)
- Features that require accounts/login

---

## 📅 Timeline

```
Dec 2025  ████████████████████ Phase 0 ✅
Jan 2026  ████████░░░░░░░░░░░░ Phase 1 (Scraper)
Feb 2026  ░░░░████████░░░░░░░░ Phase 2 (Dashboard)
Mar 2026  ░░░░░░░░████████░░░░ Phase 3 (Payments)
Apr 2026  ░░░░░░░░░░░░████████ Phase 4 (Grocery)
May 2026  ░░░░░░░░░░░░░░░░████ Phase 5 (Incentives)
Q3 2026   ░░░░░░░░░░░░░░░░░░░░ Phase 6-7 (AI + Sovereignty)
```

---

*Last updated: December 15, 2025*
