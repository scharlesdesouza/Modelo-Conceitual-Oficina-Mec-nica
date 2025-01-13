# Sistema de Gerenciamento de Oficina Mecânica

## 📋 Descrição

Este projeto tem como objetivo gerenciar uma oficina mecânica, permitindo o controle de clientes, veículos, ordens de serviço e tipos de serviços prestados. A modelagem foi feita com base em um diagrama conceitual que define as principais entidades e seus relacionamentos no sistema.

---

## 🛠️ Funcionalidades

1. **Cadastro de Clientes**:
   - Nome e endereço.
   - Cada cliente pode estar associado a um ou mais veículos.

2. **Cadastro de Veículos**:
   - Dados básicos como placa e descrição do veículo.
   - Cada veículo está associado a um cliente.

3. **Gestão de Mecânicos**:
   - Cadastro de mecânicos incluindo nome, especialidade e matrícula.

4. **Gestão de Ordens de Serviço (OS)**:
   - Emissão de ordens de serviço contendo:
     - Data de emissão.
     - Status da ordem (aberta, em andamento, concluída, etc.).
   - Associação de um cliente e seu respectivo veículo à ordem de serviço.

5. **Tipos de Serviço**:
   - Cadastro de serviços disponíveis na oficina, como troca de óleo, revisão, etc.
   - Associação de cada ordem de serviço aos serviços realizados.

6. **Valores dos Serviços**:
   - Registro dos valores associados a cada tipo de serviço realizado em uma ordem.

---

## 🗂️ Estrutura do Modelo Conceitual

O modelo é composto pelas seguintes entidades principais:

- **Cliente**:
  - `idCliente` (PK): Identificador único do cliente.
  - `nome`: Nome do cliente.
  - `endereco`: Endereço do cliente.

- **Veículo**:
  - `idVeiculo` (PK): Identificador único do veículo.
  - `descricao`: Descrição ou modelo do veículo.
  - `placa`: Placa do veículo.
  - Relacionamento: Um cliente pode ter vários veículos.

- **Mecânico**:
  - `idMecanico` (PK): Identificador único do mecânico.
  - `nome`: Nome do mecânico.
  - `especialidade`: Especialidade do mecânico.
  - Relacionamento: Os mecânicos podem estar vinculados a ordens de serviço.

- **Ordem de Serviço**:
  - `idOrdem` (PK): Identificador único da ordem.
  - `dataOrdem`: Data de emissão da ordem.
  - `statusOrdem`: Status atual da ordem.
  - Relacionamento: Cada ordem de serviço está associada a um cliente, um veículo e possivelmente a um ou mais mecânicos.

- **Tipo de Serviço**:
  - `idTipoServico` (PK): Identificador do tipo de serviço.
  - `descricao`: Descrição do serviço.

- **Valores de Serviços**:
  - Relaciona os tipos de serviço realizados a suas respectivas ordens, incluindo os valores cobrados.

---

## 📋 Possíveis Melhorias

- Implementar autenticação de usuários.
- Adicionar relatórios financeiros.
- Integrar alertas para clientes (via SMS ou e-mail) sobre status das ordens.
- Criar uma interface amigável para entrada de dados.

---

