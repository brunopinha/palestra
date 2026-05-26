# Design System — Decisões e Feedbacks

## O que NÃO usar

Bruno rejeita imediatamente o padrão "dark tech presentation" genérico:
- Fundo preto frio
- Verde neon ou gradientes roxo/azul
- Grid geométrico animado no fundo
- Blobs decorativos
- Fontes Inter, Space Grotesk, Roboto

Essa combinação aparece em Framer, Pitch e geradores de slides com IA — Bruno identifica como template.

## Design System atual (aprovado para validação em 26/05/2026)

### Paleta — Emerald/Teal/Fuchsia

Esta é a paleta oficial do PesoCam/Bruno (arquivo `fotos/paleta-cores.png`):

```css
--dark:         #091817;   /* emerald escuro profundo — bg principal */
--dark-mid:     #0e2322;
--dark-hi:      #104544;   /* emerald da paleta (#104544) */

--text:         #FFFAF5;   /* Snow — texto principal */
--text-mid:     #8db5b3;
--text-dim:     #3d7876;

--teal:         #249F9C;   /* Turquoise — accent principal */
--teal-dim:     rgba(36,159,156,.15);
--teal-glow:    rgba(36,159,156,.08);
--teal-dark:    #037A76;   /* Teal escuro */

--fuchsia:      #C11A63;   /* highlight máximo */
--fuchsia-dim:  rgba(193,26,99,.18);
--fuchsia-glow: rgba(193,26,99,.07);
```

### Tipografia

- **Display/títulos:** Bricolage Grotesque weight 800 — substituiu Syne. Mais impacto em retroprojetor, caráter industrial/construído.
- **Body:** Outfit
- **Labels/mono:** JetBrains Mono
- **Tamanho mínimo:** 28px. Títulos: `clamp(60px, 6.8vw, 90px)`

### Regra do Fuchsia

Fuchsia aparece em **no máximo 3 momentos** por apresentação — só nas viradas narrativas de máximo impacto. Exemplos nos 4 slides atuais:
1. Palavra "problemas" na frase-tese (S3)
2. Linha 07 PesoCam no stack (S4)
3. "sem contato físico?" na hipótese (S13)

O teal faz a cadência. O fuchsia quebra e surpreende.

### Por que esta paleta

- Emergald escuro é raríssimo em apresentações — imediatamente distinguível
- É a paleta de identidade do próprio Bruno/PesoCam (não foi inventada)
- Teal funciona melhor que âmbar em retroprojetor com luz ambiente (mais croma)
- Fuchsia cria contraste dramático sem ser arbitrário
