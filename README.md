# Blog do Mario Alencar — como publicar (GitHub Pages, grátis, sem login pra ler)

Esta pasta é um site estático pronto (HTML puro, sem build, sem framework). Pra colocar no ar,
grátis, com um link que qualquer pessoa acessa sem precisar de conta:

## Passo a passo

1. No GitHub (usuário `firmacon`), crie um repositório novo chamado **exatamente**:
   ```
   firmacon.github.io
   ```
   Esse nome é especial — o GitHub Pages publica ele direto na raiz de
   `https://firmacon.github.io/`, sem precisar configurar nada depois.

   (Se preferir manter isolado dos outros repositórios, pode criar com outro nome, tipo `blog` —
   aí o site fica em `https://firmacon.github.io/blog/` em vez da raiz. Funciona igual, só muda o link.)

2. Suba o **conteúdo desta pasta** (`blog_firmacon/`) pra raiz do repositório — ou seja, o
   `index.html` precisa ficar direto na raiz do repo, não dentro de uma subpasta.

   Do jeito que você já faz commit do Micro-Leitor-SPED em outra conversa, é o mesmo processo:
   ```bash
   cd caminho/para/blog_firmacon
   git init
   git remote add origin https://github.com/firmacon/firmacon.github.io.git
   git add .
   git commit -m "Primeiro post: anonimização de dados"
   git branch -M main
   git push -u origin main
   ```

3. Espere 1-2 minutos. O site fica no ar em `https://firmacon.github.io/` — sem login, sem
   paywall, sem limite de leitura pra quem acessa. Repositório público no plano gratuito não tem
   limite de visualizações.

## Estrutura

```
blog_firmacon/
├── index.html                          ← página inicial, lista os artigos
├── .nojekyll                           ← evita o GitHub tentar processar como site Jekyll
├── assets/
│   ├── style.css                       ← tema escuro único do blog
│   ├── capa1.png                       ← capa do artigo 1
│   ├── capa2_pt.png                    ← capa do artigo 2 (PT — "Quem é o culpado?")
│   └── capa2_en.png                    ← capa do artigo 2 (EN — "Who's guilty?")
└── posts/
    ├── anonimizando-dados-1-pt.html
    ├── anonymizing-data-1-en.html
    ├── ilusoes-anonimizacao-2-pt.html
    └── illusions-anonymization-2-en.html
```

## Pra publicar o próximo artigo

1. Copie um dos arquivos de `posts/` como modelo.
2. Troque título, subtítulo, texto e capa.
3. Adicione um novo `.post-card` em `index.html` apontando pro novo arquivo.
4. `git add . && git commit -m "Novo artigo" && git push`

Sem build, sem Jekyll, sem dependência — só HTML e CSS puro, editável em qualquer editor de texto.
