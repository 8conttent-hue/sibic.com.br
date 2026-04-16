# CLAUDE.md — SIBIC

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** SIBIC
**Nicho:** Educação
**Keywords:** Nossa historia foi construida com uma trajetoria de muito trabalho ao longo
**Paleta de cores:** sunset | **Fonte:** playfair

Nossa história foi construída com uma trajetória de muito trabalho ao longo de mais de 10 anos. Muito bem vindo ao nosso site. Usamos este espaço para falar sobre o nosso conhecimento, experiências paixão ao meio ambiente. Sinta-se em casa! Somos o meio facilitador pelo qual empresas e pessoas buscam informações para um planeta terra melhor. O Sibic já existe há 2 anos e nós acreditamos que a preservação do meio ambiente é um benefício para quem é daqui e para nós só existe uma forma de trabalhar: fazendo o certo. Nós falamos com pessoas de todos os níveis de conhecimento dentro do assunto. Mesmo você sendo iniciante na arte te cuidar do nosso lindo planta, nós temos um espaço reservado para você. Aqui você só encontrará os melhores conteúdos gratuitos sobre meio ambiente. Para acompanhar tudo basta se inscrever na newsletter.



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-B |
| Hero | Hero-D |
| Features | Features-J |
| About Section | About-H |
| Posts | Posts-J |
| Footer | Footer-E |
| Página Sobre | Sobre-F |
| Página Contato | Contato-G |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
