# Mapa Solidário

Projeto acadêmico desenvolvido por **David Sulbaran e Ruan Both**, na disciplina de **Introdução ao Desenvolvimento Web**, do curso de **Ciência da Computação da Universidade Federal da Fronteira Sul — Campus Chapecó**.

A landing page aborda o **ODS 2 — Fome Zero e Agricultura Sustentável**, reunindo informações sobre insegurança alimentar, dados municipais de Pernambuco e iniciativas que apoiam a causa.

## Objetivo

Facilitar o acesso à informação e apresentar caminhos para a participação em ações solidárias. O site permite conhecer dados, explorar as regiões do Brasil e encontrar organizações que recebem apoio.

## Seções

- **Início:** apresentação do projeto com vídeo de fundo.
- **Apresentação de dados:** contextualização e gráficos informativos.
- **Mapa do Brasil:** mapa SVG com seleção das cinco regiões; os dados disponíveis estão restritos a Pernambuco, na região Nordeste.
- **Organizações e projetos:** Mãos que Alimentam, SERTA e Centro Sabiá.
- **Como ajudar:** links externos para doações e voluntariado.
- **Rodapé:** identidade do projeto, navegação e créditos acadêmicos.

## Tecnologias

- HTML5 e CSS.
- Tailwind CSS 4, com compilação local pelo `@tailwindcss/cli`.
- DaisyUI 5, utilizado nos componentes de interface.
- SVG para o mapa e os gráficos.

O site não utiliza JavaScript. O menu lateral funciona com um checkbox e CSS; a seleção das regiões utiliza âncoras, `:target` e `:has()`; a tabela de Pernambuco é expandida com `<details>` e `<summary>`.

O `package.json` também declara `nira-ui`, mantido conforme a configuração original. Não há importação desse pacote no HTML ou no CSS desta página.

## Estrutura

```text
README.md
PaletaDeCores.md
src/
  Index.html
  package.json
  package-lock.json
  css/
    input.css
    output.css
  assets/
    fonts/
    icons/
    img/
    video/
```

- `Index.html`: conteúdo, estrutura e classes dos componentes.
- `input.css`: configuração do Tailwind, fonte local, componentes, responsividade, animação do gradiente e interações do mapa.
- `output.css`: arquivo gerado pelo Tailwind e carregado pela página; não deve ser editado manualmente.
- `assets/`: arquivos originais de imagens, fontes, ícones e vídeo.
- `PaletaDeCores.md`: documentação das cores do projeto.

## Como executar

É necessário ter Node.js e npm instalados para compilar o CSS.

No terminal, entre na pasta `src` do projeto:

```bash
cd src
npm install
```

Compile o CSS:

```bash
npx @tailwindcss/cli -i ./css/input.css -o ./css/output.css --minify
```

Para recompilar automaticamente durante as alterações:

```bash
npx @tailwindcss/cli -i ./css/input.css -o ./css/output.css --watch
```

Abra `src/Index.html` no navegador ou utilize um servidor local, como o Live Server do VS Code. Se o `output.css` já estiver compilado e os arquivos de `assets` estiverem presentes, não é necessário instalar dependências apenas para visualizar a página.

O nome do arquivo é **`Index.html`**, com inicial maiúscula. Em hospedagens que exigem `index.html` minúsculo como página inicial, ajuste o nome e a declaração `@source` do `input.css` em conjunto.

## Organização dos estilos

As classes utilitárias permanecem no HTML para ajustes simples. Estilos de componentes e padrões repetidos ficam em `@layer components` no `input.css`, utilizando `@apply` quando apropriado.

Os principais grupos são:

- Cabeçalho e menu: `.site-header`, `.site-navbar`, `.sidebar-panel` e `.sidebar-copyright`.
- Apresentação: `.hero-section`, `.hero-title` e `.hero-actions`.
- Dados: `.data-section`, `.data-description` e `.data-charts`.
- Mapa e tabela: `.map-layout`, `.regiao`, `.painel-regiao` e `.municipal-table`.
- Organizações: `.organizations-grid` e `.organization-card`.
- Participação e rodapé: `.help-content`, `.footer-columns` e `.footer-bottom`.

Para alterar o comportamento das regiões, preserve a relação entre `mapa-regiao-N`, `painel-regiao-N` e as regras correspondentes no CSS. As formas SVG e os dados da tabela ficam no HTML.

## Responsividade e navegação

- Títulos com tamanho fluido e espaçamento adaptável à largura da tela.
- Cabeçalho flexível e menu lateral limitado à largura disponível.
- Créditos do menu posicionados com `margin-top: auto`, sem blocos vazios de espaçamento.
- Cards com altura mínima e crescimento conforme o conteúdo.
- Seção “Como ajudar” no fluxo normal da página, evitando sobreposição com o rodapé.
- Mapa e dados em uma coluna nas telas menores e duas colunas a partir de `64rem`.
- Tabela com rolagem dentro do próprio contêiner, sem exigir que a página inteira role horizontalmente.
- Rodapé com colunas adaptáveis e espaço para quebra de texto.
- Espaçamento de navegação para compensar o cabeçalho fixo.
- Animação do gradiente condicionada à preferência de movimento do usuário.

Utilize um navegador atualizado com suporte a `:has()`, unidades de viewport modernas e aos recursos CSS usados pelo Tailwind 4.

## Conteúdo e referências

A página mantém o conjunto de dados fornecido para o trabalho. Não há consulta automática a uma API nem atualização em tempo real dos indicadores.

Os limites regionais do mapa são associados à [documentação de malhas do IBGE](https://servicodados.ibge.gov.br/api/docs/malhas?versao=3). Essa referência não substitui a indicação da fonte e do período dos indicadores municipais, que devem acompanhar a documentação acadêmica.

Organizações e iniciativas vinculadas na página:

- [Mãos que Alimentam — ADRA](https://adra.org.br/projetos/maos-que-alimentam-pe/)
- [SERTA](https://serta.org.br/)
- [Centro Sabiá](https://centrosabia.org.br/)
- [GoodTruck](https://goodtruck.org.br/)
- [Cozinha Solidária](https://cozinhasolidaria.com/)

Os links de apoio levam aos sites das iniciativas. O Mapa Solidário não processa pagamentos nem recebe doações diretamente.

## Verificação desta revisão

- Compilação concluída com Tailwind CSS 4.3.5 e DaisyUI 5.7.50.
- Comparação automática confirmou a preservação dos textos, dados, destinos dos links, IDs e caminhos SVG.
- Estrutura de abertura e fechamento das tags verificada; corrigido um contêiner aberto na seção do mapa.
- Nenhum JavaScript adicionado à página.

A revisão visual em diferentes larguras não foi concluída no ambiente de edição. Antes da entrega, confira o site em celular, tablet e desktop, incluindo o menu, todas as regiões do mapa, a tabela expandida e o rodapé.

## Autoria e créditos

**David Sulbaran e Ruan Both**  
Ciência da Computação — UFFS, Campus Chapecó  
Introdução ao Desenvolvimento Web — 2026

As imagens, fontes e demais materiais de terceiros permanecem sujeitos aos direitos de seus respectivos titulares. Este README não atribui uma licença de código aberto ao projeto.
