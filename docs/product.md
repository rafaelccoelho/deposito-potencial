# Depósito Potencial

## 1. Visão do Produto

O **Depósito Potencial** é um sistema de gestão desenvolvido para pequenos e médios depósitos de materiais de construção.

O sistema terá como objetivo centralizar as principais operações do negócio em uma única plataforma, incluindo:

- cadastro e gestão de produtos;
- controle de estoque;
- vendas no balcão;
- vendas por canais digitais;
- clientes;
- fornecedores;
- compras;
- orçamentos;
- entregas;
- contas a pagar;
- contas a receber;
- relatórios gerenciais.

A arquitetura será desenvolvida inicialmente para uma única empresa, mas deverá evitar decisões que dificultem uma futura evolução para um modelo **SaaS multiempresa**.

---

## 2. Problema

Pequenos e médios depósitos podem ter operações distribuídas entre sistemas diferentes, planilhas, aplicativos de mensagens e processos manuais.

Isso pode gerar problemas como:

- falta de controle preciso do estoque;
- dificuldade para acompanhar vendas;
- informações de clientes espalhadas;
- dificuldade para acompanhar contas a pagar e receber;
- perda de informações de orçamentos;
- dificuldade para acompanhar entregas;
- pouca visibilidade sobre os resultados do negócio;
- retrabalho entre vendedores, estoque e administração.

O Depósito Potencial pretende centralizar essas informações e proporcionar uma visão integrada da operação.

---

## 3. Público-alvo

O produto será inicialmente direcionado a:

- pequenos depósitos de materiais de construção;
- médios depósitos de materiais de construção;
- lojas de materiais de construção;
- estabelecimentos que trabalham com vendas presenciais e digitais.

O foco inicial será uma operação de pequeno/médio porte, evitando complexidade desnecessária de grandes redes varejistas.

---

## 4. Personas

### Proprietário

Responsável pelo negócio.

Principais necessidades:

- acompanhar vendas;
- acompanhar resultados;
- controlar contas;
- acompanhar estoque;
- identificar produtos mais vendidos;
- tomar decisões de compra.

### Gerente

Responsável pela operação.

Principais necessidades:

- acompanhar estoque;
- controlar compras;
- acompanhar vendas;
- gerenciar vendedores;
- acompanhar entregas;
- analisar indicadores.

### Vendedor

Responsável pelo atendimento ao cliente.

Principais necessidades:

- consultar produtos;
- consultar preços;
- cadastrar clientes;
- criar orçamentos;
- registrar vendas;
- acompanhar pedidos;
- iniciar vendas provenientes de canais digitais.

### Estoquista

Responsável pelo controle físico dos produtos.

Principais necessidades:

- registrar entradas;
- registrar saídas;
- realizar ajustes;
- realizar inventários;
- consultar movimentações;
- identificar produtos abaixo do estoque mínimo.

### Responsável por entregas

Responsável pela logística.

Principais necessidades:

- visualizar entregas;
- consultar endereço;
- acompanhar status;
- registrar saída para entrega;
- registrar entrega realizada.

### Administrador

Responsável pela configuração do sistema.

Principais necessidades:

- gerenciar usuários;
- configurar permissões;
- configurar parâmetros do sistema;
- administrar cadastros.

---

## 5. Objetivos

### Objetivo principal

Criar uma plataforma capaz de centralizar a operação de um pequeno/médio depósito de materiais de construção.

### Objetivos secundários

- reduzir processos manuais;
- reduzir erros de estoque;
- facilitar o processo de venda;
- melhorar o acompanhamento financeiro;
- organizar entregas;
- disponibilizar indicadores gerenciais;
- permitir futura integração com canais digitais;
- criar uma base tecnológica para futura evolução para SaaS;
- criar uma arquitetura preparada para futuras funcionalidades de IA.

---

## 6. Módulos do sistema

O sistema será dividido inicialmente nos seguintes módulos:

### Produtos

Responsável pelo catálogo de produtos.

Funcionalidades:

- cadastro;
- edição;
- consulta;
- categorias;
- marcas;
- unidades de medida;
- código interno;
- código de barras;
- preço de custo;
- preço de venda;
- estoque mínimo;
- situação do produto.

---

### Estoque

Responsável pelo controle das movimentações físicas.

Funcionalidades:

- entrada;
- saída;
- ajuste;
- inventário;
- consulta de saldo;
- histórico de movimentações;
- estoque mínimo;
- produtos sem estoque.

Regra fundamental:

> Toda alteração relevante do estoque deverá possuir uma movimentação registrada.

---

### Clientes

Funcionalidades:

- cadastro;
- contatos;
- endereço;
- histórico de compras;
- histórico de orçamentos;
- histórico de entregas.

---

### Fornecedores

Funcionalidades:

- cadastro;
- contatos;
- produtos fornecidos;
- histórico de compras;
- condições comerciais.

---

### Vendas

O sistema deverá suportar vendas realizadas no estabelecimento e vendas originadas de canais digitais.

Funcionalidades:

- venda no balcão;
- venda originada de canal digital;
- seleção de cliente;
- produtos;
- descontos;
- formas de pagamento;
- parcelamento;
- baixa automática do estoque;
- histórico da venda.

---

### Orçamentos

Funcionalidades:

- criação de orçamento;
- inclusão de produtos;
- desconto;
- validade;
- envio ao cliente;
- aprovação;
- cancelamento;
- conversão de orçamento em venda.

Fluxo:

```text
Cliente
   ↓
Orçamento
   ↓
Aprovado
   ↓
Venda
   ↓
Pagamento
   ↓
Entrega
```

---

### Compras

Funcionalidades:

- pedido de compra;
- fornecedor;
- itens;
- quantidade;
- custo;
- recebimento;
- entrada no estoque.

