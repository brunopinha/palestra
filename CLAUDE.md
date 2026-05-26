# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML presentation for a 60-minute technical talk: **"Carreira em Tecnologia Não É Uma Linha Reta"** by Bruno Pinha Ribeiro at the 8ª Semana de Tecnologia — Senac Maringá, May 21, 2026. Audience: ~200 students in an auditorium.

No build system. Open `palestra-bruno-pinha.html` directly in a browser.

## Keyboard Shortcuts (Presenter Controls)

| Key | Action |
|-----|--------|
| Arrow keys / Spacebar | Navigate slides |
| N | Toggle presenter notes panel |
| F | Toggle fullscreen |
| Home / End | First / last slide |
| Touch swipe | Mobile navigation |

## File Structure

- `palestra-bruno-pinha.html` — 24-slide interactive presentation deck (self-contained)
- `roteiro-palestra-bruno-pinha.md` — Word-for-word script with minute-by-minute timing
- `bio-bruno-pinha.md` — Bio variants (30 words → 350 words) + oral moderator script
- `fotos/` — Image assets (profile photo, PesoCam images, logos, backgrounds)

## HTML Presentation Architecture

**Single-file design:** All CSS, JS, and slide content lives in `palestra-bruno-pinha.html`. Each slide is a `<section class="slide">` with a `data-notes` attribute containing presenter notes.

**Slide navigation model:** JS tracks `currentSlide` index; `showSlide(n)` adds/removes the `.active` class. Progress bar and counter update automatically.

**Design system — CSS custom properties:**
```css
--accent: #00e5a0   /* green — primary CTA/highlight */
--blue:   #4b8eff
--orange: #ff7b35
--purple: #a46fff
--pink:   #ff4d7e
--yellow: #ffc740
```
Font stack: Syne (display/headings), Outfit (body), JetBrains Mono (code/labels). Minimum body text 26px — sized for auditorium projection.

**Reusable CSS component classes:**
- `.stack` — vertical layer visualization (career stack metaphor)
- `.flow` — horizontal pipeline diagram (PesoCam data flow)
- `.card` / `.hbox` — highlighted content boxes
- `.pgrid` — 2-column principles grid
- `.dgrid` — 3-column domain grid
- `.pills` — tag labels
- `.timeline` — chronological event list

**External CDN dependencies:**
- Google Fonts (Syne, JetBrains Mono, Outfit)
- `qrcodejs` — generates the WhatsApp QR code on the closing slide

## Presentation Content Structure (24 slides)

1. Cover (event details)
2. Central question: "O que conecta tudo isso?"
3. Opening thesis quote
4–11. Career-as-stack metaphor — 7 layers (electronics → programming → architecture → management → entrepreneurship → research → PesoCam convergence)
12–16. PesoCam deep-dive (problem, hypothesis, pipeline, challenges, 9 domains)
17–18. Engineering as connector + external validations
19–20. AI ethics / "vibe coding" warning
21–23. Career advice, networking, teaching
24. Closing + contact + QR code

## Key Narrative & Messaging

**Central thesis:** "Minha carreira não foi definida pelas linguagens que dominei, mas pelos problemas que aprendi a resolver."

**PesoCam** (the convergence project): Contactless bovine weight estimation using OAK-D-Pro-W depth camera + edge AI. Avoids stress and cost of traditional scale weighing. No public dataset existed — Bruno built one. Pipeline: bovine → RGB+depth capture → edge processing → AI model → weight estimate.

**Tone:** Conversational, story-driven, self-reflective, encouraging. Direct address to students. Technically credible but accessible.

## Contact Info (for closing slide / QR code)
- Website: brunopinha.com
- LinkedIn: linkedin.com/in/brunopinha7
- WhatsApp: (44) 99185-7884
- Email: brunopinha@msn.com
