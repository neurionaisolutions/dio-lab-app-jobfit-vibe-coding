# 📲✨📑JobFit — App Gerador de Currículos ATS Friendly com Lovable
PRD (Documento de Requisitos do Produto) Refinado no ChatGPT Web:
```TXT
# PROMPT ÚNICO — JOBFIT — APP DE MATCHMAKING DE VAGAS + CURRÍCULO ATS

Crie **do zero, exclusivamente no Lovable**, uma aplicação web SaaS chamada **JobFit** para **matchmaking entre candidatos e vagas de emprego**, com geração e personalização de **currículos ATS-friendly específicos para cada vaga**.

**IMPORTANTE:** Ignore completamente qualquer projeto, exemplo, arquitetura, interface, banco de dados ou lógica anteriormente criada envolvendo **Match, Ghost ou qualquer exemplo semelhante**. Este projeto deve ser construído como uma aplicação **100% nova**, sem reaproveitar conceitos de projetos anteriores.

O nome oficial do produto é:

# **JobFit**

Posicionamento da marca:

> **Encontre a vaga certa. Mostre o seu melhor.**

Proposta de valor:

> **IA que conecta seu perfil às melhores oportunidades e adapta seu currículo para cada vaga, aumentando sua compatibilidade com sistemas ATS.**

Nesta primeira versão, quero um **MVP funcional sem sistema de login ou cadastro**.

O usuário deve **entrar diretamente na aplicação e começar a utilizar o produto**, sem autenticação, e sem telas de login, cadastro, recuperação de senha ou criação de conta.

A autenticação, persistência individual de usuários e demais recursos relacionados a contas poderão ser adicionados posteriormente.

O produto deve ter aparência de um **SaaS profissional, moderno, confiável e preparado para evolução**, com foco em empregabilidade, inteligência artificial e experiência do usuário.

---

# 1. CONCEITO DO PRODUTO

O **JobFit** deve permitir que o usuário:

1. Entre diretamente na aplicação.
2. Monte seu perfil profissional.
3. Cadastre ou importe seu currículo.
4. Informe suas experiências, competências, formação e preferências profissionais.
5. Encontre vagas compatíveis com seu perfil.
6. Veja um **Match Score** entre seu perfil e cada vaga.
7. Entenda exatamente por que possui aquela pontuação.
8. Identifique competências que possui e competências que faltam.
9. Gere uma versão personalizada do currículo para determinada vaga.
10. Otimize o currículo para sistemas ATS.
11. Visualize o currículo antes de exportá-lo.
12. Exporte o currículo em **PDF**.
13. Salve diferentes versões do currículo durante a sessão.
14. Acompanhe as vagas de interesse e o status das candidaturas durante a sessão.

O aplicativo deve transmitir a ideia de:

> **"Encontre vagas que combinam com você e adapte seu currículo para aumentar suas chances de passar pelo ATS."**

---

# 2. PRINCÍPIOS FUNDAMENTAIS

Construa o produto seguindo estas regras:

* Aplicação **100% construída dentro do Lovable**.
* Nesta primeira versão, **NÃO implementar login**.
* **NÃO implementar cadastro de usuários**.
* **NÃO implementar recuperação de senha**.
* **NÃO criar tela de autenticação**.
* O usuário deve entrar diretamente no aplicativo.
* Interface responsiva para desktop, tablet e mobile.
* UX simples para usuários que não possuem conhecimento técnico.
* Design SaaS premium.
* Arquitetura organizada e escalável.
* Componentes reutilizáveis.
* Código limpo e modular.
* Estados de loading, vazio, erro e sucesso em todas as funcionalidades importantes.
* Feedback visual para todas as ações.
* Não criar funcionalidades falsas ou botões sem comportamento.
* Quando uma integração ainda não estiver configurada, criar uma estrutura preparada para integração futura e deixar isso claramente identificado.
* Priorizar acessibilidade.
* Utilizar textos em **português do Brasil**.

---

# 3. DESIGN SYSTEM

Utilize **shadcn/ui como design system principal**.

Não crie um design system visual paralelo.

Utilize os componentes do shadcn/ui sempre que apropriado, incluindo:

* Button
* Input
* Textarea
* Select
* Checkbox
* Radio Group
* Switch
* Dialog
* Drawer
* Sheet
* Card
* Badge
* Avatar
* Dropdown Menu
* Tabs
* Accordion
* Tooltip
* Alert
* Alert Dialog
* Toast/Sonner
* Progress
* Skeleton
* Table
* Pagination
* Breadcrumb
* Calendar
* Command
* Form
* Separator
* Scroll Area

Crie componentes próprios somente quando realmente necessário, mantendo o padrão visual do shadcn/ui.

---

# 4. IDENTIDADE VISUAL DO JOBFIT

A identidade visual do **JobFit** deve utilizar exclusivamente uma paleta baseada em:

### Branco

Para:

* fundos principais;
* cards;
* áreas de conteúdo;
* formulários;
* espaços de leitura.

### Azul-marinho

Para:

* títulos;
* textos principais;
* navegação;
* elementos de maior destaque;
* identidade da marca;
* logo/nome JobFit.

### Azul-claro

Para:

* botões secundários;
* indicadores;
* destaques;
* gráficos;
* badges;
* estados informativos;
* elementos relacionados à inteligência artificial;
* Match Score;
* elementos de destaque do produto.

A interface deve ser:

* limpa;
* elegante;
* tecnológica;
* profissional;
* minimalista;
* confiável;
* moderna.

Evite aparência excessivamente futurista, neon, gamer ou infantil.

Não utilizar gradientes exagerados.

Não utilizar excesso de sombras.

Priorize:

**White Space + Typography + Cards + Azul-marinho + Azul-claro.**

---

# 5. BRANDING DO JOBFIT

Utilizar **JobFit** como nome principal em toda a aplicação.

Não utilizar nomes genéricos como:

* App;
* Plataforma;
* Dashboard;
* Career App.

Sempre que fizer sentido, utilizar a marca:

**JobFit**

Criar uma identidade textual simples e profissional.

Sugestão de assinatura:

> **JobFit — Encontre a vaga certa. Mostre o seu melhor.**

A marca deve transmitir:

* tecnologia;
* inteligência;
* carreira;
* precisão;
* compatibilidade;
* confiança;
* profissionalismo.

---

# 6. ESTRUTURA PRINCIPAL

Nesta primeira versão, a aplicação deve abrir **diretamente no produto**.

Não criar fluxo:

Login → Cadastro → Dashboard.

Criar fluxo:

**Entrada direta → Perfil → Vagas → Match → Currículo ATS → PDF**

A aplicação deve possuir:

## Área principal

### Dashboard

### Meu Perfil

### Encontrar Vagas

### Vagas Salvas

### Candidaturas

### Meus Currículos

### Configurações

Como não existe login nesta versão, os dados podem permanecer em estado local/browser durante o MVP, mas a arquitetura deve ser organizada de forma que posteriormente seja possível conectar autenticação e banco de dados sem precisar reconstruir toda a aplicação.

---

# 7. DASHBOARD

Criar dashboard principal do **JobFit** com visão geral.

Ao entrar no aplicativo, o usuário deve visualizar:

### Saudação

> Olá! 👋

### Resumo

Cards:

* Vagas compatíveis;
* Match médio;
* Currículos criados;
* Candidaturas acompanhadas.

### Seção "Melhores oportunidades"

Exibir as vagas com maior Match Score.

Cada vaga deve mostrar:

* Cargo;
* Empresa;
* Localização;
* Modelo de trabalho;
* Senioridade;
* Match Score;
* Botão "Ver vaga";
* Botão "Criar currículo ATS".

### Seção "Seu perfil"

Mostrar percentual de completude:

> Perfil 85% completo

CTA:

> Completar perfil

### Seção "Últimas atividades"

Mostrar:

* currículo criado;
* vaga salva;
* candidatura atualizada;
* perfil atualizado.

---

# 8. ONBOARDING

Como não existe login, o primeiro acesso deve iniciar um onboarding simples.

Criar onboarding dividido em etapas.

### Etapa 1 — Informações pessoais

Campos:

* Nome;
* Sobrenome;
* E-mail;
* Telefone;
* Cidade;
* Estado;
* LinkedIn;
* GitHub;
* Portfólio/site.

### Etapa 2 — Objetivo profissional

Campos:

* Cargo desejado;
* Área profissional;
* Senioridade;
* Modelo de trabalho;
* Localização desejada;
* Pretensão salarial;
* Disponibilidade.

Modelo de trabalho:

* Presencial;
* Híbrido;
* Remoto.

### Etapa 3 — Experiência

Permitir adicionar múltiplas experiências:

* Cargo;
* Empresa;
* Localização;
* Data inicial;
* Data final;
* Cargo atual;
* Descrição;
* Principais responsabilidades;
* Principais resultados/conquistas.

### Etapa 4 — Formação

Permitir adicionar:

* Curso;
* Instituição;
* Grau;
* Data inicial;
* Data final;
* Status.

### Etapa 5 — Competências

Permitir adicionar:

* Hard Skills;
* Soft Skills;
* Idiomas;
* Certificações;
* Ferramentas;
* Tecnologias.

### Etapa 6 — Currículo

Permitir:

* preencher manualmente;
* importar currículo existente;
* revisar informações extraídas;
* editar informações antes de salvar.

Ao finalizar:

> **Seu perfil profissional está pronto para encontrar seu próximo JobFit.**

---

# 9. ÁREA DE VAGAS

Criar página:

**Vagas**

Com mecanismo de busca e filtros.

Filtros:

* Cargo;
* Palavra-chave;
* Localização;
* Remoto;
* Híbrido;
* Presencial;
* Senioridade;
* Faixa salarial;
* Área;
* Data de publicação;
* Match mínimo.

Campo de busca:

> Ex.: Desenvolvedor React, Analista de Dados, Engenheiro de IA...

Cada vaga deve aparecer em um card profissional.

Informações:

* Cargo;
* Empresa;
* Localização;
* Modelo;
* Salário, quando disponível;
* Data de publicação;
* Tags;
* Match Score.

---

# 10. MATCHMAKING

Esta é uma das funcionalidades centrais do **JobFit**.

Para cada vaga, calcular um **Match Score de 0 a 100** comparando:

* competências;
* experiência;
* senioridade;
* formação;
* localização;
* modelo de trabalho;
* palavras-chave;
* requisitos da vaga;
* tecnologias;
* certificações;
* idiomas.

Exibir visualmente:

### Match Score

**87%**

Criar indicadores:

* Competências: 92%
* Experiência: 88%
* Formação: 100%
* Senioridade: 90%
* Localização: 100%
* Palavras-chave: 78%

---

# 11. EXPLICAÇÃO DO MATCH

Não mostrar somente a porcentagem.

Criar uma seção:

## Por que esta vaga combina com você?

### Você atende

Mostrar competências/requisitos encontrados no perfil.

Exemplo:

* React
* TypeScript
* JavaScript
* Git
* APIs REST

### Você precisa desenvolver

Mostrar requisitos ausentes ou parcialmente atendidos.

Exemplo:

* AWS
* Docker
* Kubernetes

### Pontos fortes

Mostrar os principais fatores que aumentaram o Match Score.

### Pontos de atenção

Mostrar os fatores que reduziram o Match Score.

O usuário deve conseguir compreender claramente **como o score foi calculado**.

---

# 12. PÁGINA DETALHADA DA VAGA

Criar página completa da vaga.

Estrutura:

### Header

* Cargo;
* Empresa;
* Localização;
* Modelo;
* Match Score.

### Descrição

Exibir descrição completa.

### Requisitos

Separar:

**Obrigatórios**

**Desejáveis**

### Compatibilidade

Exibir análise detalhada do Match.

### Ações

Botões:

> Criar currículo para esta vaga

> Salvar vaga

> Marcar como candidatura

---

# 13. CURRÍCULO ATS

Criar uma área dedicada:

**Meu Currículo**

O usuário deve poder criar diferentes versões do currículo.

Exemplo:

* Currículo Base;
* Desenvolvedor Front-end — Empresa X;
* Analista de Dados — Empresa Y;
* Engenheiro de IA — Empresa Z.

---

# 14. GERADOR DE CURRÍCULO PERSONALIZADO

Quando o usuário clicar:

> Criar currículo ATS

O sistema deve utilizar:

1. Perfil profissional;
2. Currículo base;
3. Experiências;
4. Competências;
5. Formação;
6. Informações da vaga;
7. Requisitos da vaga;
8. Palavras-chave relevantes.

Gerar uma versão personalizada do currículo.

### IMPORTANTE

A IA **não deve inventar experiências, empresas, cargos, formação, certificações ou competências que o usuário não possui**.

A IA pode:

* reorganizar informações;
* melhorar redação;
* destacar experiências relevantes;
* adaptar palavras-chave verdadeiras;
* melhorar descrições;
* transformar responsabilidades em realizações quando houver informação suficiente;
* adequar o currículo aos requisitos da vaga.

Nunca criar informação profissional falsa.

---

# 15. OTIMIZAÇÃO ATS

Criar um painel:

## Análise ATS

Mostrar:

### ATS Score

Exemplo:

**91/100**

Dividir a análise em:

* Palavras-chave;
* Estrutura;
* Clareza;
* Experiência;
* Competências;
* Formação;
* Legibilidade;
* Compatibilidade com a vaga.

Mostrar recomendações práticas.

Exemplo:

> Adicione "TypeScript" à seção de competências. Essa tecnologia aparece nos requisitos da vaga e está presente no seu perfil.

---

# 16. PALAVRAS-CHAVE

Criar análise visual:

### Palavras-chave encontradas

Mostrar badges.

### Palavras-chave importantes ausentes

Mostrar badges.

### Palavras-chave já utilizadas

Mostrar onde aparecem no currículo.

Não realizar keyword stuffing.

A otimização deve priorizar naturalidade e veracidade.

---

# 17. EDITOR DE CURRÍCULO

Criar editor visual dividido em duas áreas:

### Esquerda

Campos editáveis:

* Informações pessoais;
* Resumo profissional;
* Experiência;
* Formação;
* Competências;
* Certificações;
* Idiomas.

### Direita

Preview do currículo em tempo real.

Permitir:

* editar;
* reorganizar seções;
* ocultar seções;
* alterar conteúdo;
* salvar versão.

O editor deve possuir autosave durante a sessão.

---

# 18. CURRÍCULO ATS-FRIENDLY

O template padrão deve priorizar compatibilidade com ATS.

Regras:

* Layout simples;
* Uma coluna;
* Hierarquia clara;
* Títulos de seção tradicionais;
* Texto selecionável;
* Sem elementos essenciais em imagens;
* Sem excesso de elementos gráficos;
* Sem tabelas desnecessárias;
* Sem barras de habilidade;
* Sem informações importantes dentro de ícones;
* Tipografia profissional;
* Estrutura semântica clara.

Criar opções de templates simples, profissionais e ATS-friendly.

---

# 19. EXPORTAÇÃO DO CURRÍCULO EM PDF

Adicionar uma funcionalidade completa de **exportação do currículo em PDF**.

O usuário deve possuir um botão claramente identificado:

> **Exportar PDF**

Ao clicar, o sistema deve:

1. Validar se o currículo possui informações suficientes.
2. Mostrar o preview final.
3. Gerar um PDF profissional.
4. Preservar o layout ATS-friendly.
5. Manter texto selecionável no PDF.
6. Não transformar o currículo inteiro em uma imagem.
7. Utilizar uma estrutura de uma coluna.
8. Manter títulos e seções claramente identificáveis.
9. Utilizar margens profissionais.
10. Garantir boa leitura em impressão e tela.
11. Gerar o arquivo com nome profissional.

Formato sugerido:

`Curriculo_Nome_Sobrenome_Vaga.pdf`

Exemplo:

`Curriculo_Joao_Silva_Desenvolvedor_Frontend.pdf`

O PDF deve representar fielmente o preview apresentado no editor.

Após a geração, apresentar feedback:

> **Seu currículo foi exportado com sucesso!**

Adicionar opção:

> Baixar PDF

### IMPORTANTE

A exportação deve ser implementada de forma realmente funcional no MVP.

Não criar apenas um botão visual.

O PDF precisa ser efetivamente gerado pelo aplicativo.

---

# 20. MEUS CURRÍCULOS

Criar biblioteca de currículos.

Cada card deve apresentar:

* Nome;
* Vaga relacionada;
* Empresa;
* ATS Score;
* Data de atualização;
* Status.

Ações:

* Abrir;
* Editar;
* Duplicar;
* Renomear;
* Excluir;
* Exportar PDF.

---

# 21. VAGAS SALVAS

Criar página:

**Vagas Salvas**

Permitir organizar oportunidades.

Status:

* Salva;
* Quero me candidatar;
* Candidatura enviada;
* Entrevista;
* Processo encerrado;
* Oferta;
* Recusado.

Criar filtros por status.

---

# 22. ACOMPANHAMENTO DE CANDIDATURAS

Criar uma área simples de pipeline.

Visualização estilo Kanban:

**Salvas → Candidatura enviada → Entrevista → Oferta → Encerrada**

Permitir mover vagas entre etapas.

Cada candidatura deve guardar:

* Vaga;
* Empresa;
* Data;
* Currículo utilizado;
* Observações;
* Status.

Como não existe login nesta primeira versão, armazenar essas informações durante a sessão/localmente.

---

# 23. PERFIL PROFISSIONAL

Criar página:

**Meu Perfil**

Permitir editar:

* Dados pessoais;
* Objetivos;
* Experiência;
* Formação;
* Competências;
* Certificações;
* Idiomas;
* Links profissionais;
* Preferências de trabalho.

Mostrar:

**Completude do perfil**

com barra de progresso.

---

# 24. IA

A inteligência artificial deve ser utilizada principalmente para:

### Matchmaking

Comparar perfil e vaga.

### Análise de vaga

Extrair:

* requisitos;
* competências;
* senioridade;
* palavras-chave;
* responsabilidades;
* diferenciais.

### Currículo

Adaptar o currículo à vaga.

### ATS

Avaliar compatibilidade.

### Recomendações

Sugerir melhorias.

Criar uma arquitetura preparada para integração com modelo de IA através de API.

**Não expor API keys no frontend.**

Nunca colocar chaves secretas diretamente no código cliente.

---

# 25. BANCO DE DADOS / ESTRUTURA DE DADOS

Nesta primeira versão, o aplicativo **não precisa de autenticação**.

Organizar a camada de dados de maneira que futuramente possa ser conectada a um banco de dados persistente.

Estruturar as entidades pensando em:

### profiles

* id
* name
* email
* phone
* location
* professional_title
* summary
* desired_role
* seniority
* work_model
* salary_expectation
* linkedin
* github
* portfolio

### experiences

* id
* profile_id
* company
* role
* location
* start_date
* end_date
* current
* description
* achievements

### education

* id
* profile_id
* institution
* course
* degree
* start_date
* end_date
* status

### skills

* id
* profile_id
* name
* category
* proficiency

### certifications

* id
* profile_id
* name
* issuer
* date

### languages

* id
* profile_id
* language
* proficiency

### jobs

* id
* title
* company
* location
* work_model
* seniority
* salary
* description
* requirements
* desirable_requirements
* published_at
* source

### job_matches

* id
* profile_id
* job_id
* score
* skills_score
* experience_score
* education_score
* seniority_score
* location_score
* keywords_score
* analysis

### resumes

* id
* profile_id
* job_id
* name
* content
* ats_score
* version
* created_at
* updated_at

### saved_jobs

* id
* profile_id
* job_id
* status
* notes
* created_at

### applications

* id
* profile_id
* job_id
* resume_id
* status
* applied_at
* notes

---

# 26. PERSISTÊNCIA DO MVP

Como não haverá login nesta versão:

Utilizar uma solução de armazenamento local adequada ao ambiente da aplicação para manter os dados do usuário durante a utilização.

Preferencialmente:

* localStorage para dados simples;
* estado global quando necessário;
* IndexedDB caso seja necessário armazenar dados maiores, como currículos importados.

A arquitetura deve ser preparada para futuramente substituir o armazenamento local por banco de dados com autenticação.

**Não criar dependência estrutural que impeça essa migração futura.**

---

# 27. IMPORTAÇÃO DE CURRÍCULO

Permitir que o usuário importe um currículo existente.

Formatos prioritários:

* PDF;
* DOCX.

Após importação:

1. Ler o conteúdo;
2. Extrair informações;
3. Identificar:

   * nome;
   * contato;
   * resumo;
   * experiências;
   * formação;
   * competências;
   * certificações;
   * idiomas;
4. Mostrar os dados extraídos;
5. Permitir correção manual;
6. Salvar no perfil.

Nunca assumir que uma informação extraída automaticamente está correta.

O usuário deve conseguir revisar tudo antes de utilizar os dados.

---

# 28. SEGURANÇA

Mesmo sem login, implementar:

* validação de formulários;
* sanitização de entradas;
* tratamento de erros;
* proteção contra entradas malformadas;
* cuidado com dados pessoais;
* nenhuma API key no frontend;
* nenhuma informação secreta no código público.

---

# 29. NAVEGAÇÃO

Criar sidebar no dashboard com:

* Dashboard
* Encontrar Vagas
* Vagas Salvas
* Candidaturas
* Meus Currículos
* Meu Perfil
* Configurações

No mobile, transformar a navegação em menu responsivo.

Não incluir:

* Login;
* Cadastro;
* Logout;
* Conta de usuário.

Esses recursos serão implementados posteriormente.

---

# 30. CONFIGURAÇÕES

Criar:

### Preferências profissionais

* Localização;
* Modelo de trabalho;
* Cargos;
* Senioridade.

### Preferências de currículo

* Template padrão;
* Preferência de exportação.

### Preferências de IA

* Ativar/desativar recomendações de IA quando aplicável.

---

# 31. EXPERIÊNCIA DE USUÁRIO

Toda ação importante deve apresentar feedback.

Exemplos:

Ao salvar:

> Vaga salva com sucesso.

Ao gerar currículo:

> Seu currículo personalizado está sendo preparado.

Durante análise de IA:

> Analisando os requisitos da vaga...

Durante geração do PDF:

> Preparando seu currículo em PDF...

Após exportação:

> Seu currículo foi exportado com sucesso!

Usar:

* Skeleton;
* Progress;
* Toast;
* Empty States;
* Error States.

Não deixar telas vazias sem explicação.

---

# 32. EMPTY STATES

Criar estados vazios profissionais.

### Nenhuma vaga salva

> Você ainda não salvou nenhuma vaga.

CTA:

> Encontrar vagas

### Nenhum currículo

> Crie seu primeiro currículo personalizado para começar.

CTA:

> Criar currículo

### Nenhuma candidatura

> Suas candidaturas aparecerão aqui quando você começar a acompanhar oportunidades.

---

# 33. RESPONSIVIDADE

A aplicação deve funcionar perfeitamente em:

* Desktop;
* Notebook;
* Tablet;
* Smartphone.

No mobile:

* sidebar vira menu;
* cards se adaptam;
* tabelas tornam-se responsivas;
* editor de currículo se reorganiza;
* preview do currículo continua acessível;
* botão de exportação PDF permanece facilmente acessível.

---

# 34. MICROINTERAÇÕES

Utilizar animações discretas.

Exemplos:

* hover;
* transições;
* loading;
* progress;
* expansão de cards;
* atualização do Match Score.

Evitar animações exageradas.

A experiência deve parecer premium e rápida.

---

# 35. DASHBOARD VISUAL

Criar gráficos simples e úteis:

* Match médio;
* Vagas compatíveis;
* Evolução das candidaturas;
* Currículos criados.

Não exagerar na quantidade de gráficos.

---

# 36. COMPONENTE DE MATCH SCORE

Criar um componente reutilizável chamado:

`MatchScore`

Deve aceitar:

* score;
* tamanho;
* variante;
* detalhes.

Exibir de forma visualmente clara.

Faixas:

* 0–49: baixa compatibilidade;
* 50–69: compatibilidade moderada;
* 70–84: boa compatibilidade;
* 85–100: excelente compatibilidade.

---

# 37. COMPONENTE ATS SCORE

Criar componente reutilizável:

`ATSScore`

Exibir:

* pontuação;
* status;
* recomendações.

Exemplo:

**91/100 — Excelente**

---

# 38. COMPONENTE JOB CARD

Criar:

`JobCard`

Com:

* cargo;
* empresa;
* localização;
* modelo;
* tags;
* Match Score;
* data;
* ações.

O componente deve ser reutilizável em diferentes páginas.

---

# 39. COMPONENTE RESUME CARD

Criar:

`ResumeCard`

Com:

* nome;
* vaga;
* ATS Score;
* última atualização;
* ações.

Incluir ação específica:

> Exportar PDF

---

# 40. COMPONENTE PROFILE COMPLETENESS

Criar:

`ProfileCompleteness`

Mostrar:

> Seu perfil está 82% completo.

Listar o que falta.

---

# 41. PRINCÍPIOS DE COPY

Utilizar português brasileiro profissional.

Evitar textos genéricos como:

* "Lorem ipsum";
* "Teste";
* "Clique aqui";
* "Exemplo".

Os textos devem parecer de um produto SaaS real.

CTAs devem ser claros:

* Encontrar vagas;
* Ver compatibilidade;
* Criar currículo;
* Otimizar currículo;
* Salvar vaga;
* Acompanhar candidatura;
* Completar perfil;
* Exportar PDF.

---

# 42. EXPERIÊNCIA DE PRIMEIRO ACESSO

Como não haverá login, o usuário deve entrar diretamente na aplicação.

Fluxo:

1. Abrir aplicação;
2. Welcome/Onboarding;
3. Perfil profissional;
4. Currículo;
5. Primeira análise;
6. Dashboard.

Criar uma jornada simples:

**Perfil → Vagas → Match → Currículo ATS → PDF → Candidatura**

---

# 43. ARQUITETURA VISUAL

A estrutura visual deve seguir:

### Entrada direta

↓

### Dashboard

↓

### Encontrar Vagas

↓

### Detalhes da Vaga

↓

### Match Score

↓

### Criar Currículo ATS

↓

### Editor

↓

### ATS Score

↓

### Preview

↓

### Exportar PDF

↓

### Acompanhar candidatura

---

# 44. QUALIDADE

Antes de considerar o projeto concluído, revise:

* Todos os links;
* Todos os botões;
* Formulários;
* Responsividade;
* Estados de loading;
* Estados vazios;
* Estados de erro;
* Persistência local;
* Navegação;
* Componentes;
* Consistência visual;
* Tipografia;
* Espaçamento;
* Acessibilidade;
* Geração do PDF;
* Qualidade visual do PDF;
* Texto selecionável no PDF;
* Nome correto do arquivo PDF.

Não deixar funcionalidades importantes apenas como elementos visuais.

---

# 45. REGRA IMPORTANTE SOBRE DADOS E IA

Não inventar dados profissionais.

Nunca atribuir ao usuário:

* experiência inexistente;
* formação inexistente;
* certificação inexistente;
* empresa inexistente;
* tecnologia que ele não declarou dominar;
* resultados profissionais não informados.

Quando uma informação não existir, solicitar ao usuário ou indicar que ela está ausente.

A IA deve **otimizar a apresentação da experiência real**, e não fabricar uma experiência profissional.

---

# 46. RESULTADO FINAL ESPERADO

Entregar uma aplicação SaaS chamada **JobFit**, funcional, profissional e escalável, que permita ao usuário percorrer toda esta jornada **sem precisar criar uma conta**:

**Entrar diretamente no aplicativo**

→ **Montar perfil profissional**

→ **Encontrar vagas**

→ **Calcular Match Score**

→ **Entender a compatibilidade**

→ **Selecionar uma vaga**

→ **Gerar currículo personalizado**

→ **Otimizar para ATS**

→ **Editar currículo**

→ **Visualizar currículo**

→ **Analisar ATS Score**

→ **Exportar currículo em PDF**

→ **Salvar vaga**

→ **Registrar candidatura**

→ **Acompanhar processo seletivo**

---

# 47. REGRA FINAL DE IMPLEMENTAÇÃO

Construa primeiro uma **base sólida e funcional**, não apenas uma interface bonita.

Prioridades:

1. UX;
2. Arquitetura;
3. Estrutura de dados;
4. Entrada direta sem autenticação;
5. Perfil profissional;
6. Vagas;
7. Matchmaking;
8. Currículo ATS;
9. IA;
10. Editor de currículo;
11. ATS Score;
12. Exportação funcional para PDF;
13. Vagas salvas;
14. Candidaturas;
15. Polimento visual.

Use **shadcn/ui como base do design system** e mantenha toda a identidade visual em **branco, azul-marinho e azul-claro**.

O resultado deve parecer um **produto SaaS profissional pronto para validação comercial**, e não um protótipo genérico.

**Nome oficial do produto: JobFit.**

**Slogan: "Encontre a vaga certa. Mostre o seu melhor."**

**Não implemente login, cadastro ou autenticação nesta versão.**

**O usuário deve conseguir abrir a aplicação e começar a utilizar o produto imediatamente.**

**A exportação para PDF deve funcionar de verdade e gerar um currículo profissional, ATS-friendly, com texto selecionável e layout fiel ao preview.**

Comece criando a estrutura completa da aplicação e implemente as funcionalidades de forma incremental, garantindo que cada etapa esteja funcional antes de avançar para a próxima.

```
# Interações com o Lovable
>PROMPT ÚNICO — JOBFIT — APP DE MATCHMAKING DE VAGAS + CURRÍCULO ATS: 

