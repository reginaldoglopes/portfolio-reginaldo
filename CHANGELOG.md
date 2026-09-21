# Changelog

Formato baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/).

## [2026-09-21]

### Added
- Botões "Baixar currículo (PDF)" no topo (hero) e no rodapé apontando para `curriculo-reginaldo-goncalves-lopes.pdf`, em substituição ao fallback por e-mail.

### Changed
- Seção **Ferramentas** removida como tópico próprio: os 8 logos agora aparecem em uma linha, em círculos e sem textos, abaixo dos cards de Habilidades. Link "Ferramentas" removido do menu.

## [2026-09-18]

### Added
- Headers de segurança (`vercel.json`): CSP, X-Frame-Options, X-Content-Type-Options, Referrer-Policy, Permissions-Policy.
- Modal de detalhes por projeto na seção Trabalhos: cada card, ao ser clicado, abre uma descrição completa (problema, funcionamento, stack, segurança/status).
- Efeito de hover nos cards de Trabalhos (elevação + brilho na borda).

### Changed
- Paleta de destaque dos badges/hover/títulos de seção do dourado (`--brass`) para azul (`--forest`).
- Texto sobre religião no "Sobre mim" ("católico" → "cristão").
- Repositório GitHub tornado público — necessário para o deploy automático funcionar no plano gratuito do Vercel (ver seção "Infraestrutura" abaixo).

## [2026-09-17]

### Added
- Seção **Trabalhos**: 3 estudos de caso de projetos técnicos, cada um com uma recriação fiel da interface real usando dados fictícios (ver [`docs/CASE-STUDIES.md`](docs/CASE-STUDIES.md)).
- Seção **Ferramentas**: 8 cards de ferramentas usadas no dia a dia, com ícones reais para as marcas conhecidas.
- Botão de currículo no rodapé (fallback por e-mail até haver um PDF).

### Changed
- Renomeado `index_6.html` → `index.html`, necessário para servir a página na raiz do domínio.
- Texto do "Sobre mim" reescrito para explicar a ponte entre a formação em Ciências Contábeis e o desenvolvimento dos projetos técnicos.
- "CACS-FUNDEB" padronizado para "CACs Fundeb" em todas as ocorrências.
- Removido trecho de autocrítica sobre timidez/dicção na seção Habilidades.

### Fixed
- Link do LinkedIn (estava com placeholder `seu-perfil`) corrigido para o perfil real; nota de aviso removida.

## [2026-09-16]

### Added
- Versão inicial do site: Sobre, Trajetória, Formação, Habilidades, Rotina, Contato.

---

## Infraestrutura (fora do histórico de commits)

- **Deploy:** Vercel, conectado ao GitHub, deploy automático a cada push em `main`. URL de produção: https://portfolio-reginaldo-tau.vercel.app/
- **Bug de deploy resolvido em 2026-09-18:** os deploys pararam de atualizar automaticamente porque o autor dos commits (identidade Git configurada nesta máquina) não é colaborador do projeto na conta Vercel dona do repositório, e o plano gratuito do Vercel bloqueia deploys de autores sem acesso em repositórios privados. Resolvido tornando o repositório público.
