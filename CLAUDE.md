# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML presentation for a 60-minute technical talk: **"Carreira em Tecnologia Não É Uma Linha Reta"** by Bruno Pinha Ribeiro at the 8ª Semana de Tecnologia — Senac Maringá, May 21, 2026. Audience: ~200 students in an auditorium, retroprojetor (possibly 1280×720 or 1920×1080).

No build system. Open HTML files directly in a browser.

## Keyboard Shortcuts (Presenter Controls)

| Key | Action |
|-----|--------|
| Arrow keys / Spacebar | Navigate slides |
| N | Toggle presenter notes panel |
| F | Toggle fullscreen |
| Home / End | First / last slide |
| Touch swipe | Mobile navigation |

## File Structure

- `palestra-preview.html` — **ARQUIVO ATIVO** — 4-slide validation prototype with new design system (work in progress)
- `palestra-bruno-pinha.html` — old 24-slide version, **OBSOLETA** — design system replaced
- `roteiro-palestra-bruno-pinha.md` — word-for-word script with minute-by-minute timing (content reference)
- `bio-bruno-pinha.md` — bio variants (30 → 350 words) + oral moderator script
- `fotos/` — image assets (see key photos below)
- `memoria/` — session context files (read these to understand current state)

## Current Status (session 2026-05-26)

**The design is in validation phase.** `palestra-preview.html` has 4 slides built in the new design system. Bruno needs to approve this direction before all 24 slides are built.

**Next step:** Bruno approves (or adjusts) the 4 preview slides → build all 24 slides in the new design system → replace `palestra-bruno-pinha.html`.

Read `memoria/project_palestra.md` and `memoria/feedback_design_autoral.md` for full context.

## Design System — Emerald/Teal/Fuchsia (CURRENT)

All new work must use this system. Do NOT revert to the old amber/Campo+Estrato palette.

```css
:root {
  /* Backgrounds */
  --dark:      #091817;   /* emerald escuro profundo */
  --dark-mid:  #0e2322;
  --dark-hi:   #104544;

  /* Texto */
  --text:      #FFFAF5;   /* Snow */
  --text-mid:  #8db5b3;
  --text-dim:  #3d7876;

  /* Accent principal */
  --teal:      #249F9C;   /* Turquoise — labels, barras, destaques normais */
  --teal-dim:  rgba(36,159,156,.15);
  --teal-glow: rgba(36,159,156,.08);
  --teal-dark: #037A76;

  /* Highlight máximo — usar em NO MÁXIMO 3 momentos por apresentação */
  --fuchsia:      #C11A63;
  --fuchsia-dim:  rgba(193,26,99,.18);
  --fuchsia-glow: rgba(193,26,99,.07);
}
```

**Typography:**
- Display/titles: **Bricolage Grotesque** weight 800 (Google Fonts)
- Body: **Outfit** (Google Fonts)
- Labels/mono: **JetBrains Mono** (Google Fonts)
- Minimum body text: **28px** for projector readability; titles use `clamp(60px, 6.8vw, 90px)`

**Fuchsia rule:** Only at narrative turning points. In the current 4 slides: (1) word "problemas" in the thesis statement, (2) PesoCam row in the stack, (3) "sem contato físico?" in the hypothesis slide.

## Key Photos

- `fotos/intro-bg3.jpg` — B&W editorial portrait, frontal, chin resting on hand, natural black background. **Use on cover (S1)** — face left, text right
- `fotos/intro-bg.jpg` / `intro-bg2.jpg` — side profile B&W and color. For transition/closing slides
- `fotos/pesocam/boi-selecao-visao-computacional.png` — bovine with cyan bounding box, aerial view. **Use on hypothesis slide (S13)**
- `fotos/conmaket_50_lojas.JPG` — Bruno and partner at Conmarket store. **Use on entrepreneurship slide**

## HTML Architecture (palestra-preview.html)

**Single-file design:** All CSS, JS, and slide content in one file. Each slide is a `<div class="slide">` with `data-notes` attribute for presenter notes.

**Critical CSS rule:** `.slide { position: absolute; inset: 0; }` — individual slide IDs must NOT override `position`, or the slide won't fill the viewport (ID selector specificity wins over class).

**Slide navigation:** JS tracks `cur` index; `goTo(n)` adds/removes `.active` class. Progress bar and counter update automatically.

**External CDN:**
- Google Fonts (Bricolage Grotesque, JetBrains Mono, Outfit)

## Presentation Content Structure (24 slides — to be built)

1. Cover (event details + Bruno's photo full-bleed)
2. Central question: "O que conecta tudo isso?"
3. Opening thesis quote (frase-tese)
4–11. Career-as-stack — 7 layers (electronics → programming → architecture → management → entrepreneurship → research → PesoCam)
12–16. PesoCam deep-dive (problem, hypothesis, pipeline, challenges, 9 domains)
17–18. Engineering as connector + external validations (GDIN Korea)
19–20. AI ethics / "vibe coding" warning
21–23. Career advice, networking, teaching
24. Closing + contact + QR code

## Key Narrative & Messaging

**Central thesis:** "Minha carreira não foi definida pelas linguagens que dominei, mas pelos problemas que aprendi a resolver."

**PesoCam:** Contactless bovine weight estimation using OAK-D-Pro-W depth camera + edge AI. Pipeline: bovine → RGB+depth capture → edge processing → AI model → weight estimate. Approved in GDIN 2026 AI & Digital Transformation (South Korea). Incubated at Incubadora Tecnológica de Ivaiporã.

**Tone:** Conversational, story-driven, self-reflective, encouraging. Direct address to students.

## Contact Info (closing slide / QR code)
- Website: brunopinha.com
- LinkedIn: linkedin.com/in/brunopinha7
- WhatsApp: (44) 99185-7884
- Email: brunopinha@msn.com
