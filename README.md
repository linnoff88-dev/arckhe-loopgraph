ï»¿# ê°Å¸â¢Â¸ê¯Â¸Â Graph Engineering ê¢â¬â de loops a grafos

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Curso completo, em portuguêÂªs, sobre **graph engineering**: de loops isolados a grafos de agentes.
ComeêÂ§a do zero ê¢â¬â o que êÂ© um nêÂ³, o que êÂ© uma aresta ê¢â¬â e termina com vocêÂª desenhando, rodando e
depurando um grafo de agentes de verdade. Com o antêÂ­doto para o hype no meio do caminho.

**No ar:** https://inematds.github.io/loopgraph/

---

## A tese

> **Um loop jêÂ¡ êÂ© um grafo ê¢â¬â um grafo cujo caminho volta a um nêÂ³ anterior.**

VocêÂª nêÂ£o gradua de loops para grafos. VocêÂª **compêÂµe** loops em grafos quando um loop deixa de
bastar ê¢â¬â e paga por isso em prompts, em *state schema* e em novos modos de falha.
Acerte o loop primeiro; monte o grafo quando o trabalho exigir.

## As 5 trilhas

| # | Trilha | O que cobre |
|---|--------|-------------|
| 1 | **Fundamentos: o grafo** | NêÂ³, aresta, direêÂ§êÂ£o, peso, ciclo, DAG êÂ· sua manhêÂ£, o grafo social, o funil CAC/churn/LTV, o backlog, a documentaêÂ§êÂ£o, o build êÂ· travessia, caminho mêÂ­nimo, ordem topolêÂ³gica, paralelismo, detecêÂ§êÂ£o de ciclo |
| 2 | **Loop Engineering** | O ciclo descobrirê¢â âplanejarê¢â âagirê¢â âverificarê¢â âparar êÂ· condiêÂ§êÂ£o de parada em camadas êÂ· por que o **verificador êÂ© o gargalo** êÂ· as 4 falhas estruturais do loop |
| 3 | **Agentic êâ Loop êâ Graph** | As cinco camadas (prompt, contexto, harness, loop, grafo) êÂ· o mesmo caso construêÂ­do nas 3 arquiteturas êÂ· a tabela **mito êâ fato** contra o hype |
| 4 | **Graph Engineering na prêÂ¡tica** | NêÂ³s, arestas e estado êÂ· org graph êâ work graph êÂ· zone defense êÂ· fan-out/fan-in êÂ· state schema êÂ· modos de falha novos êÂ· observabilidade |
| 5 | **MêÂ£o na massa** | Migrar um caso real de loop para grafo (com critêÂ©rio pra **nêÂ£o** migrar) êÂ· modelar o grafo do negêÂ³cio e do backlog êÂ· biblioteca de 6 prompts copy-run |

**5 trilhas êÂ· 15 mêÂ³dulos êÂ· 90 têÂ³picos êÂ· ~10h**

## Como usar

Abre direto no navegador ê¢â¬â nêÂ£o precisa de build, servidor nem instalaêÂ§êÂ£o:

```bash
git clone git@github.com:inematds/loopgraph.git
cd loopgraph
xdg-open index.html      # ou simplesmente abra o arquivo
```

Cada pêÂ¡gina êÂ© self-contained (HTML + Tailwind via CDN + JS inline) e funciona em `file://`.

### Camada de aprendizagem

Progresso, dêÂºvidas e anotaêÂ§êÂµes ficam **no seu prêÂ³prio navegador** (`localStorage`) ê¢â¬â nada sobe pra
servidor nenhum:

- **Marcar como lido** por seêÂ§êÂ£o ê¢â¬â êÂ© o que faz o progresso andar (curso, trilha e mêÂ³dulo)
- **Tenho dêÂºvida** por têÂ³pico, e **grifo/anotaêÂ§êÂ£o** selecionando qualquer trecho do texto
- **Minha jornada** ê¢â¬â painel que agrega progresso, dêÂºvidas e notas, com "continuar de onde parei"
- **Export/import** do seu estado em `.json`
- Temas de leitura (claro, sêÂ©pia, foco, alto contraste) + tamanho, entrelinha e largura de linha

Se o JavaScript falhar ou o `localStorage` estiver bloqueado, o curso continua 100% legêÂ­vel.

## Estrutura do repositêÂ³rio

```
.
ê¢âÅê¢ââ¬ê¢ââ¬ index.html                 # landing
ê¢âÅê¢ââ¬ê¢ââ¬ capa/capa.png              # capa oficial
ê¢âÅê¢ââ¬ê¢ââ¬ assets/
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ learn.css / learn.js   # camada de aprendizagem (INEMA formato-curso-v2)
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ curso.css              # base + light mode das 5 trilhas
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ img/                   # diagramas usados nos mêÂ³dulos
ê¢âÅê¢ââ¬ê¢ââ¬ curso/trilha1..5/
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ index.html             # êÂ­ndice da trilha
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ modulo-N-M.html        # mêÂ³dulos
ê¢ââê¢ââ¬ê¢ââ¬ doc/
    ê¢âÅê¢ââ¬ê¢ââ¬ PLANO.md               # estrutura, decisêÂµes e conteêÂºdo de cada mêÂ³dulo
    ê¢âÅê¢ââ¬ê¢ââ¬ IMAGENS.md             # o que cada imagem mostra e onde êÂ© usada
    ê¢âÅê¢ââ¬ê¢ââ¬ auditar.mjs            # auditoria automêÂ¡tica do curso
    ê¢ââê¢ââ¬ê¢ââ¬ _template.html         # head/nav/footer canêÂ´nicos
```

### Auditoria

```bash
node doc/auditar.mjs
```

Valida por pêÂ¡gina: anti-FOUC antes do Tailwind, manifesto do curso idêÂªntico em todas as pêÂ¡ginas,
`topics` do manifesto batendo com os `data-inema-topic` reais do DOM, nav completo, INEMA.CLUB +
PRO, "Mapa da trilha", "Ver Completo" em cada card, mêÂ­nimo de 6 têÂ³picos por mêÂ³dulo, as 3 seêÂ§êÂµes
por têÂ³pico, SVG com `aria-label`, `alt` em toda imagem, code box com "Como verificar", e links e
imagens quebrados. Sai com cêÂ³digo 1 se achar problema.

## Fontes

Ponto de partida: o vêÂ­deo [*Larguei tudo pra aprender Graph Engineering*](https://www.youtube.com/watch?v=IYV_rqQpwcA).
Aprofundado com a discussêÂ£o pêÂºblica de julho de 2026 sobre o tema ê¢â¬â incluindo as posiêÂ§êÂµes cêÂ©ticas ê¢â¬â
e a documentaêÂ§êÂ£o de LangGraph, Microsoft AutoGen e Google ADK. Detalhes em `doc/PLANO.md`.

---

Feito com o formato **INEMA formato-curso-v2**.
[INEMA.CLUB](https://inema.club) êÂ· [PRO](https://inema.pro)

<!-- inema-backlink:v1 -->
## Mais no INEMA.CLUB

- [Ficha completa deste curso](https://www.inema.club/cursos/232-graph-engineering-de-loops-a-grafos/)
- [Guia: como aprender inteligêÂªncia artificial](https://www.inema.club/aprender-inteligencia-artificial/)
- [Todos os cursos](https://www.inema.club/cursos/)
<!-- /inema-backlink:v1 -->

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>