# ðŸ•¸ï¸ Graph Engineering â€” de loops a grafos

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Curso completo, em portuguÃªs, sobre **graph engineering**: de loops isolados a grafos de agentes.
ComeÃ§a do zero â€” o que Ã© um nÃ³, o que Ã© uma aresta â€” e termina com vocÃª desenhando, rodando e
depurando um grafo de agentes de verdade. Com o antÃ­doto para o hype no meio do caminho.

**No ar:** https://inematds.github.io/loopgraph/

---

## A tese

> **Um loop jÃ¡ Ã© um grafo â€” um grafo cujo caminho volta a um nÃ³ anterior.**

VocÃª nÃ£o gradua de loops para grafos. VocÃª **compÃµe** loops em grafos quando um loop deixa de
bastar â€” e paga por isso em prompts, em *state schema* e em novos modos de falha.
Acerte o loop primeiro; monte o grafo quando o trabalho exigir.

## As 5 trilhas

| # | Trilha | O que cobre |
|---|--------|-------------|
| 1 | **Fundamentos: o grafo** | NÃ³, aresta, direÃ§Ã£o, peso, ciclo, DAG Â· sua manhÃ£, o grafo social, o funil CAC/churn/LTV, o backlog, a documentaÃ§Ã£o, o build Â· travessia, caminho mÃ­nimo, ordem topolÃ³gica, paralelismo, detecÃ§Ã£o de ciclo |
| 2 | **Loop Engineering** | O ciclo descobrirâ†’planejarâ†’agirâ†’verificarâ†’parar Â· condiÃ§Ã£o de parada em camadas Â· por que o **verificador Ã© o gargalo** Â· as 4 falhas estruturais do loop |
| 3 | **Agentic Ã— Loop Ã— Graph** | As cinco camadas (prompt, contexto, harness, loop, grafo) Â· o mesmo caso construÃ­do nas 3 arquiteturas Â· a tabela **mito Ã— fato** contra o hype |
| 4 | **Graph Engineering na prÃ¡tica** | NÃ³s, arestas e estado Â· org graph Ã— work graph Â· zone defense Â· fan-out/fan-in Â· state schema Â· modos de falha novos Â· observabilidade |
| 5 | **MÃ£o na massa** | Migrar um caso real de loop para grafo (com critÃ©rio pra **nÃ£o** migrar) Â· modelar o grafo do negÃ³cio e do backlog Â· biblioteca de 6 prompts copy-run |

**5 trilhas Â· 15 mÃ³dulos Â· 90 tÃ³picos Â· ~10h**

## Como usar

Abre direto no navegador â€” nÃ£o precisa de build, servidor nem instalaÃ§Ã£o:

```bash
git clone git@github.com:inematds/loopgraph.git
cd loopgraph
xdg-open index.html      # ou simplesmente abra o arquivo
```

Cada pÃ¡gina Ã© self-contained (HTML + Tailwind via CDN + JS inline) e funciona em `file://`.

### Camada de aprendizagem

Progresso, dÃºvidas e anotaÃ§Ãµes ficam **no seu prÃ³prio navegador** (`localStorage`) â€” nada sobe pra
servidor nenhum:

- **Marcar como lido** por seÃ§Ã£o â€” Ã© o que faz o progresso andar (curso, trilha e mÃ³dulo)
- **Tenho dÃºvida** por tÃ³pico, e **grifo/anotaÃ§Ã£o** selecionando qualquer trecho do texto
- **Minha jornada** â€” painel que agrega progresso, dÃºvidas e notas, com "continuar de onde parei"
- **Export/import** do seu estado em `.json`
- Temas de leitura (claro, sÃ©pia, foco, alto contraste) + tamanho, entrelinha e largura de linha

Se o JavaScript falhar ou o `localStorage` estiver bloqueado, o curso continua 100% legÃ­vel.

## Estrutura do repositÃ³rio

```
.
â”œâ”€â”€ index.html                 # landing
â”œâ”€â”€ capa/capa.png              # capa oficial
â”œâ”€â”€ assets/
â”‚   â”œâ”€â”€ learn.css / learn.js   # camada de aprendizagem (INEMA formato-curso-v2)
â”‚   â”œâ”€â”€ curso.css              # base + light mode das 5 trilhas
â”‚   â””â”€â”€ img/                   # diagramas usados nos mÃ³dulos
â”œâ”€â”€ curso/trilha1..5/
â”‚   â”œâ”€â”€ index.html             # Ã­ndice da trilha
â”‚   â””â”€â”€ modulo-N-M.html        # mÃ³dulos
â””â”€â”€ doc/
    â”œâ”€â”€ PLANO.md               # estrutura, decisÃµes e conteÃºdo de cada mÃ³dulo
    â”œâ”€â”€ IMAGENS.md             # o que cada imagem mostra e onde Ã© usada
    â”œâ”€â”€ auditar.mjs            # auditoria automÃ¡tica do curso
    â””â”€â”€ _template.html         # head/nav/footer canÃ´nicos
```

### Auditoria

```bash
node doc/auditar.mjs
```

Valida por pÃ¡gina: anti-FOUC antes do Tailwind, manifesto do curso idÃªntico em todas as pÃ¡ginas,
`topics` do manifesto batendo com os `data-inema-topic` reais do DOM, nav completo, INEMA.CLUB +
PRO, "Mapa da trilha", "Ver Completo" em cada card, mÃ­nimo de 6 tÃ³picos por mÃ³dulo, as 3 seÃ§Ãµes
por tÃ³pico, SVG com `aria-label`, `alt` em toda imagem, code box com "Como verificar", e links e
imagens quebrados. Sai com cÃ³digo 1 se achar problema.

## Fontes

Ponto de partida: o vÃ­deo [*Larguei tudo pra aprender Graph Engineering*](https://www.youtube.com/watch?v=IYV_rqQpwcA).
Aprofundado com a discussÃ£o pÃºblica de julho de 2026 sobre o tema â€” incluindo as posiÃ§Ãµes cÃ©ticas â€”
e a documentaÃ§Ã£o de LangGraph, Microsoft AutoGen e Google ADK. Detalhes em `doc/PLANO.md`.

---

Feito com o formato **INEMA formato-curso-v2**.
[INEMA.CLUB](https://inema.club) Â· [PRO](https://inema.pro)

<!-- inema-backlink:v1 -->
## Mais no INEMA.CLUB

- [Ficha completa deste curso](https://www.inema.club/cursos/232-graph-engineering-de-loops-a-grafos/)
- [Guia: como aprender inteligÃªncia artificial](https://www.inema.club/aprender-inteligencia-artificial/)
- [Todos os cursos](https://www.inema.club/cursos/)
<!-- /inema-backlink:v1 -->

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>