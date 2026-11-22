# Paleta de cores

O Mapa Solidário utiliza verdes, amarelos e tons terrosos para aproximar sua identidade visual da agricultura sustentável e do combate à fome, temas da ODS 2. A escolha busca tornar a página acolhedora para pessoas interessadas em segurança alimentar e em apoiar iniciativas sociais.

| Cor | Código hexadecimal | Aplicação e justificativa |
| --- | --- | --- |
| Oliva escuro | `#2B2B22` | Fundo do cabeçalho e do menu. Cria uma base discreta para a navegação e remete aos tons da terra. |
| Verde escuro | `#016630` | Fundo da seção do mapa. Reforça a relação com a natureza e a agricultura. |
| Creme | `#FEF9C2` | Títulos e textos sobre fundos escuros. Mantém a aparência acolhedora e favorece o contraste nessas combinações. |
| Amarelo âmbar | `#FFB900` | Destaques e elementos de navegação. Busca chamar a atenção e remeter à luz e à colheita. |
| Amarelo claro | `#FFD230` | Botão de exploração e destaque das regiões do mapa durante a interação. |
| Dourado terroso | `#CCB366` | Gradiente das seções de participação. Aproxima essas áreas da ideia de alimento e colheita. |
| Oliva ocre | `#8D871B` | Complemento do gradiente. Dá continuidade aos tons ligados ao cultivo. |
| Coral suave | `#FFB3A3` | Destaques nos gráficos sobre insegurança alimentar. Direciona a atenção aos dados de vulnerabilidade. |

Essas associações expressam a intenção visual do projeto. Nos gráficos, as cores são acompanhadas de textos e legendas para facilitar a compreensão dos dados.

Os códigos das cores da interface são aproximações em hexadecimal sRGB dos valores registrados no documento original, arredondadas para 8 bits por canal. Os códigos do gradiente e do coral já estavam definidos em hexadecimal.

## Contraste e legibilidade

Para textos comuns, a referência é uma relação de contraste de pelo menos 4,5:1, conforme o nível AA das WCAG. Os cálculos abaixo consideram cores sólidas, sem transparência.

| Texto | Fundo | Contraste aproximado | Avaliação para texto comum |
| --- | --- | --- | --- |
| Creme `#FEF9C2` | Oliva escuro `#2B2B22` | 13,28:1 | Atende ao nível AA. |
| Creme `#FEF9C2` | Verde escuro `#016630` | 6,64:1 | Atende ao nível AA. |
| Creme claro `#FFFBEB` | Amarelo claro `#FFD230` | 1,40:1 | Precisa de ajuste. |
| Verde muito escuro `#032E15` | Amarelo claro `#FFD230` | 10,33:1 | Alternativa recomendada para o texto do botão. |

No botão “Explorar Mapa”, recomenda-se substituir o texto creme claro pelo verde muito escuro. Essa é uma proposta de ajuste; o site não foi alterado. Textos sobre vídeo, gradientes ou fundos transparentes precisam ser conferidos na página, pois o contraste varia conforme a imagem de fundo.

## Referências para conferência

- [Adobe Color](https://color.adobe.com/br/create/color-wheel): permite visualizar as cores e explorar combinações da paleta.
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/): permite inserir o hexadecimal do texto em “Foreground” e o do fundo em “Background” para conferir a relação de contraste e o resultado WCAG AA.
- [Cores do Tailwind CSS](https://tailwindcss.com/docs/colors): referência para consultar a paleta do framework. Cores personalizadas e diferenças entre versões devem ser conferidas no CSS do próprio projeto.

As ferramentas ajudam a conferir os valores e a legibilidade das combinações. As justificativas ligadas ao tema representam escolhas de design.
