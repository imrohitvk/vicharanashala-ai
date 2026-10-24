# Changelog

All notable content and structural changes to this site are documented here.  
Changes are tracked before being committed or raised as a PR.

---

## [Unreleased] — BOG Deck Sync (June 2026)

Source of truth: Vicharanashala Lab BOG Deck, June 2026 (VLED Lab | IIT Ropar)  
Branch: `content/bog-updates-june-2026`  
Contributor: Pavani Ayinampudi

### Status Key
- [ ] Pending
- [x] Done

---

### Homepage — Problem-First Vision Rewrite
- [ ] Rewrite `index.md` to lead with WHY WE EXIST before stating what we believe
- **Old tone:** Generic EdTech aspiration with no grounding in specific problems
- **New structure:**
  1. WHY WE EXIST — the three unsolved problems in Indian HE:
     - Faculty development at scale: fragmented, low-quality, no personalisation (ARPIT reached millions, didn't move the needle)
     - Online learning's 10% completion wall: passive video delivery produces dashboards, not learning
     - Student internships are exclusionary & manual: coordination-heavy, gate-kept by networks, Tier 2/3 students locked out
  2. WHAT WE BUILT — two tracks, one mandate: National Programs + EdTech Products
  3. Retain "How We Work" philosophy section with minor edits

---

### Products / Nav

#### HP Dashboard → Spurti (rename)
- [ ] Rename `_projects/hp-dashboard-lti.md` to `_projects/spurti.md`
- [ ] Update title, page_title, permalink in frontmatter
- [ ] Update product description to match deck: "Gamified progress tracking for self-regulated learning. Deployed in live classroom settings."
- [ ] Update nav in `products.md`
- **Confirmed from deck:** Listed as PILOT status

#### Samagama + Yaksha (new product page)
- [ ] Create `_projects/samagama.md`
- [ ] Add to `products.md` nav (position 2, after ViBe)
- **Confirmed numbers from deck:**
  - 8,428 Students Registered
  - 5,032 AI-Conducted Interviews (zero human screeners)
  - 2,943 Offer Letters Issued
  - 4,57,728 Messages handled autonomously by Yaksha
  - 18,268 Student sessions (6,142 unique users)
  - 47,500+ Engagement point transactions
  - Run by a 4-person core team (equivalent of 20–30 coordinators)
- **Description from deck:** "Internship management at national scale — fully automated. Can every student get a high quality internship experience at IITs without overburdening the human resources."

#### Note: Tenali
- Jinal Gupta is listed in the team section as working on "Tenali" — a product name not documented elsewhere on the site. No page added in this PR; flagged for future addition once content is available.

---

### ViBe — Impact Numbers Update
- [ ] Update impact section in `_projects/vibe.md`
- **Old:** "over 3,500 learners for more than 23,000 verified watch hours... 50 percent increase in course completion rates"
- **New (confirmed from deck):**
  - 9,984 Unique Learners
  - 10,959 Active Enrollments
  - 39 Courses / Cohorts Live
  - ~35% Completion Rate (3.5× the industry norm of <10%)
  - Verified, proctored, at marginal cost

---

### National Initiatives — Updates

#### Reach Numbers
- [ ] Update `national_initiatives.md` CBPAI participant count
- **Old:** "we reached more than 2400 participants"
- **New:** 3,500+ faculty reached across both programs, 600+ certified

#### GuruSetu — Add Verified Details
- [ ] Add/update: 3-IIT partnership (IIT Ropar · IIT Madras · IIT Gandhinagar), 9 thematic pillars, active since December 2024
- [ ] Add funding: ₹1,45,00,000 sanctioned (FY 2024–25 to 2026–27)

#### CBPAI — Add 26-item Instrument + Funding
- [ ] Add: 26-item AI literacy benchmarking instrument (currently in expert validation & pilot testing) — original IP with no comparable instrument in Indian HE context
- [ ] Add: active since February 2025
- [ ] Add funding: ₹70,00,000 sanctioned (FY 2024–25 to 2026–27)
- [ ] Add combined line: ₹2,15,00,000 total funding secured across both programs

---

### Lab Initiatives — Summership 2026 (new section)
- [ ] Add Summership as a new section in `lab_initiatives.md`
- **Confirmed from deck:** 8,428 students in structured internships, run by 4-person core team via Samagama + Yaksha automation
- **Framing from deck:** "Can every student get a high quality internship experience at IITs without overburdening the human resources."
- Institutional alignment: addresses the problem of exclusionary, coordination-heavy internships for Tier 2/3 students

---

### Team Page — Roles and Designations
- [ ] Update `team-members.md` with confirmed roles from deck
- **Confirmed roles:**
  - Prof. Sudarshan Iyengar — Principal Investigator & Group Lead
  - Dr. Pavani Ayinampudi — Learning Innovation & Process Architect (GuruSetu · CBPAI · Summership)
  - Prakash Hegade — Instruction Systems Scientist (Course design · FDP delivery · Research)
  - Meenakshi V — AI Skill Development Head & Research Scholar (ViBe platform research & ops)
  - Sakshi Sharma — Research Scholar (Spurti)
  - Rohit Sharma — Research Scholar (Spandan & Vi-Slides)
  - Jinal Gupta — Research Scholar (Tenali)
- **Add:** note on broader team (admin & operations staff, NPTEL pre-doc fellows, offline interns, positions actively hiring under UGC-MMTTP)

---

### Notes
- All changes sourced from BOG Deck, June 2026 (VLED Lab | IIT Ropar, PI: Prof. Sudarshan Iyengar)
- No changes will be committed until this changelog is reviewed
- PR will be raised to `vicharanashala/vicharanashala-ai` from `pavaniasn/vicharanashala-ai`, branch `content/bog-updates-june-2026`
