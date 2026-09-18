# Segurança

## Superfície de ataque

Este site é 100% estático: um único arquivo HTML, sem backend, sem formulário, sem coleta de dados, sem cookies, sem armazenamento local usado para dados sensíveis. Não há login, não há banco de dados, não há API própria. Isso reduz a superfície de ataque a praticamente zero — o único vetor realista é conteúdo malicioso injetado no próprio HTML publicado, o que é mitigado pelos headers abaixo.

## Headers de segurança

Configurados em [`vercel.json`](../vercel.json) e aplicados a todas as rotas:

| Header | Valor | Motivo |
|---|---|---|
| `Content-Security-Policy` | restringe `script-src`/`style-src`/`font-src`/`img-src` às origens necessárias (`self`, Google Fonts, inline apenas onde o próprio site usa) | Limita o impacto de qualquer injeção de conteúdo |
| `X-Frame-Options` | `DENY` | Evita que o site seja carregado dentro de um `<iframe>` de terceiros (clickjacking) |
| `X-Content-Type-Options` | `nosniff` | Evita que o navegador reinterprete o tipo de conteúdo servido |
| `Referrer-Policy` | `strict-origin-when-cross-origin` | Limita quanta informação de referrer vaza para outros sites |
| `Permissions-Policy` | desativa geolocalização, câmera e microfone | Nenhuma dessas APIs é usada; desativar reduz a superfície mesmo que um script de terceiro seja injetado no futuro |
| `Strict-Transport-Security` | aplicado automaticamente pela Vercel | Força HTTPS |

## JavaScript inline (modal de projetos)

A seção Trabalhos usa um pequeno script inline para abrir/fechar o modal de detalhes de cada projeto. Todo o conteúdo inserido dinamicamente usa `textContent`, nunca `innerHTML`, para evitar qualquer vetor de XSS — mesmo que os dados exibidos sejam todos estáticos (hardcoded no próprio arquivo, não vêm de input do usuário nem de API externa).

## Política de dados sensíveis nos estudos de caso

Alguns dos projetos apresentados na seção Trabalhos foram construídos para uso interno da Secretaria de Estado de Educação do Pará (SEDUC-PA) e originalmente manipulam dados orçamentários e de processos administrativos reais. Para esses casos, aplicamos as seguintes regras, sem exceção:

1. **Nenhum valor financeiro real é publicado.** Todo print/mockup exibido nos cards foi recriado com números fictícios, mantendo apenas a estrutura visual da interface real.
2. **Nenhum identificador real** (números de processo, nomes de fornecedores/credores reais, e-mails de administradores) é publicado — todos foram substituídos por exemplos genéricos.
3. **Projetos sem autenticação adequada, ou cujo código-fonte embute dados reais diretamente no arquivo, não recebem link público** (nem para a aplicação, nem para o repositório de código), independentemente de estarem "no ar" ou não. Ver [`docs/CASE-STUDIES.md`](CASE-STUDIES.md) para o status de cada projeto.

Essa política existe para proteger dados públicos/institucionais reais, não apenas para "ficar bonito" no portfólio — o critério de publicação é sempre a segurança do sistema de origem, não a vontade de mostrar mais detalhes.