>Crie do zero, exclusivamente no Lovable, uma aplicação web SaaS chamada JobFit para matchmaking entre candidatos e vagas de emprego, com geração e personalização de currículos ATS-friendly específicos para cada vaga.
IMPORTANTE: Ignore completamente qualquer projeto, exemplo, arquitetura, interface, banco de dados ou lógica anteriormente criada envolvendo Match, Ghost ou qualquer exemplo semelhante. Este projeto deve ser construído como uma aplicação 100% nova, sem reaproveitar conceitos de projetos anteriores.
O nome oficial do produto é: `JobFit`

>Remover o emoji 👋 dos títulos do Dashboard para evitar caracteres sem glifo no ambiente de teste.

>Auditar o app para remover ou substituir todos os emojis e caracteres que possam não ter glifo no ambiente de teste.

>Rodar um scan de vulnerabilidades nas dependências para confirmar que a CVE-2026-59870 não aparece mais.

>Estamos lidando com dados sensíveis, precisamos adotar medidas  de segurança que estejam de acordo com as leis do LGPD, qual sua sugestão para ajustar essa última fase?

# JobFit — Resumo das Funcionalidades

Este documento descreve, em alto nível, as funcionalidades do JobFit e serve como referência rápida para desenvolvedores e designers.

1. Onboarding e Perfil
   - Onboarding em etapas (informações pessoais, objetivo profissional, experiência, formação, competências, currículo).
   - Perfil profissional completo com campos de contato, redes, preferências e completude.

