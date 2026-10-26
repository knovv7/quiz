# Ensino superior e desigualdades territoriais no interior da Amazônia paraense

Site do questionário de pesquisa com estudantes de graduação do Sul e Sudeste do Pará.
São 10 perguntas, uma por tela, com revisão antes de concluir.

O site é um único arquivo, `index.html`. Não precisa instalar nada nem rodar build.

## Testar no computador

Dê dois cliques em `index.html` para abrir no navegador.

## Onde ficam as respostas

As respostas ficam salvas **só no navegador do aparelho onde o questionário foi respondido**.
Elas não são enviadas para nenhum servidor.

- Para ver e exportar: clique em **Área do pesquisador**, no rodapé da tela inicial (ou abra o endereço do site com `#pesquisador` no final).
- Dá para baixar uma planilha CSV (abre no Excel, LibreOffice e Google Planilhas) ou copiar as respostas para colar numa planilha.
- A Área do pesquisador não tem senha.

Isso funciona para coleta presencial, com os estudantes respondendo no mesmo celular ou tablet.
Se cada estudante responder no próprio celular pelo link, as respostas ficam no celular dele e **não chegam até você**.
Para receber essas respostas, o site precisa ser ligado a um serviço que guarde os dados, como o Google Forms ou uma planilha do Google.

## Publicar no GitHub

### Pelo site do GitHub (sem usar o terminal)

1. Entre em <https://github.com/new>.
2. Em **Repository name**, escreva um nome, por exemplo `questionario-ensino-superior-para`.
3. Escolha **Public** ou **Private** (a Vercel funciona com os dois) e clique em **Create repository**.
4. Na página seguinte, clique em **uploading an existing file**.
5. Arraste os arquivos `index.html`, `README.md` e `.gitignore` desta pasta.
   No Windows, o `.gitignore` pode aparecer sem nome; se não conseguir arrastar, pode deixá-lo de fora.
6. Clique em **Commit changes**.

### Pelo terminal (com git)

Na primeira vez, configure seu nome e e-mail no git (aparecem no histórico público do GitHub):

```bash
git config --global user.name "Seu Nome"
```

```bash
git config --global user.email "seu-email@exemplo.com"
```

Crie o repositório vazio em <https://github.com/new> (sem README) e rode, dentro desta pasta:

```bash
git init -b main
```

```bash
git add .
```

```bash
git commit -m "Questionário de pesquisa"
```

```bash
git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git
```

```bash
git push -u origin main
```

## Publicar na Vercel

1. Entre em <https://vercel.com> com a sua conta do GitHub.
2. Clique em **Add New… → Project**.
3. Em **Import Git Repository**, escolha o repositório do questionário e clique em **Import**.
   Se ele não aparecer, clique em **Adjust GitHub App Permissions** e libere o acesso ao repositório.
4. Em **Framework Preset**, deixe **Other**. Não preencha Build Command nem Output Directory.
5. Clique em **Deploy**.

Em menos de um minuto a Vercel mostra o endereço do site, algo como `nome-do-repositorio.vercel.app`.
Cada vez que você alterar o `index.html` no GitHub, a Vercel publica a nova versão sozinha.

## Alterar as perguntas

As perguntas estão no `index.html`, na lista `PERGUNTAS` dentro do `<script>`.
Cada pergunta tem o texto, a seção, o tipo (`escolha`, `escala` ou `texto`), se é obrigatória e as opções.
