# Cronograma de Artefatos e Entregas Técnicas

## Informações Gerais

- **Projeto:** Ecossistema CMK (Campeonato Maverick de Kart)
- **Mentor:** Heitor (Maverick)
- **Desenvolvedor:** Matheus

## 1. Visão Geral da Documentação

Para cada etapa do desenvolvimento (MVP), serão exigidos documentos auxiliares que validam a arquitetura e a lógica do sistema. A aprovação desses artefatos é pré-requisito para o encerramento de cada ciclo.

## 2. Tabela de Entregáveis por Milestone

| Artefato | Descrição Técnica | MVP 1 (Dia 30) | MVP 2 (Dia 60) | MVP 3 (Dia 90) |
| -------- | ----------------- | -------------- | -------------- | -------------- |
| Diagrama de Classes (UML) | Representação das classes de domínio e seus atributos/métodos. | Essencial | Atualização | Final |
| DER (Modelo de Dados) | Diagrama Entidade-Relacionamento focado na estrutura das tabelas. | Essencial | Atualização | Final |
| Diagrama de Sequência | Fluxo de uma requisição: PageModel -> Service -> Repository. | - | Essencial | Opcional |
| Dicionário de Dados | Tabela em Markdown descrevendo tipos, nulos e funções de cada campo. | Sim | Sim | Sim |
| Mapa de Rotas (Sitemap) | Listagem de URLs da aplicação e verbos HTTP (GET/POST). | Sim | Sim | Sim |
| README de Operação | Guia de como configurar o banco e rodar a aplicação localmente. | Básico | Detalhado | Completo |

## 3. Detalhamento dos Artefatos

### Fase 1: Fundamentos (MVP 1)

O foco é a modelagem correta dos dados e o entendimento do ciclo de vida do Razor Pages.

- **Diagrama de Classes:** Deve focar na estrutura de Itens e Categorias.
- **DER:** Deve mostrar chaves primárias e estrangeiras de forma clara.
- **Dicionário de Dados:** Explicar a precisão de campos como Preço (Decimal) e SKU (String).

### Fase 2: Lógica e Desacoplamento (MVP 2)

O foco aqui é o processo e a integridade da regra de negócio.

- **Diagrama de Sequência:** Exigido especificamente para o fluxo de "Baixa de Estoque". Deve mostrar a interação entre a Página e a Classe de Serviço.
- **Dicionário de Dados:** Atualizado com as tabelas de Kart e Ordens de Serviço.

### Fase 3: Segurança e Maturidade (MVP 3)

O foco é a entrega profissional e a segurança.

- **Mapa de Rotas:** Deve indicar quais rotas são protegidas por autenticação e quais exigem perfil de Administrador.
- **README Profissional:** Deve conter instruções de configuração do `appsettings.json`, gerenciamento de Migrations e como realizar o primeiro login (Seed Data).

## 4. Padrão de Entrega

Todos os diagramas devem ser entregues preferencialmente em formato de imagem (`.png`) ou através de código Mermaid.js dentro do próprio repositório no GitHub.