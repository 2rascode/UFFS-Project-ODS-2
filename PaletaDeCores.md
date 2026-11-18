# Paleta de cores - Mapa Solidário

## Conceito visual e psicologia das cores

A paleta do Mapa Solidário combina verdes, oliva, amarelos, dourados e tons terrosos. Esta leitura relaciona as cores existentes no projeto à agricultura sustentável, ao alimento, ao acolhimento e à mobilização social.

As associações abaixo são **interpretações de design para este projeto**, não resultados de testes com seus visitantes. A psicologia das cores considera que o significado e a resposta a uma cor dependem do contexto; não existe garantia de que uma tonalidade provoque a mesma emoção em todas as pessoas. Essa cautela acompanha a revisão de Elliot e Maier (2014).

| Família | Associação pretendida | Relação com o Mapa Solidário |
| --- | --- | --- |
| Verde | Natureza, crescimento, renovação e cuidado. | Aproxima a identidade da agricultura, da sustentabilidade e da manutenção da vida. |
| Oliva escuro | Sobriedade, estabilidade e proximidade com a terra. | Dá uma base discreta à navegação e sustenta a identidade ligada ao ambiente rural. |
| Amarelo e âmbar | Calor, energia, esperança e atenção. | Destaca chamadas e títulos; remete visualmente à luz e à colheita. |
| Creme | Suavidade e acolhimento. | Mantém textos e títulos dentro de uma identidade quente, com contraste visual sobre verdes escuros. |
| Ocre e dourado terroso | Terra, cultivo e colheita. | Conecta as seções de participação social ao tema alimentar. |
| Coral suave | Atenção e sensibilidade diante de uma situação crítica. | Evidencia insegurança alimentar nos gráficos sem depender de um vermelho intenso. |
| Branco e preto translúcido | Clareza, separação e profundidade. | Apoiam foco, bordas, superfícies e sombras de texto. |

## Valores utilizados na interface

Os valores abaixo foram extraídos de `src/css/output.css`, considerando as famílias de cores referenciadas em `src/Index.html`. O CSS compilado utiliza **OKLCH**; esses valores são mantidos para documentar precisamente a implementação, sem substituir por códigos hexadecimais de outra versão do Tailwind.

| Token | Valor exato no CSS |
| --- | --- |
| amber-100 | oklch(96.2% 0.059 95.617) |
| amber-200 | oklch(92.4% 0.12 95.746) |
| amber-300 | oklch(87.9% 0.169 91.605) |
| amber-400 | oklch(82.8% 0.189 84.429) |
| amber-50 | oklch(98.7% 0.022 95.277) |
| amber-500 | oklch(76.9% 0.188 70.08) |
| amber-700 | oklch(55.5% 0.163 48.998) |
| amber-800 | oklch(47.3% 0.137 46.201) |
| green-600 | oklch(62.7% 0.194 149.214) |
| green-700 | oklch(52.7% 0.154 150.069) |
| green-800 | oklch(44.8% 0.119 151.328) |
| green-950 | oklch(26.6% 0.065 152.934) |
| lime-300 | oklch(89.7% 0.196 126.665) |
| olive-800 | oklch(28.6% 0.016 107.4) |
| yellow-100 | oklch(97.3% 0.071 103.193) |
| yellow-500 | oklch(79.5% 0.184 86.047) |

### Aplicações principais

| Elemento | Cores/classes presentes | Intenção de comunicação |
| --- | --- | --- |
| Cabeçalho e menu lateral | `bg-olive-800`, `text-yellow-100` e `text-amber-400` | Base sóbria com identificação e navegação em tons acolhedores. |
| Botão do menu | `bg-green-700`, `text-yellow-500` | Continuidade com a identidade agrícola e destaque do controle. |
| Apresentação | `bg-amber-200/50`, `text-yellow-100`, `text-amber-100` e `text-amber-400` | Atmosfera quente e receptiva sobre o vídeo. |
| Explorar Mapa | `bg-amber-300`, `hover:bg-amber-400`, `text-amber-50` | Destaque para iniciar a exploração. |
| Buscar Iniciativas | `bg-amber-700`, `hover:bg-amber-800`, `text-amber-50` | Tom terroso para uma chamada complementar. |
| Seção de dados | `bg-green-600/60`, `text-yellow-100`, `text-amber-100/80` | Integração entre informação, cuidado e sustentabilidade. |
| Seção do mapa | `bg-green-800`, `text-yellow-100` | Base escura que separa o mapa e os dados do fundo. |
| Regiões do mapa | `fill-lime-300`, `fill-amber-300` em seleção/hover | Verde-lima identifica as regiões; âmbar evidencia a interação. |
| Contornos e nomes no mapa | `stroke-green-950`, `fill-green-950` | Delimitação e leitura sobre preenchimentos claros. |
| Foco no mapa | Branco | Diferencia a navegação por teclado. |

