# Termo de Abertura de Projeto: CMK Service
**Cliente:** Gerência de Operações - CMK
**Responsável Técnico:** Matheus

## 1. Visão Geral
Evolução do sistema anterior para permitir o registro de manutenções realizadas nos karts (Ordens de Serviço). O sistema deve garantir que peças sejam debitadas do estoque automaticamente.

## 2. Requisitos Funcionais (Escopo)
* Cadastro de Karts (Número, Modelo, Ano).
* Abertura de Ordem de Serviço vinculada a um Kart.
* Adição de múltiplos itens (peças) a uma Ordem de Serviço.
* Regra de Negócio: Não permitir fechar uma OS se a peça solicitada não possuir estoque disponível.

## 3. Critérios de Aceite Técnico (Análise de Código)
* **Camada de Serviço:** A lógica de débito de estoque e validação de OS deve estar em uma `Service Class` injetada via DI.
* **Integridade:** Uso de Transações no EF Core para garantir que a OS só seja salva se o estoque for atualizado com sucesso.
* **UX:** Uso de TempData para exibir mensagens de sucesso ou erro (Toasts) após o POST.

## 4. Prazo de Entrega
* 60 dias após o início (30 dias após o MVP 1).
