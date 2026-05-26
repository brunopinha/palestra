# Contexto do Projeto — Palestra Bruno Pinha

**Evento:** 8ª Semana de Tecnologia — Senac Maringá  
**Data:** 21 de maio de 2026, 21h–22h  
**Formato:** Auditório, ~200 pessoas, retroprojetor (possivelmente 1280×720 ou 1920×1080)  
**Palestrante:** Bruno Pinha Ribeiro

## Tese Central

"Minha carreira não foi definida pelas linguagens que dominei, mas pelos problemas que aprendi a resolver."

Metáfora estrutural: carreira como stack profissional — 7 camadas que se acumulam e convergem no PesoCam.

## Estado atual (sessão 26/05/2026)

**Fase:** validação de design — 4 slides prontos em `palestra-preview.html`

**4 slides de validação:**
- S1 (capa): full-bleed `fotos/intro-bg3.jpg`, corpo posicionado na metade direita (left:45%), títulos Bricolage Grotesque 800
- S3 (frase-tese): slide escuro puro, "linguagens" em teal, "problemas" em fuchsia
- S4 (stack): sidebar 300px + 7 linhas; barras teal com opacidade crescente, linha 07 PesoCam quebra em fuchsia
- S13 (hipótese PesoCam): "?" decorativo teal op.08, "sem contato físico?" em fuchsia, foto bovino coluna direita

**Bug S1 resolvido:** `#s1` NÃO pode ter `position: relative` ou qualquer override de position — herda `position:absolute; inset:0` do `.slide`. O `.s1-body` usa `position:absolute; top:0; right:0; bottom:0; left:45%`.

## Próximos passos

1. Bruno avalia os 4 slides do `palestra-preview.html` e aprova (ou ajusta) a direção
2. Construir todos os 24 slides no novo design system, substituindo `palestra-bruno-pinha.html`
3. Usar `roteiro-palestra-bruno-pinha.md` como referência de conteúdo slide a slide

## Arquivos

- `palestra-preview.html` — **ATIVO** — 4 slides de validação
- `palestra-bruno-pinha.html` — **OBSOLETO** — design âmbar anterior, não usar
- `roteiro-palestra-bruno-pinha.md` — roteiro completo minuto a minuto (conteúdo de referência)
- `bio-bruno-pinha.md` — bios em múltiplos tamanhos + script do mediador

## Fotos-chave

- `fotos/intro-bg3.jpg` — retrato P&B frontal, mão no queixo, fundo preto. CAPA (S1)
- `fotos/intro-bg.jpg` / `intro-bg2.jpg` — perfil lateral. Slides de transição/fechamento
- `fotos/pesocam/boi-selecao-visao-computacional.png` — bovino com bounding box. S13
- `fotos/conmaket_50_lojas.JPG` — Bruno na loja Conmarket. Slide de empreendedorismo
