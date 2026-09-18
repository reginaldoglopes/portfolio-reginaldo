# Estudos de caso — seção Trabalhos

Detalhes de cada projeto apresentado na seção Trabalhos do portfólio, incluindo o motivo por trás de cada decisão de link/sigilo. Ver a política geral em [`docs/SECURITY.md`](SECURITY.md).

## 1. Sistema de Empenho SEDUC

**O que é:** ferramenta web para controlar o empenho da folha de pagamento do FUNDEB/SEDUC. Substitui a conferência manual entre o documento de empenho e o relatório da folha do SIAFEM, cruzando os dois automaticamente por grupo orçamentário e apontando divergências. Inclui tela de empenho por fonte de recurso, com teto controlado em tempo real.

**Stack:** Node.js, HTML/JS no frontend, SQLite em desenvolvimento e PostgreSQL em produção.

**Status de publicação:** `estudo de caso`, **sem link**.

**Por quê:** o sistema real está em produção com dados reais do FUNDEB e, hoje, sem autenticação — qualquer pessoa com o link consegue visualizar e alterar os dados. Divulgar esse link no portfólio aumentaria a exposição de um sistema que já precisa ser corrigido de qualquer forma. O card usa uma recriação da interface com valores fictícios, não o print real.

## 2. Level Up Contábil

**O que é:** plataforma web gamificada de preparação para o Exame de Suficiência do CFC. Organiza o estudo em trilhas por nível, com questões inéditas geradas por IA a partir de provas reais (com verificação anti-plágio e aprovação humana obrigatória antes de publicar qualquer questão), e um painel administrativo completo com acesso restrito (sem cadastro público).

**Stack:** Next.js 16, TypeScript, Tailwind CSS, Supabase (PostgreSQL), Google Gemini.

**Status de publicação:** `em produção`, **sem link** (por escolha do autor, não por questão de segurança — este projeto tem autenticação real e poderia ser linkado).

## 3. DFIN — Controle de Processos

**O que é:** dashboard de acompanhamento consolidado dos processos financeiros da Diretoria de Finanças (DFIN/SEDUC-PA), com visão geral por programa (PETE/PEAE), controle de descontingenciamento, execução financeira e um modo de gestão com cadastro, edição e log de auditoria das alterações.

**Stack:** HTML/CSS/JS, Chart.js, Google Identity Services.

**Status de publicação:** `estudo de caso`, **sem link e sem repositório**.

**Por quê:** a versão atual desse projeto mantém dados reais da DFIN embutidos diretamente no próprio arquivo da aplicação. Publicar o link ou o código-fonte exporia esses dados por completo. O card apresenta apenas a estrutura e as funcionalidades da ferramenta, com uma recriação da interface usando valores fictícios.

---

**Regra geral para novos projetos adicionados aqui:** antes de publicar link, repositório ou qualquer print, confirmar que (a) o sistema de origem tem autenticação real, (b) nenhum dado real (financeiro, pessoal, institucional) fica visível no card ou no código publicado, e (c) o autor está de acordo com a exposição pública daquele projeto.
