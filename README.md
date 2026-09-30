<div align="center">

<img src=".github/readme/banner.svg" alt="The Odin Library — estante de livros no navegador" width="100%">

**Estante de livros do The Odin Project: cadastre título e autor num modal, marque como lido ou não lido e remova com um clique.**

[![Demo](https://img.shields.io/badge/demo-ao%20vivo-ccad7a?style=for-the-badge&logo=githubpages&logoColor=white)](https://kessleru.github.io/TheOdin-Library/)
[![GitHub Pages](https://img.shields.io/github/deployments/kessleru/TheOdin-Library/github-pages?style=for-the-badge&label=pages)](https://github.com/kessleru/TheOdin-Library/actions/workflows/pages/pages-build-deployment)
[![Último commit](https://img.shields.io/github/last-commit/kessleru/TheOdin-Library?style=for-the-badge&color=8b7d6b)](https://github.com/kessleru/TheOdin-Library/commits/main)

<img src=".github/readme/desktop.png" alt="Lista 'My Books' com quatro livros, cada um com capa, título, autor, status Read/Unread e botão de excluir" width="100%">

</div>

## Sobre

O projeto [Library](https://www.theodinproject.com/lessons/node-path-javascript-library) do
currículo de JavaScript do [The Odin Project](https://www.theodinproject.com). O objetivo é praticar
**manipulação do DOM** e **organização com classes**: cada livro é uma instância de `Book`, guardada
num array `myLibrary`, e cada item da lista é montado com `createElement` e `appendChild`.

Os livros vivem só em memória — ao recarregar a página, a estante volta vazia.

## Telas

### Adicionando um livro

O botão **Add Book** abre um modal com título, autor e a caixa "I have read this book". O modal
fecha pelo botão, ao enviar o formulário ou com um clique fora dele.

<img src=".github/readme/modal.png" alt="Modal 'Add New Book' aberto sobre a lista, com os campos preenchidos" width="100%">

### Celular

<table>
<tr>
<td width="50%"><img src=".github/readme/mobile.png" alt="Lista de livros no celular, em cards" width="100%"></td>
<td width="50%">

Abaixo de 715px o cabeçalho da tabela some e cada livro vira um card, com os rótulos
**Title** e **Author** junto dos valores e as ações numa linha própria.

</td>
</tr>
</table>

## Funcionalidades

| | |
|---|---|
| ➕ **Adicionar** | Modal com título, autor e status de leitura |
| 🔁 **Lido / não lido** | Clique no status alterna entre **Read** e **Unread** chamando `book.toggleRead()` |
| ❌ **Remover** | Tira o livro do array e o item do DOM |
| 🪟 **Modal** | Fecha pelo botão, ao salvar ou com clique fora do conteúdo |
| 📱 **Responsivo** | Tabela no desktop, cards abaixo de 715px |

## Stack

| Camada | Ferramenta |
|---|---|
| Marcação | HTML5 |
| Estilo | CSS3, fontes [IBM Plex Sans e Fira Mono](https://fonts.google.com) |
| Lógica | JavaScript — classes, eventos e DOM |
| Deploy | [GitHub Pages](https://pages.github.com) |

## Rodando localmente

```bash
git clone https://github.com/kessleru/TheOdin-Library.git
cd TheOdin-Library
python -m http.server 8000
```

Abra `http://localhost:8000`. Não há dependências nem build — abrir o `index.html` direto no
navegador também funciona.

## Estrutura

```
├── index.html     # cabeçalho, lista #books e o modal com o formulário #add
├── script.js      # classe Book, myLibrary e renderização dos itens
├── css/
│   └── style.css
└── img/           # logo, capa genérica e ícones
```

<details>
<summary><b>Regerando as imagens deste README</b></summary>

```bash
node .github/readme/gerar.mjs                 # banner.svg

python -m http.server 8000                    # em outro terminal
npm i --no-save puppeteer-core sharp
node .github/readme/capturar.mjs              # cadastra livros pelo formulário e captura em 2x
```

</details>

---

<div align="center">
<sub>Feito por <a href="https://github.com/kessleru">Otávio Kessler Ustra</a> · projeto do <a href="https://www.theodinproject.com">The Odin Project</a></sub>
</div>