O HTML também referencia `bg-green-900` no rodapé, mas a variável `--color-green-900` não foi encontrada na folha compilada consultada. Por isso, não é apresentada aqui como uma cor efetivamente definida nesse arquivo.

As cores das regiões do mapa representam **estados de interação**, e não uma escala de gravidade da insegurança alimentar.

## Gradiente das seções de participação

As seções `#ongs` e `#como-ajudar` utilizam a mesma combinação:

| Nome descritivo | HEX exato | Aplicação | Associação proposta |
| --- | --- | --- | --- |
| Dourado terroso | `#CCB366` | Início e fim do gradiente. | Colheita, calor e alimento. |
| Oliva ocre | `#8D871B` | Centro do gradiente. | Terra, cultivo e continuidade com os verdes. |

```css
linear-gradient(110deg, #ccb366, #8d871b, #ccb366)
```

O gradiente possui animação de posição com duração de oito segundos, alternada e infinita, aplicada por uma variante `motion-safe`. As duas seções ainda não possuem conteúdo textual.

## Paleta complementar dos gráficos

Os arquivos `graph1.svg`, `graph2.svg` e `graph3.svg` possuem valores próprios. Eles complementam a paleta da interface; não são equivalentes automáticos às classes Tailwind.

| Nome descritivo | HEX exato | Uso nos SVGs | Relação conceitual |
| --- | --- | --- | --- |
| Verde suave | `#7BA77F` | Linhas separadoras. | Organização discreta e continuidade visual. |
| Creme suave | `#EDE9BB` | Fontes dos dados, rótulos e textos complementares. | Acolhimento e unidade com os amarelos da página. |
| Creme luminoso | `#FFF6C5` | Títulos, números e textos principais. | Ênfase e clareza visual dentro da paleta quente. |
| Coral suave | `#FFB3A3` | Número de domicílios afetados, insegurança grave e barras de Norte/Nordeste. | Atenção para a vulnerabilidade. |
| Verde claro | `#A6CAA5` | Faixa e legenda de segurança alimentar no gráfico nacional. | Condição favorável e cuidado. |
| Amarelo dourado | `#FFCB62` | Insegurança alimentar leve ou moderada. | Sinalização de atenção intermediária. |
| Verde médio | `#51875E` | Apoio gráfico na comparação regional. | Estrutura e integração com o tema ambiental. |
| Verde-lima suave | `#C8EC84` | Outras barras regionais e destaques do Mesa Brasil. | Vitalidade e valorização das ações de assistência. |

As cores devem ser interpretadas junto dos textos, números e legendas. Por exemplo, o coral também destaca o total de domicílios afetados; seu significado depende do elemento em que aparece.

## Transparência e leitura

Os modificadores de opacidade fazem parte da aparência final: `bg-amber-200/50` usa 50% de opacidade, `bg-green-600/60` usa 60% e `text-amber-100/80` usa 80%. A cor percebida depende do fundo ou do vídeo abaixo desses elementos.

As sombras de títulos utilizam `#0008`, equivalente a preto com aproximadamente 53% de opacidade. Branco também aparece em foco e em detalhes de apoio.

A justificativa psicológica não substitui a avaliação de legibilidade. Combinações claras, como texto creme sobre âmbar claro, e textos sobre vídeo precisam ser avaliadas no resultado renderizado. Este documento registra a paleta existente; não afirma que todas as combinações já passaram por uma verificação de contraste.

## Síntese da identidade

A leitura proposta é: **verdes para natureza e cuidado; amarelos e cremes para acolhimento e atenção; ocres para terra e colheita; coral para destacar a vulnerabilidade nos dados**. A combinação conecta visualmente o conteúdo informativo à proposta de solidariedade do projeto.

## Referências

- ELLIOT, Andrew J.; MAIER, Markus A. **Color psychology: effects of perceiving color on psychological functioning in humans**. Annual Review of Psychology, v. 65, p. 95–120, 2014. DOI: [10.1146/annurev-psych-010213-115035](https://doi.org/10.1146/annurev-psych-010213-115035). Base para contextualizar os limites das interpretações psicológicas; não valida individualmente as associações propostas nesta paleta.
- **Fontes da implementação:** `src/Index.html`, `src/css/input.css`, `src/css/output.css` e `src/assets/img/graph1.svg`, `graph2.svg`, `graph3.svg`.
