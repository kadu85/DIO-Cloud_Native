Desafio 1 - Armazenando dados de um E-Commerce na Cloud

Resource Group

Um Resource Group é um contêiner lógico no Azure que agrupa recursos relacionados (como VMs, bancos de dados, redes, etc.) para facilitar o gerenciamento, monitoramento e controle de acesso.

Exemplo prático:

Você está desenvolvendo um sistema de e-commerce. Pode criar um Resource Group chamado rg-ecommerce-prod e dentro dele colocar:

- Web App
- Banco de dados SQL
- Conta de armazenamento
- Application Insights

Assim, você pode aplicar políticas, permissões e monitoramento a todos esses recursos de forma centralizada.

SQL Database

O Azure SQL Database é um serviço de banco de dados relacional gerenciado baseado no SQL Server, oferecido como PaaS (Plataforma como Serviço).

Exemplo prático:

Você precisa armazenar dados de clientes, pedidos e produtos. Em vez de instalar e manter um SQL Server, você cria um banco sqldb-ecommerce no Azure SQL Database, que já vem com backup automático, escalabilidade e alta disponibilidade.

Storage Account

Uma Storage Account é o ponto de entrada para armazenar dados no Azure. Ela permite acesso a diferentes serviços de armazenamento: Blobs, Files, Queues e Tables.

Exemplo prático:

Você cria uma conta chamada stgecommercefiles para armazenar:

- Imagens de produtos (Blob)
- Logs de pedidos (Table)
- Arquivos compartilhados entre sistemas (File Share)

Blob Storage

O Blob Storage é um serviço dentro da Storage Account para armazenar grandes volumes de dados não estruturados, como arquivos de mídia, documentos e backups.

Exemplo prático:

Você armazena imagens dos produtos do seu e-commerce em um container chamado produtos dentro do Blob Storage. Cada imagem pode ser acessada via URL pública ou protegida com token.

![image](https://github.com/user-attachments/assets/471b1406-3e41-4595-bb14-a71d217a9f3c)



