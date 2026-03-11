# Termo de Abertura de Projeto: CMK Assets
**Cliente:** Departamento de Manutenção - CMK
**Responsável Técnico:** Matheus

## 1. Visão Geral
O projeto consiste em desenvolver um sistema monolítico para controle de estoque de peças e insumos utilizados na manutenção dos karts da frota. O objetivo é substituir planilhas manuais por uma aplicação web centralizada.

## 2. Requisitos Funcionais (Escopo)
* Cadastro de categorias de peças (Motores, Pneus, Chassis).
* CRUD completo de itens com campos: Nome, SKU, Quantidade em Estoque e Preço Unitário.
* Listagem com filtros por categoria e busca por nome.
* Alerta visual para itens com estoque abaixo de 5 unidades.

## 3. Critérios de Aceite Técnico (Análise de Código)
* **Arquitetura:** Uso obrigatório de Razor Pages.
* **Dados:** Implementar o padrão InputModel para os formulários de criação/edição.
* **Persistência:** Uso de Entity Framework Core com Migrations (LocalDB ou SQLite).
* **UI:** Uso de Layouts compartilhados e Partial Views para componentes repetidos.

## 4. Prazo de Entrega
* 30 dias após o início.