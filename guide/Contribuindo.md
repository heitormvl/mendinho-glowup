# Guia de Padronização: Engenharia de Software e Versionamento

## Informações do Projeto

- **Projeto:** Ecossistema CMK (Campeonato Maverick de Kart)
- **Responsável Técnico:** Matheus
- **Mentor:** Heitor (Maverick)

## 1. Nomenclatura de Branches

O repositório utiliza *rulesets* para validar a criação de branches. O push será bloqueado pelo servidor caso o nome da branch não siga um dos prefixos abaixo:

- `feat/`: Implementação de novas funcionalidades ou requisitos do MVP.
- `fix/`: Correção de bugs, erros de lógica ou problemas de ambiente.
- `docs/`: Atualização de artefatos (UML, DER, Dicionário de Dados) ou arquivos Markdown.
- `refactor/`: Melhorias de código que não alteram o comportamento funcional (Clean Code).

**Padrão Regex aplicado:** `^(feat|fix|docs|refactor)\/.*`

## 2. Padrão de Commits (Conventional Commits)

As mensagens de commit devem ser claras e descritivas para manter a rastreabilidade das alterações no histórico do Git.

**Formato:** `tipo: descrição curta em letras minúsculas`

Exemplos:

- `feat: adiciona modelagem da entidade kart e migrations iniciais`
- `fix: corrige vinculo de chave estrangeira na tabela de insumos`
- `docs: inclui diagrama de sequencia do processo de baixa de estoque`
- `refactor: aplica injecao de dependencia no pagemodel de inventario`

## 3. Fluxo de Trabalho (GitHub Flow)

O acesso direto à branch principal (`main`) está bloqueado por regras de proteção. Toda e qualquer alteração deve seguir o fluxo abaixo:

1. **Isolamento:** Criação de branch a partir da `main` com nomenclatura padronizada.
2. **Desenvolvimento:** Commits frequentes e atômicos na branch de trabalho.
3. **Entrega:** Abertura de Pull Request (PR) utilizando o template obrigatório do repositório.
4. **Review Automatizado:** O GitHub Copilot realizará uma análise automática de padrões e sintaxe.
5. **Review Humano:** O mentor realizará a revisão técnica dos artefatos e do código.
6. **Merge:** O merge será liberado apenas após a aprovação do mentor e a resolução de todas as pendências levantadas no review.

## 4. Governança e Revisão de Código

O ambiente foi configurado com travas automáticas para garantir a qualidade:

- **Required Approvals:** É necessária no mínimo uma aprovação manual para o merge.
- **Status Checks:** O merge depende do sucesso da Action de validação de nomenclatura (`check-branch-name`).
- **Thread Resolution:** Todas as conversas e comentários iniciados no PR devem ser marcados como resolvidos antes da integração.
- **Copilot Review:** O sistema realizará varreduras em busca de vulnerabilidades e sugestões de otimização no Razor Pages.
