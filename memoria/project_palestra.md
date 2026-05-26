# Contexto do Projeto — Palestra Bruno Pinha

**Evento:** 8ª Semana de Tecnologia — Senac Maringá  
**Data:** 21 de maio de 2026, 21h–22h  
**Formato:** Auditório, ~200 pessoas, retroprojetor (possivelmente 1280×720 ou 1920×1080)  
**Palestrante:** Bruno Pinha Ribeiro

## Tese Central

"Minha carreira não foi definida pelas linguagens que dominei, mas pelos problemas que aprendi a resolver."

Metáfora estrutural: carreira como stack profissional — 7 camadas que se acumulam e convergem no PesoCam.

## Estado atual (sessão 26/05/2026 — encerrada)

**Fase:** entrega pronta. 24 slides finalizados, deploy ativo, contingências geradas.

### Entregáveis online (FTP brunopinha.com em `/public_html/palestra/`)

- **`index.html`** — apresentação interativa (renomeada de `palestra-bruno-pinha.html`) — Plano A
- **`palestra-bruno-pinha.pdf`** — PDF 16:9 (1920×1080) pixel-perfect, 24 páginas, 42MB — Plano B offline
- **`cue-cards-bruno-pinha.docx`** — 24 cue cards A4 (2 col × 3 lin = 6/página, 4 páginas) — Plano C físico

URLs:
- https://brunopinha.com/palestra/
- https://brunopinha.com/palestra/palestra-bruno-pinha.pdf
- https://brunopinha.com/palestra/cue-cards-bruno-pinha.docx

### Design system (consolidado)

Paleta Emerald/Teal/Fuchsia (`--dark #091817`, `--teal #249F9C`, `--fuchsia #C11A63`), tipografia Bricolage Grotesque (display) + Outfit (body) + JetBrains Mono (labels).

**Fuchsia (4 momentos):**
- S3 "problemas"
- S4 linha 07 PesoCam
- S13 "sem contato físico?"
- S17 "IA · câmera · algoritmo" (adicionado a pedido)

**Responsividade:** todo o deck usa `clamp()` em fontes, paddings e gaps — testado para 1280×720 e 1920×1080.

**Bug crítico resolvido (fix sistêmico):** todos os 24 slides (inclusive templates `.tpl-camada`, `.tpl-fourcards`) têm `position: absolute; inset: 0` nos containers internos — garante centralização Y real em qualquer viewport.

### Mapa de fotos (versão final)

| Slide | Foto | Pasta |
|---|---|---|
| S1 | intro-bg3.jpg | fotos/ |
| S9 (Empreendedorismo) | conmaket_50_lojas.JPG | fotos/ |
| S10 (Mestrado UEM) | mestrao-uem.jpg | fotos/ |
| S11 (PesoCam pico) | Bruno-Pinha-PesoCam.png | fotos/pesocam/ |
| S12 (Problema) | bovinos.png | fotos/pesocam/ |
| S13 (Hipótese) | boi-selecao-visao-computacional.png | fotos/pesocam/ |
| S14 (Pipeline) | produto-mvp.png (MVP do produto) | fotos/ |
| S18 (Validações) | logos: gdin.jpg + incubadora-ivaipora.png (Korean Valley) + logo-uem.png | fotos/logos/ |
| S22 (Networking) | reuniao-de-trabalho-deepfarm.png | fotos/pesocam/ |
| S23 (Docência) | aula-api-first.png (Bruno ministrando Meet Up) | fotos/ |
| S24 (Fechamento) | pesocam-logo-branca-fundo-transparente.png + QR via api.qrserver.com | fotos/pesocam/ |

**Logo PesoCam:** versão branca com transparência (`pesocam-logo-branca-fundo-transparente.png`) — substitui a versão tom escuro anterior, melhor pra fundo emerald.

### Templates CSS

- `.tpl-camada` (+ `.with-photo`, `.peak`) — S5–S11 (camadas da stack)
- `.tpl-fourcards` — S20 (princípios) e S21 (pilares), com overrides #s20 / #s21 (2-col, flat progressivo)
- `@media print` — força layout 1920×1080 por slide com `page-break-after` para o PDF de contingência

### Scripts auxiliares

- `gen-cue-cards.py` — gera DOCX dos cue cards a partir dos `data-notes` do HTML. Rodar com `python3 gen-cue-cards.py` (requer `python-docx` e `beautifulsoup4`).
- Geração do PDF: `chromium-browser --headless --print-to-pdf=palestra-bruno-pinha.pdf --no-pdf-header-footer --window-size=1920,1080 file:///root/palestra/palestra-bruno-pinha.html`

## Próximos passos (pré-palco)

Bruno deve, antes do dia 21/05:
1. Baixar o PDF no notebook que vai usar e guardar offline
2. Testar a URL `brunopinha.com/palestra/` em fullscreen (tecla F) no notebook
3. Escanear o QR do S24 com o celular pra confirmar abertura do WhatsApp
4. Cronometrar a passagem inteira com notas (tecla N) — verificar caber em 60min
5. Imprimir o DOCX em A4 → cortar nas linhas tracejadas → 24 cue cards físicos

## Arquivos do repositório

- `palestra-bruno-pinha.html` — apresentação 24 slides (single file, CSS embutido)
- `palestra-bruno-pinha.pdf` — PDF de contingência (42MB, gerado via Chromium)
- `cue-cards-bruno-pinha.docx` — DOCX dos cue cards (gerado via python-docx)
- `gen-cue-cards.py` — script gerador dos cue cards
- `roteiro-palestra-bruno-pinha.md` — roteiro minuto a minuto (referência)
- `bio-bruno-pinha.md` — bios em múltiplos tamanhos + script do mediador
- `palestra-preview.html` — referência dos 4 slides originais de validação
- `fotos/` — todos os assets
- `memoria/` — contexto de sessão (este arquivo + `feedback_design_autoral.md`)
