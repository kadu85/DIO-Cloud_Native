Desafio 6 - Construção de uma Aplicação de Aluguel de Carros totalmente Cloud-Native

Desenho da Arquitetura e Configuração do Ambiente Cloud

Uma arquitetura cloud-native é baseada em microsserviços, escalável, resiliente e desacoplada. No Azure, isso significa usar serviços como Azure App Service, Azure Functions, Azure API Management, Azure Cosmos DB e Azure Container Registry.

Exemplo prático:

- Frontend: hospedado em Azure Static Web Apps (React ou Angular)
- Backend/API: Azure App Service ou Azure Container Apps
- Banco de dados: Azure Cosmos DB (NoSQL) ou Azure SQL
- Mensageria: Azure Service Bus
- Funções serverless: Azure Functions para processos assíncronos
- CI/CD: GitHub Actions ou Azure DevOps

Configuração inicial via CLI:

az group create --name rg-jk-aluguel --location eastus
az appservice plan create --name plano-api --resource-group rg-jk-aluguel --sku B1 --is-linux
az webapp create --name jk-api --resource-group rg-jk-aluguel --plan plano-api --runtime "NODE|18-lts"

Desenvolvimento da API JK Aluguel de Carros

A API é o núcleo da aplicação, responsável por gerenciar carros, reservas, usuários e pagamentos.

Exemplo prático (Node.js + Express):

app.get('/carros', async (req, res) => {
  const carros = await db.collection('carros').find().toArray();
  res.json(carros);
});

app.post('/reservas', async (req, res) => {
  const reserva = { carroId: req.body.carroId, cliente: req.body.cliente, status: 'pendente' };
  await db.collection('reservas').insertOne(reserva);
  res.status(201).send(reserva);
});

Boas práticas:

- Versionamento: /api/v1/carros
- Autenticação com JWT
- Documentação com Swagger

Azure Function: RentProcess

Função serverless que processa reservas de aluguel de forma assíncrona, por exemplo, após o cliente clicar em "Confirmar Reserva".

Exemplo prático (JavaScript):

![image](https://github.com/user-attachments/assets/d5887894-0cff-4bc6-978a-f6e54ca7784e)

Gatilho: Azure Service Bus Queue

Uso: desacoplar o front-end do processamento de lógica de negócio.

Azure Function: Payment

Função que processa o pagamento da reserva, integrando com um gateway como Stripe ou Mercado Pago.

Exemplo prático (C#):

![image](https://github.com/user-attachments/assets/3d5b09c0-1e30-48a9-9e50-d8f86d6577d8)

Boas práticas:

- Validar token JWT do cliente
- Registrar logs e falhas no Application Insights
- Retentativas automáticas em caso de falha
