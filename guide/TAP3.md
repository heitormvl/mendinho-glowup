# Termo de Abertura de Projeto: CMK Admin Portal
**Cliente:** Diretoria Executiva - CMK
**Responsável Técnico:** Matheus

## 1. Visão Geral
Finalização do ecossistema CMK com foco em segurança, auditoria e controle de acesso. O sistema deve ser blindado contra acessos não autorizados e estar pronto para uso por diferentes perfis de funcionários.

## 2. Requisitos Funcionais (Escopo)
* Sistema de Login e Logout.
* Diferenciação de perfis: 
    * **Mecânico:** Abre e fecha Ordens de Serviço.
    * **Administrador:** Gerencia estoque, usuários e deleta registros.
* Painel de resumo (Dashboard) mostrando total de karts em manutenção e valor total em estoque.

## 3. Critérios de Aceite Técnico (Análise de Código)
* **Segurança:** Implementação do ASP.NET Core Identity.
* **Autorização:** Uso do atributo `[Authorize]` por pastas ou páginas específicas.
* **Performance:** Uso de Projeções (LINQ Select) para o Dashboard, evitando carregar objetos pesados do banco.
* **Configuração:** Uso correto do `appsettings.json` para diferentes ambientes.

## 4. Prazo de Entrega
* 90 dias após o início (30 dias após o MVP 2).