Fluxo:

```text
Necessidade
    ↓
Pedido de compra
    ↓
Fornecedor
    ↓
Recebimento
    ↓
Estoque
```

---

### Entregas

O módulo de entrega fará parte da primeira versão funcional.

Funcionalidades:

- criação de entrega;
- endereço;
- venda relacionada;
- data prevista;
- responsável;
- veículo;
- status;
- observações;
- confirmação de entrega.

Status previstos:

```text
Pendente
   ↓
Separando
   ↓
Pronto para entrega
   ↓
Em transporte
   ↓
Entregue
```

---

### Financeiro

O sistema deverá contemplar contas a pagar e contas a receber.

#### Contas a receber

Exemplos:

- vendas;
- parcelas;
- pagamentos pendentes;
- pagamentos recebidos;
- vencimentos.

#### Contas a pagar

Exemplos:

- fornecedores;
- despesas;
- aluguel;
- serviços;
- outras obrigações.

Funcionalidades:

- lançamento;
- vencimento;
- pagamento;
- baixa;
- situação;
- categorias;
- consulta;
- relatórios.

---

## 7. Canais de venda

O produto deverá considerar desde o início uma estratégia omnichannel.

### Canal 1 — Balcão

Venda realizada diretamente no estabelecimento.

### Canal 2 — Site

Possibilidade futura de venda através de uma interface web voltada ao cliente.

### Canal 3 — WhatsApp

O sistema deverá ser projetado para permitir futuramente integração com WhatsApp.

Exemplo:

```text
Cliente
   ↓
WhatsApp
   ↓
Atendimento
   ↓
Orçamento
   ↓
Aprovação
   ↓
Venda
   ↓
Entrega
```

A integração específica com o WhatsApp não precisa fazer parte do primeiro incremento técnico, mas o domínio deverá ser estruturado para não impedir essa evolução.

---

## 8. MVP

O MVP deverá permitir que um depósito execute seu fluxo operacional básico.

### Incluído no MVP

#### Cadastro

- produtos;
- categorias;
- marcas;
- clientes;
- fornecedores;
- usuários.

#### Estoque

- entrada;
- saída;
- ajuste;
- consulta;
- histórico;
- estoque mínimo.

#### Vendas

- venda;
- itens;
- cliente;
- pagamento;
- desconto;
- baixa de estoque.

#### Orçamentos

- criação;
- edição;
- aprovação;
- conversão em venda.

#### Compras

- pedido;
- recebimento;
- entrada no estoque.

#### Entregas

- criação;
- acompanhamento;
- status;
- conclusão.

#### Financeiro

- contas a pagar;
- contas a receber;
- pagamentos;
- recebimentos;
- vencimentos.

#### Dashboard

- vendas;
- contas vencendo;
- estoque baixo;
- produtos mais vendidos;
- entregas pendentes.

---

## 9. Fora do MVP

Os seguintes recursos serão considerados para versões futuras:

- aplicativo mobile;
- integração completa com WhatsApp;
- e-commerce público;
- inteligência artificial;
- previsão de demanda;
- RAG;
- chatbot inteligente;
- multiempresa/SaaS;
- integração fiscal;
- integração com marketplaces;
- programa de fidelidade;
- roteirização avançada de entregas;
- integração com gateways de pagamento;
- sincronização offline;
- arquitetura distribuída avançada.

---

## 10. Visão futura

A evolução esperada do produto é:

```text
                    Depósito Potencial
                           │
       ┌───────────────────┼───────────────────┐
       │                   │                   │
     Gestão              Vendas             Logística
       │                   │                   │
   Estoque             Balcão             Entregas
   Compras             Site               Motoristas
   Financeiro          WhatsApp
       │
       └───────────────────┬───────────────────┘
                           │
                        Dados
                           │
                           ▼
                           IA
                           │
             ┌─────────────┼─────────────┐
             │             │             │
         Assistente   Previsão       Análises
                       demanda
```

Posteriormente:

```text
                    Plataforma SaaS
                           │
             ┌─────────────┼─────────────┐
             │             │             │
          Empresa A     Empresa B     Empresa C
```

---

## 11. Princípios do produto

### Simplicidade

O sistema deve ser fácil de utilizar por pessoas que não possuem conhecimento técnico.

### Confiabilidade

Operações críticas, especialmente estoque e financeiro, devem possuir rastreabilidade.

### Segurança

Usuários somente poderão executar operações autorizadas.

### Evolução

A arquitetura deve permitir crescimento sem introduzir complexidade desnecessária no início.

### Dados como ativo

As informações de vendas, estoque, clientes e financeiro deverão formar uma base para futuros relatórios e funcionalidades de inteligência artificial.

---

## 12. Definição de sucesso do MVP

O MVP será considerado funcional quando um usuário conseguir executar o seguinte fluxo completo:

```text
Cadastrar produto
       ↓
Cadastrar cliente
       ↓
Registrar estoque
       ↓
Criar orçamento
       ↓
Aprovar orçamento
       ↓
Gerar venda
       ↓
Registrar pagamento
       ↓
Baixar estoque
       ↓
Criar entrega
       ↓
Registrar entrega
       ↓
Registrar recebimento
```

Esse fluxo será nosso primeiro grande **"vertical slice"** do produto.

---

## 13. Próxima etapa

Após a aprovação deste Product Discovery, o projeto deverá avançar para:

**Etapa 02 — Requisitos e Histórias de Usuário**

Nessa etapa serão definidos:

- requisitos funcionais;
- requisitos não funcionais;
- épicos;
- histórias de usuário;
- critérios de aceitação;
- prioridades;
- MVP;
- backlog inicial.

As histórias serão posteriormente transformadas em **Issues do GitHub**.