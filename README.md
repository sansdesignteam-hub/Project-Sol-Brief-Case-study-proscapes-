
<!-- _paginate: false -->
<!-- _backgroundColor: #1D2E33 -->
<!-- _color: #FFFFFF -->

**SANS DESIGN · DESIGN WORKFLOW**

# Designing with Claude

### Alur kerja desain untuk **Project Sol** — Proscapes.us

`Brief · Notion` → `Moodboard` → `Wireframe` → `Hi-Fi` → `Prototype`

🟫 `#985131` woody  🟩 `#516C65` olive  🟢 `#6B7A55` sage  🟨 `#E8C9A8` peach

---

## Lima tahap, satu alur

Dari brief mentah di Notion sampai prototipe yang bisa diklik. Claude masuk di setiap tahap — sebagai **akselerator, bukan pengganti** keputusan desain.

| # | Tahap | Fokus | Peran Claude |
|---|---|---|---|
| 01 | **Brief · Notion** | Kumpulkan scope & konten jadi satu sumber | Rangkum & tarik requirement |
| 02 | **Moodboarding** | Tentukan arah visual & referensi | Artikulasi art direction |
| 03 | **Wireframing** | Susun struktur & hierarki low-fi | Generate struktur section |
| 04 | **Hi-Fi Design** | Figma: komponen, token, warna final | Binding variable & token |
| 05 | **Prototype** | Interaksi, state & motion | Prototipe motion cepat |

---

## Tahap 01 — Brief dari Notion

> Titik nol: semua konteks proyek jadi satu sumber kebenaran.

- **Yang terjadi** — Scope, tujuan brand, referensi & inventaris konten dirapikan di Notion. Jadi *single source of truth* sebelum satu piksel pun dibuat.
- **Peran Claude** — Merangkum brief jadi poin desain actionable, menarik requirement yang belum terjawab, menyusun content inventory awal.
- **Catatan** — Claude paling kuat di sintesis & eksplorasi, bukan "langsung jadi". Tentukan dulu: full workflow atau sebagian.

`Langkah 1 dari 5`

---

## Tahap 02 — Moodboarding

> Menerjemahkan brief jadi arah rasa: tone, warna, tipografi.

- **Yang terjadi** — Kumpulkan arah visual Sol: nuansa natural/earthy, palet, pairing font, referensi studio sebagai benchmark rasa.
- **Peran Claude** — Mengartikulasikan art direction jadi kata, mengusulkan palet & kombinasi font, bikin gambaran cepat via HTML untuk uji vibe.
- **Catatan** — Untuk arah custom banget, Claude bagus untuk "gambaran" & eksplorasi awal; finishing rasa tetap keputusan desainer.

`Langkah 2 dari 5`

---

## Tahap 03 — Wireframing

> Menetapkan struktur & hierarki sebelum masuk detail visual.

- **Yang terjadi** — Susun kerangka halaman low-fi: urutan section, flow, prioritas konten. Fokus logika layout, bukan estetika.
- **Peran Claude** — Generate struktur section dari brief, mengusulkan urutan & pola layout, mempercepat iterasi beberapa varian.
- **Catatan** — Kerjakan **homepage lebih dulu** sebagai patokan; pola yang matang jadi acuan untuk halaman lain.

`Langkah 3 dari 5`

---

## Tahap 04 — Hi-Fi Design

> Naik ke fidelity penuh di Figma dengan token & komponen final.

- **Yang terjadi** — Bangun tampilan final: komponen, spacing, tipografi & warna dari token semantik Sol (`text-primary`, `woody`, `olive`, `on-teal`, `peach`).
- **Peran Claude** — Binding variable ke properti, generate section, jaga konsistensi token, translate *design → code* saat perlu.
- **Catatan** — Mulai dari satu halaman yang sudah matang (lihat slide berikut).

`Langkah 4 dari 5`

---

<!-- _backgroundColor: #1D2E33 -->
<!-- _color: #FFFFFF -->

