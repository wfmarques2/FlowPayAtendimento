# FlowPay Atendimento

Sistema de distribuição de atendimentos para a central de relacionamento da FlowPay. O sistema gerencia a distribuição automática de solicitações de clientes para times especializados de atendimento.

## 🚀 Funcionalidades Detalhadas

### Distribuição Automática
- Solicitações são automaticamente direcionadas para times específicos
- PROBLEMAS_CARTAO → Time CARTOES
- CONTRATACAO_EMPRESTIMO → Time EMPRESTIMOS
- Outros assuntos → Time OUTROS_ASSUNTOS

### Controle de Atendimentos
- Limite de 3 atendimentos simultâneos por atendente
- Sistema de fila quando todos atendentes estão ocupados
- Distribuição automática quando atendentes ficam disponíveis

### Gerenciamento de Times
- Três times especializados: CARTOES, EMPRESTIMOS, OUTROS_ASSUNTOS
- Monitoramento de fila por time
- Consulta de atendentes disponíveis

## 🛠️ Tecnologias Utilizadas
- Java 17
- Spring Boot 3.2.1
- Maven
- JUnit 5
- Swagger/OpenAPI

## ⚙️ Pré-requisitos
- Java JDK 17 ou superior
- Maven 3.6 ou superior

## 📦 Instalação e Execução

1. Clone o repositório
2. Execute: `mvn spring-boot:run`
3. Acesse: `http://localhost:8080/swagger-ui.html`

## Endpoints e Exemplos de Uso

### 1. Adicionar Atendente
- POST /api/atendimento/atendente - Adiciona novo atendente
- POST /api/atendimento/solicitacao - Cria nova solicitação
- GET /api/atendimento/fila/{time} - Consulta tamanho da fila
- GET /api/atendimento/atendentes/{time} - Lista atendentes do time 