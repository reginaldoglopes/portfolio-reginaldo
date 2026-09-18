# Portfólio — Reginaldo Gonçalves Lopes

Site pessoal de portfólio, em produção em **https://portfolio-reginaldo-tau.vercel.app/**.

Apresenta a trajetória profissional, formação, ferramentas e projetos técnicos de Reginaldo Gonçalves Lopes — Auxiliar Administrativo na Diretoria de Finanças (DFIN) da SEDUC-PA, graduando em Ciências Contábeis, que também desenvolve sistemas web para automatizar processos do próprio dia a dia de trabalho.

## Stack

Site estático de arquivo único — sem build, sem framework, sem dependências de runtime.

- **HTML/CSS/JS** puro, tudo em [`index.html`](index.html)
- Fontes: [Newsreader](https://fonts.google.com/specimen/Newsreader) (serifada) e [IBM Plex Sans/Mono](https://fonts.google.com/specimen/IBM+Plex+Sans) via Google Fonts
- Imagens embutidas como `data:` URI (base64) — nenhum asset externo
- Hospedagem: [Vercel](https://vercel.com), deploy automático a cada push na branch `main`

## Estrutura do site

| Seção | Conteúdo |
|---|---|
| Sobre | Apresentação pessoal e trajetória resumida |
| Trajetória | Linha do tempo profissional (FADESP → SEDUC → DFIN) |
| Trabalhos | Cards de estudos de caso de projetos técnicos, com modal de detalhes ao clicar |
| Ferramentas | Sistemas e ferramentas usadas no dia a dia (SIAFE, SIMAS, Google Sheets, stack de desenvolvimento) |
| Formação | Graduação em Ciências Contábeis |
| Habilidades | Competências comportamentais e técnicas |
| Rotina | Rotina semanal |
| Contato | E-mail, WhatsApp, LinkedIn |

Ver [`docs/CASE-STUDIES.md`](docs/CASE-STUDIES.md) para detalhes sobre os projetos apresentados na seção Trabalhos e as decisões de sigilo de dados por trás de cada card.

## Rodando localmente

Não há passo de build. Basta abrir o arquivo direto no navegador:

```bash
# Windows
start index.html

# macOS
open index.html

# Linux
xdg-open index.html
```

Ou servir com qualquer servidor estático, por exemplo:

```bash
npx serve .
```

## Deploy

O projeto está conectado ao Vercel via GitHub — qualquer push para `main` gera um novo deploy em produção automaticamente. Ver [`docs/SECURITY.md`](docs/SECURITY.md) para os headers de segurança configurados em [`vercel.json`](vercel.json).

## Documentação

- [`docs/SECURITY.md`](docs/SECURITY.md) — headers de segurança e política de dados sensíveis
- [`docs/CASE-STUDIES.md`](docs/CASE-STUDIES.md) — detalhes dos projetos da seção Trabalhos
- [`CHANGELOG.md`](CHANGELOG.md) — histórico de mudanças

## Contato

- E-mail: rreginaldogoncalveslopes@gmail.com
- LinkedIn: [reginaldo-gonçalves-lopes](https://www.linkedin.com/in/reginaldo-gonçalves-lopes-923792350/)