## Pelajaran: bikin variable dari homepage dulu

Merapikan token di awal — sebelum ada halaman nyata — justru bikin arsitektur **berantakan**. Yang terbukti jalan: tracking variable dari homepage yang sudah jadi.

`1 · Homepage matang` → `2 · Ekstrak token` → `3 · Generate collection` → `4 · Apply ke page lain`

1. **Homepage matang** — selesaikan satu halaman dulu sebagai fondasi visual.
2. **Ekstrak token** — tarik warna, teks & spacing jadi variable semantik.
3. **Generate collection** — susun Token Color, Typography, Radius, Spacing.
4. **Apply ke page lain** — terapkan & bind ke halaman berikutnya (dibantu Claude).

> **Prinsipnya:** token *mengikuti* halaman nyata, bukan sebaliknya. Homepage jadi patokan, sisanya di-reuse.

---

## Tahap 05 — Prototype

> Menghidupkan desain: interaksi, state & motion untuk divalidasi.

- **Yang terjadi** — Rangkai flow yang bisa diklik: transisi, state, motion (GSAP/Lenis), lalu uji apakah alurnya terasa benar.
- **Peran Claude** — Prototipe motion cepat lewat HTML/GSAP, generate interaksi, bikin showcase interaktif sebagai proof-of-concept.
- **Catatan** — Ideal untuk eksplorasi motion & pembuktian ide sebelum di-porting ke produksi.

`Langkah 5 dari 5`

---

## Full workflow atau sebagian?

Handover alurnya ke tim dulu, lalu sepakati Claude dipakai penuh atau di titik tertentu. Kuncinya tahu di mana ia paling cepat — dan di mana tetap butuh tangan desainer.

| ✅ Cocok diserahkan ke Claude | ⚠️ Tetap pegang manual |
|---|---|
| Sintesis brief jadi poin desain | Hasil super-custom "sekali klik jadi" |
| Eksplorasi arah visual & gambaran cepat | Keputusan rasa & selera akhir |
| Generate struktur wireframe & section | Merapikan token tanpa halaman acuan |
| Binding variable & konsistensi token | Detail finishing produksi |
| Prototipe motion & proof-of-concept | Menggantikan review manusia |

---

## design.md — benang merah

Satu file `design.md` dibuat di tahap awal, lalu **di-upload ulang sebagai konteks di tiap tahap berikutnya**. Itu yang menjaga token konsisten dari homepage sampai halaman terakhir.

**Isinya:** Colors (11 token) · Typography (11 token) · Spacing & Rounded · Components · Do's & Don'ts

```yaml
colors:
  primary:   "#985131"   # woody — CTA, active
  secondary: "#1D2E33"   # ink — headlines, nav
  tertiary:  "#516C65"   # olive-teal — panels
typography:
  headline:  Fraunces
  body:      Inter
```

> Dipakai di: **Moodboard · Wireframe · Hi-Fi · Prototype**

---

## Prompt & skill tiap tahap

| Tahap | Upload | Prompt starter | Skill |
|---|---|---|---|
| **01 Brief** | `brief.md` + referensi | Rangkum brief → requirements & content inventory, generate `design.md` | `prd-to-design-system` |
| **02 Moodboard** | `design.md` + referensi | Usulkan 2–3 arah palet + font pairing, bikin 1 gambaran HTML | `ui-ux-pro-max`, `frontend-design` |
| **03 Wireframe** | `design.md` + sitemap | Susun struktur section homepage low-fi + varian hero | `ui-ux-pro-max` |
| **04 Hi-Fi** | `design.md` final + wireframe | Buat variable dari homepage, bangun hi-fi, bind ke token | `figma-generate-library`, `figma-generate-design` |
| **05 Prototype** | hi-fi HTML / Figma URL | Tambah motion GSAP + ScrollTrigger, hormati reduced-motion | `gsap-scrolltrigger`, `gsap-timeline` |


---

<!-- _paginate: false -->
<!-- _backgroundColor: #16242A -->
<!-- _color: #FFFFFF -->