2. Busca de Vagas e Filtros
   - Página de Vagas com busca por palavra-chave e filtros (cargo, local, modelo, senioridade, faixa salarial, área, data, match mínimo).
   - Cards profissionais com Match Score.

3. Matchmaking
   - Cálculo de Match Score (0-100) comparando competências, experiência, senioridade, formação, localização, modelo de trabalho, palavras-chave, requisitos, tecnologias, certificações e idiomas.
   - Indicadores por categoria (competências, experiência, formação, senioridade, localização, palavras-chave).

4. Explicação do Match
   - Seção "Por que esta vaga combina com você?" com: você atende, você precisa desenvolver, pontos fortes, pontos de atenção.

5. Página detalhada da vaga
   - Header (cargo, empresa, localização, modelo, Match Score), descrição, requisitos (obrigatórios/desejáveis), análise de compatibilidade e ações (criar currículo, salvar vaga, marcar candidatura).

6. Currículo ATS e Editor
   - Área "Meu Currículo" com versões (base e por vaga).
   - Editor visual com preview em tempo real, autosave e funcionalidades de reorganização.

7. Gerador de Currículo Personalizado (IA)
   - Geração de currículo usando perfil, currículo base, experiências e informações da vaga.
   - IA NÃO inventa informações — pode reorganizar, melhorar redação e adaptar palavras-chave verdadeiras.

8. Otimização ATS
   - Painel de Análise ATS (ATS Score, palavras-chave, estrutura, clareza, experiência, competências, formação, legibilidade) com recomendações práticas.

9. Exportação em PDF
   - Exportar currículo em PDF preservando layout ATS-friendly e texto selecionável. Nome de arquivo profissional sugerido.

10. Meus Currículos (biblioteca)
   - Cards com nome, vaga relacionada, empresa, ATS Score, data de atualização, ações (abrir, editar, duplicar, renomear, excluir, exportar).

11. Requisitos de MVP e Arquitetura
   - MVP sem autenticação (persistência local/browser), arquitetura escalável e preparada para futuras integrações.
   - Uso do design system shadcn/ui.

---






