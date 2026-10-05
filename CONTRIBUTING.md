# Contribuindo com o Depósito Potencial

Obrigado pelo interesse no projeto.

O Depósito Potencial está sendo desenvolvido inicialmente como um projeto de estudo e poderá evoluir futuramente para um produto comercial.

## Fluxo de desenvolvimento

O desenvolvimento deverá seguir, preferencialmente, o fluxo:

```text
Issue
  ↓
Branch
  ↓
Desenvolvimento
  ↓
Testes
  ↓
Pull Request
  ↓
Code Review
  ↓
Merge
```

## Branches

As branches deverão seguir uma convenção simples:

```text
feature/nome-da-funcionalidade
fix/nome-actor/nomdo-problema
refe-da-refatoracao
docs/nome-da-documentacao
test/nome-do-teste
```

Exemplos:

```text
feature/product-registration
feature/inventory-entry
fix/negative-stock
docs/update-readme
test/product-service
```

## Commits

Os commits deverão ser objetivos e descrever a alteração realizada.

Exemplos:

```text
feat: add product registration
fix: prevent negative inventory
test: add product validation tests
docs: update product documentation
refactor: simplify inventory service
```

## Pull Requests

Cada Pull Request deverá:

- possuir uma descrição clara;
- informar a Issue relacionada;
- incluir testes quando necessário;
- manter o escopo da alteração controlado;
- não incluir credenciais ou informações sensíveis.

## Qualidade

Antes de realizar o merge, o código deverá:

- compilar;
- passar pelos testes existentes;
- seguir os padrões definidos no projeto;
- não introduzir informações sensíveis no repositório.