# Satu alur, dari brief sampai prototipe

### `Brief · Notion` → `Moodboard` → `Wireframe` → `Hi-Fi` → `Prototype`

*Mulai dari homepage, track token dari sana, dan pakai Claude untuk mempercepat — bukan menggantikan keputusan desain.*

<sub>Sans Design · Workflow untuk Project Sol</sub>





# Design.md Project

```yaml
version: alpha
name: Sol Proscapes Earthy Outdoor
description: A grounded, premium outdoor-living system built on woody terracotta, deep olive-teal, and warm sand — calm and natural, with confident warmth at every point of action.
colors:
  primary: "#985131"      # Woody — CTA, active states, key accents
  secondary: "#1D2E33"    # Ink — headlines, nav, strong UI
  tertiary: "#516C65"     # Olive-teal — supporting panels, secondary emphasis
  neutral: "#FFFFFF"      # page base
  surface: "#FBF7F1"      # warm off-white — cards, panels, inputs
  on-surface: "#1D2E33"   # default text on surfaces
  muted: "#737373"        # secondary text, placeholders, inactive
  border: "#E7E1D6"       # warm sand outline / divider
  link: "#516C65"         # link affordance
  error: "#C0492E"        # validation, destructive
  success: "#516C65"      # positive states (re-uses olive-teal)
typography:
  headline-display:
    fontFamily: "Fraunces"
    fontSize: 56px
    fontWeight: 600
    lineHeight: 62px
    letterSpacing: -0.5px
  headline-lg:
    fontFamily: "Fraunces"
    fontSize: 36px
    fontWeight: 600
    lineHeight: 44px
    letterSpacing: -0.3px
  headline-md:
    fontFamily: "Fraunces"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 32px
    letterSpacing: 0px
  headline-sm:
    fontFamily: "Fraunces"
    fontSize: 18px
    fontWeight: 600
    lineHeight: 26px
    letterSpacing: 0px
  body-lg:
    fontFamily: "Inter"
    fontSize: 18px
    fontWeight: 400
    lineHeight: 28px
    letterSpacing: 0px
  body-md:
    fontFamily: "Inter"
    fontSize: 15px
    fontWeight: 400
    lineHeight: 24px
    letterSpacing: 0px
  body-sm:
    fontFamily: "Inter"
    fontSize: 13px
    fontWeight: 400
    lineHeight: 20px
    letterSpacing: 0px
  label-lg:
    fontFamily: "Inter"
    fontSize: 15px
    fontWeight: 600
    lineHeight: 20px
    letterSpacing: 0px
  label-md:
    fontFamily: "Inter"
    fontSize: 13px
    fontWeight: 600
    lineHeight: 16px
    letterSpacing: 0.2px
  label-sm:
    fontFamily: "Inter"
    fontSize: 12px
    fontWeight: 600
    lineHeight: 16px
    letterSpacing: 0.4px
  navigation:
    fontFamily: "Inter"
    fontSize: 14px
    fontWeight: 500
    lineHeight: 20px
    letterSpacing: 0.2px
rounded:
  none: 0px
  sm: 6px
  md: 10px
  lg: 16px
  xl: 24px
  full: 9999px
spacing:
  xs: 8px
  sm: 20px
  md: 40px
  lg: 64px
  xl: 120px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.neutral}"
    typography: "{typography.label-lg}"
    rounded: "{rounded.full}"
    padding: "14px 28px"
    height: "52px"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.secondary}"
    typography: "{typography.label-lg}"
    rounded: "{rounded.full}"
    padding: "13px 27px"
    height: "52px"
    border: "1px solid {colors.tertiary}"
  button-link:
    backgroundColor: "transparent"
    textColor: "{colors.link}"
    typography: "{typography.label-lg}"
    rounded: "{rounded.none}"
    padding: "4px 0px"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.lg}"
    padding: "24px"
    border: "1px solid {colors.border}"
  input:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "12px 16px"
    height: "48px"
    border: "1px solid {colors.border}"
  chip:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.tertiary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: "6px 14px"
    border: "1px solid {colors.border}"
  banner:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.neutral}"
    typography: "{typography.body-md}"
    rounded: "{rounded.lg}"
    padding: "20px 24px"


# Sol — Proscapes Design System

## Overview
Sol is an outdoor-living brand, and the system should feel like being in a well-designed garden at golden hour — warm, calm, and quietly premium. The character is grounded and natural, never sterile: earthy tones do the heavy lifting, generous whitespace lets the content breathe, and warmth arrives at every point of action through the woody terracotta accent. The tone is refined and confident, spacious at the page level while staying tactile up close.

## Colors
Woody (#985131) is the signature action color — used for primary CTAs, active states, and eyebrow accents. It should feel warm and hand-crafted, not corporate. Ink (#1D2E33), a deep teal-charcoal, carries headlines, navigation, and strong UI; it reads nearly black but keeps a natural undertone. Olive-teal (#516C65) is the calm supporting voice for secondary panels, quotes, and "on-teal" sections. Warm off-white surface (#FBF7F1) softens cards and inputs so nothing feels stark, while sand border (#E7E1D6) separates structure gently. Error (#C0492E) sits in the same warm family so validation never clashes; success re-uses olive-teal to keep the palette tight.

## Typography
Fraunces gives headlines an organic, editorial personality — a modern serif with soft, natural curves that suits an outdoor brand better than a geometric sans. Inter handles all body, label, and navigation text for clean, quiet readability. The hierarchy runs from a 56px display down to 12px micro-labels; headlines use tight line-height (~1.1×) for confident stacking, body sits at ~1.55× for comfortable reading. Keep to these two families only.

## Layout & Spacing
Spacing is airy: an 8px micro-grid scales up to 120px hero breaks, giving landing pages room to feel like open outdoor space. Content max-width sits around 1200px. The rhythm is "spacious at page level, comfortable within modules" — sections separate by md–lg (40–64px), while UI padding stays at sm (20px). Resist crowding; the calm comes from the gaps.

## Elevation & Depth
Prefer borders over shadows. Cards define themselves with a 1px sand border on warm off-white rather than a drop shadow, keeping the surface flat and natural. Where elevation is needed (overlays, sticky nav), use a single soft, low-opacity shadow — never stacked or dramatic. Depth comes from tonal shifts between surface and tertiary panels, not from heavy shadows.

## Shapes
Default radius is lg (16px) — soft and organic without being bubbly, echoing rounded stone and planter forms. Buttons and chips go full (pill) for a friendly, tactile feel; inputs use md (10px) for a slightly more structured edge. Avoid sharp 0px corners except for full-bleed imagery.

## Components
Primary buttons are pill-shaped woody CTAs with generous 14×28 padding and a 52px touch target. Secondary buttons invert to an olive-teal outline on transparent for lower-emphasis actions. Cards are warm off-white with a sand border and 16px radius, holding body content at 24px padding. Inputs stay white with a 10px radius so form fields feel a touch crisper than surrounding cards. Chips are pill outlines in olive-teal for filters and tags. Banners fill with olive-teal and inverse text for calm, non-alarming announcements.

## Do's and Don'ts
**Do**
- Lead with warm off-white and let woody appear only at points of action.
- Use Fraunces for headlines and Inter for everything else — no third font.
- Keep generous vertical rhythm; give hero and section breaks real breathing room.
- Define containers with sand borders on flat surfaces before reaching for shadow.
- Reserve pill shapes for interactive elements (buttons, chips).

**Don't**
- Don't spread woody across large fills — it's an accent, not a background.
- Don't drop to pure black (#000) or pure white cards; stay in the warm-neutral family.
- Don't add accent stripes or hard dividers where whitespace would do.
- Don't mix radius scales randomly on the same surface.
- Don't stack heavy shadows — keep depth tonal and subtle.
```
