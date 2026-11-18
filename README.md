# Mapa Solidário - UFFS / ODS 2

Landing page acadêmica sobre insegurança alimentar e iniciativas de solidariedade, desenvolvida na disciplina de Introdução ao Desenvolvimento Web do curso de Ciência da Computação da Universidade Federal da Fronteira Sul (UFFS), Campus Chapecó.

O projeto relaciona a apresentação de dados ao **Objetivo de Desenvolvimento Sustentável 2 — Fome Zero e Agricultura Sustentável**, com foco na Meta 2.1: acesso à alimentação segura, nutritiva e suficiente.

## Objetivo

Facilitar o acesso a informações sobre insegurança alimentar, permitir a identificação de localidades vulneráveis e incentivar o conhecimento de organizações e iniciativas de assistência alimentar.

O site tem caráter informativo e educativo. A divulgação de organizações e das formas de ajudar faz parte da proposta, mas essas seções ainda estão em construção.

## Abrangência

O recorte principal é **Pernambuco**, incluindo Recife e outros municípios do estado. Gráficos nacionais e regionais contextualizam o tema.

O mapa apresenta as cinco regiões brasileiras, mas a tabela municipal disponível é a de Pernambuco, acessada pela região Nordeste. As demais regiões exibem uma indicação para consultar esse recorte.

## Estrutura e estágio atual

| Seção | Identificador | Conteúdo e situação |
| --- | --- | --- |
| Início | `#hero` | Apresentação do Mapa Solidário, vídeo de fundo e chamadas para exploração. |
| Apresentação de dados | `#dados` | Texto de sensibilização e três gráficos em SVG sobre Brasil, regiões brasileiras e a atuação do Mesa Brasil em Pernambuco. |
| Mapa do Brasil | `#mapa` | Mapa SVG navegável por região e tabela expansível de municípios de Pernambuco. |
| Organizações e projetos | `#ongs` | Estrutura visual criada; conteúdo ainda não preenchido. |
| Como ajudar | `#como-ajudar` | Estrutura visual criada; conteúdo ainda não preenchido. |
| Rodapé | `#footer` | Estrutura criada; conteúdo ainda não preenchido. |

O cabeçalho fixo possui um menu lateral com links internos. O botão **Explorar Mapa** aponta para o mapa; **Buscar Iniciativas** ainda utiliza `href="#"`, sem um destino específico.

## Recursos implementados

- Menu lateral controlado por checkbox e componentes CSS do daisyUI.
- Navegação entre regiões por âncoras, `:target`, `:has()` e variantes do Tailwind.
- Tabela de Pernambuco com município, famílias em risco e percentual no CadÚnico, organizada do maior percentual para o menor.
- Abertura e fechamento da tabela com os elementos nativos `details` e `summary`.
- Gráficos estáticos em SVG e vídeo local na apresentação.
- Layouts com variantes responsivas e animação de gradiente condicionada a `motion-safe`.

A página não possui JavaScript de aplicação, backend, banco de dados ou atualização automática dos indicadores. Os conteúdos estão nos arquivos HTML e SVG.

## Tecnologias

| Tecnologia | Uso |
| --- | --- |
| HTML | Estrutura, conteúdo, âncoras e controles nativos. |
| CSS | Tipografia, animações e regras complementares de interação. |
| Tailwind CSS | Classes utilitárias e geração da folha de estilos. |
| Tailwind CLI | Compilação de `input.css` para `output.css`. |
| daisyUI | Componentes como navbar, drawer, menu e botões. |
| SVG | Mapa e gráficos. |

O `package.json` declara Tailwind CSS e CLI `^4.3.5`, daisyUI `^5.7.50` e nira-ui `^1.27.0`. O nira-ui consta como dependência, mas não possui importação explícita nos arquivos HTML e CSS consultados.

## Organização dos arquivos

| Caminho | Finalidade |
| --- | --- |
| `Readme.md` | Documentação geral do projeto. |
| `PALETA_DE_CORES.md` | Paleta utilizada e sua relação com a psicologia das cores. |
| `src/Index.html` | Página principal, mapa e tabela municipal. |
| `src/css/input.css` | Entrada do Tailwind, plugin daisyUI, fontes e CSS personalizado. |
| `src/css/output.css` | Folha de estilos compilada, carregada pela página. |
| `src/assets/fonts/` | Arquivos locais da fonte Milesdane. |
| `src/assets/icons/` | Ícones do projeto. |
| `src/assets/img/` | Marca e gráficos SVG. |
| `src/assets/video/` | Vídeo de fundo. |
| `src/package.json` | Dependências do projeto. |
| `src/package-lock.json` | Registro das versões das dependências. |

## Como visualizar

Abra `src/Index.html` em um navegador moderno. A folha `src/css/output.css` já está presente no projeto.

Também é possível abrir a página por um servidor estático local, como o Live Server do VS Code. Preserve o nome `Index.html`, com inicial maiúscula, ao informar o caminho em ambientes que diferenciam maiúsculas de minúsculas.

## Como recompilar os estilos

É necessário ter Node.js e npm disponíveis. No terminal, a partir da raiz do repositório:

```powershell
cd src
npm ci
npx @tailwindcss/cli -i ./css/input.css -o ./css/output.css --watch
```

O modo `--watch` mantém a compilação ativa durante as alterações. Para gerar a folha uma única vez:

```powershell
npx @tailwindcss/cli -i ./css/input.css -o ./css/output.css --minify
```

Os comandos de compilação devem ser executados dentro de `src`. O projeto não define scripts npm como `npm start` ou `npm run dev`.

## Dados e fontes

As seguintes fontes estão identificadas nos materiais da página:

- **IBGE — PNAD Contínua, Segurança Alimentar 2024:** contexto nacional e regional nos gráficos.
- **MDS — Brasil Sem Fome:** referência complementar indicada no gráfico regional.
- **Sesc Mesa Brasil Pernambuco:** balanço identificado no terceiro gráfico como publicado em 29 de setembro de 2026.
- **IBGE — malhas territoriais:** referência dos limites regionais, com [link presente na página](https://servicodados.ibge.gov.br/api/docs/malhas?versao=3).

A tabela municipal apresenta famílias em risco e percentual no CadÚnico. Esses indicadores possuem um universo diferente dos percentuais de domicílios da PNAD; não devem ser interpretados como uma única série diretamente comparável. A origem específica e a data de referência da tabela precisam acompanhar sua documentação.

Esta descrição registra o conteúdo dos arquivos; não representa uma validação independente dos números apresentados.

## Identidade visual

A identidade combina verdes, oliva, amarelos e tons terrosos, relacionados visualmente à agricultura, ao alimento e à solidariedade. A fonte Milesdane aparece na marca e nos títulos; Arial é utilizada em textos.

Consulte [Paleta de cores e psicologia das cores](./PALETA_DE_CORES.md) para os valores registrados no código, as aplicações e a justificativa conceitual.

## Autoria e contexto acadêmico

**Autores:** David Sulbaran e Ruan Arthur Both.  
**Instituição:** Universidade Federal da Fronteira Sul — Campus Chapecó.  
**Curso:** Ciência da Computação.  
**Disciplina:** Introdução ao Desenvolvimento Web.  
**Ano:** 2026.
