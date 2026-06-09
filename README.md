/* ============================================================
   TEM — TheoEd Mission (테오에드선교회)
   Design tokens: color + typography + spacing + elevation
   Source: TEM_BI_Design_Guidelines.pdf (converted from .ai)
   ------------------------------------------------------------
   FONT NOTE: the printed wordmark uses a rounded geometric sans
   whose exact name is not given in the guideline. We substitute
   **Nunito** (+ Noto Sans KR for Hangul) as the closest free
   match. Replace with the licensed brand face when available.
   ============================================================ */

@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,400;0,500;0,600;0,700;0,800;0,900&family=Noto+Sans+KR:wght@400;500;700;900&display=swap');

:root {
  /* ---- BRAND CORE (authoritative hex from the guideline) ---- */
  --tem-blue:   #1A365D;  /* PANTONE 534C  — 신뢰와 좋은 신학적 전통 / trust, sound tradition */
  --tem-gold:   #D6AF21;  /* PANTONE 4018C — 하나님의 영광과 빛 / glory & light */
  --tem-black:  #121212;  /* PANTONE Black 6C — 거룩성과 권위 / holiness & authority */
  --tem-green:  #2D5A27;  /* PANTONE 2266C — 생명력과 뻗어나가는 선교 / vitality & outreach */
  --tem-white:  #F8F9FA;  /* Pure White */

  /* ---- BLUE scale (primary) ---- */
  --blue-900: #0E1E36;
  --blue-800: #142A4A;
  --blue-700: #1A365D;   /* = brand blue */
  --blue-600: #25497A;
  --blue-500: #356099;
  --blue-200: #AEC0D8;
  --blue-100: #DCE5F0;
  --blue-050: #EEF3F9;

  /* ---- GOLD scale (accent) ---- */
  --gold-700: #A8861A;
  --gold-600: #C29C1E;
  --gold-500: #D6AF21;   /* = brand gold */
  --gold-400: #E1C04B;
  --gold-200: #F0DD9C;
  --gold-100: #F8EEC9;

  /* ---- GREEN scale (secondary / life) ---- */
  --green-800: #1E3D1A;
  --green-700: #2D5A27;  /* = brand green */
  --green-500: #3E7836;
  --green-200: #BBD0B6;
  --green-100: #E0EADD;

  /* ---- INK / NEUTRALS ---- */
  --ink-900:  #121212;   /* = brand black */
  --ink-700:  #2A2E33;
  --ink-500:  #565C63;
  --ink-400:  #7A8189;
  --ink-300:  #A7ADB4;
  --ink-200:  #D4D8DD;
  --ink-100:  #E7EAEE;
  --paper:    #F8F9FA;   /* = pure white */
  --paper-2:  #FFFFFF;

  /* ---- SEMANTIC ---- */
  --bg:            var(--paper);
  --bg-inverse:    var(--tem-blue);
  --bg-inverse-2:  var(--tem-green);
  --surface:       #FFFFFF;
  --surface-sunken: #F1F3F6;
  --fg:            var(--tem-blue);
  --fg-strong:     var(--ink-900);
  --fg-muted:      var(--ink-500);
  --fg-ondark:     #F2F5FA;
  --fg-ondark-mut: #A9B6CB;
  --accent:        var(--tem-gold);
  --accent-ink:    #5A4A0E;     /* readable text on gold */
  --border:        var(--ink-100);
  --border-strong: var(--ink-200);
  --focus-ring:    color-mix(in srgb, var(--tem-gold) 55%, white);

  /* ---- TYPE FAMILIES ---- */
  --font-sans:    'Nunito', system-ui, -apple-system, 'Segoe UI', sans-serif;
  --font-display: 'Nunito', system-ui, sans-serif;          /* brand / wordmark face (substitute) */
  --font-kr:      'Noto Sans KR', 'Nunito', sans-serif;     /* Hangul */
  --font-mono:    'IBM Plex Mono', ui-monospace, 'SF Mono', monospace;

  /* ---- TYPE SCALE ---- */
  --fs-display: clamp(2.6rem, 6vw, 4.25rem);
  --fs-h1:      clamp(2rem, 4vw, 3rem);
  --fs-h2:      clamp(1.5rem, 2.6vw, 2.1rem);
  --fs-h3:      1.375rem;
  --fs-lead:    1.1875rem;
  --fs-body:    1rem;
  --fs-small:   0.875rem;
  --fs-micro:   0.75rem;

  /* ---- WEIGHTS ---- */
  --w-regular: 400;
  --w-medium:  500;
  --w-semi:    600;
  --w-bold:    700;
  --w-x:       800;   /* the TEM-emphasis weight used in the wordmark */
  --w-black:   900;

  /* ---- LINE HEIGHTS ---- */
  --lh-tight: 1.08;
  --lh-snug:  1.25;
  --lh-body:  1.6;

  /* ---- TRACKING ---- */
  --ls-tight: -0.02em;
  --ls-normal: 0;
  --ls-label: 0.12em;   /* all-caps labels */
  --ls-wide:  0.2em;

  /* ---- SPACING (4pt base) ---- */
  --sp-1: 4px;  --sp-2: 8px;  --sp-3: 12px; --sp-4: 16px;
  --sp-5: 24px; --sp-6: 32px; --sp-7: 48px; --sp-8: 64px; --sp-9: 96px;

  /* ---- RADII (brand mark is a generous squircle) ---- */
  --r-sm: 6px;
  --r-md: 12px;
  --r-lg: 20px;
  --r-xl: 28px;
  --r-squircle: 30%;   /* emblem-style rounded square */
  --r-pill: 999px;

  /* ---- ELEVATION (soft, cool-tinted) ---- */
  --shadow-sm:  0 1px 2px rgba(18,30,54,0.06), 0 1px 3px rgba(18,30,54,0.08);
  --shadow-md:  0 4px 12px rgba(18,30,54,0.10), 0 2px 4px rgba(18,30,54,0.06);
  --shadow-lg:  0 18px 40px rgba(18,30,54,0.16), 0 6px 14px rgba(18,30,54,0.10);
  --shadow-emblem: 0 10px 28px rgba(18,30,54,0.22);

  /* ---- MOTION ---- */
  --tr-fast: 130ms ease-out;
  --tr-base: 200ms ease-out;
}

/* clean up the stray placeholder line above */

/* ============================================================
   SEMANTIC ELEMENT STYLES (opt-in helper classes)
   ============================================================ */

.tem-display {
  font-family: var(--font-display);
  font-weight: var(--w-x);
  font-size: var(--fs-display);
  line-height: var(--lh-tight);
  letter-spacing: var(--ls-tight);
  color: var(--fg);
}
.tem-h1 { font-family: var(--font-display); font-weight: var(--w-x); font-size: var(--fs-h1); line-height: var(--lh-tight); letter-spacing: var(--ls-tight); color: var(--fg); }
.tem-h2 { font-family: var(--font-display); font-weight: var(--w-bold); font-size: var(--fs-h2); line-height: var(--lh-snug); color: var(--fg); }
.tem-h3 { font-family: var(--font-sans); font-weight: var(--w-bold); font-size: var(--fs-h3); line-height: var(--lh-snug); color: var(--fg); }
.tem-lead { font-family: var(--font-sans); font-weight: var(--w-medium); font-size: var(--fs-lead); line-height: var(--lh-body); color: var(--fg-muted); }
.tem-body { font-family: var(--font-sans); font-weight: var(--w-regular); font-size: var(--fs-body); line-height: var(--lh-body); color: var(--fg-strong); }
.tem-small { font-size: var(--fs-small); line-height: 1.5; color: var(--fg-muted); }

/* All-caps tracked label — the one persistent type detail */
.tem-label {
  font-family: var(--font-sans);
  font-weight: var(--w-bold);
  font-size: var(--fs-micro);
  letter-spacing: var(--ls-label);
  text-transform: uppercase;
  color: var(--accent);
}

/* Korean copy */
.tem-kr { font-family: var(--font-kr); line-height: 1.7; }

/* Wordmark recreation: TEM letters carry the emphasis weight.
   Usage: <span class="tem-wordmark"><b>T</b>heo<b>E</b>d <b>M</b>ission</span> */
.tem-wordmark {
  font-family: var(--font-display);
  font-weight: var(--w-medium);
  letter-spacing: 0.01em;
  color: var(--tem-blue);
}
.tem-wordmark b { font-weight: var(--w-x); }
