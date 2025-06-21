Desafio 2 - Criando um Blog com Container Apps

Criação de Dockerfile

Um Dockerfile é um arquivo de texto que contém instruções para construir uma imagem Docker. Ele define o ambiente, dependências e comandos necessários para executar uma aplicação em um container.

Exemplo prático:

![image](https://github.com/user-attachments/assets/ca93d2f7-e1fa-4aed-af2c-7f4303877269)

Esse Dockerfile cria uma imagem para uma aplicação Node.js. Você pode construir a imagem com: docker build -t minha-app .

Criação de Resource Group

Um Resource Group é um contêiner lógico no Azure que agrupa recursos relacionados, como VMs, bancos de dados e redes. Ele facilita o gerenciamento, monitoramento e controle de acesso.

Exemplo prático:

![image](https://github.com/user-attachments/assets/eb7cba4f-b564-499c-bd84-371daf0852ef)

Esse comando cria um grupo de recursos chamado rg-cloud-native na região Leste dos EUA.

Criação de Container Registry (ACR)

O Azure Container Registry (ACR) é um repositório privado gerenciado para armazenar e gerenciar imagens de containers Docker e artefatos OCI.

Exemplo prático:

![image](https://github.com/user-attachments/assets/82ed82b5-8c6b-4054-b0b6-2a9e9eb1cee3)

Esse comando cria um ACR chamado meuRegistroACR com autenticação administrativa ativada.

Login no ACR

O login no ACR permite que você envie (push) ou baixe (pull) imagens do seu repositório privado.

Exemplo prático:

![image](https://github.com/user-attachments/assets/6858c6dd-1029-442e-8d85-fed57aa1a525)

Depois disso, você pode marcar e enviar uma imagem:

![image](https://github.com/user-attachments/assets/d993835f-8573-4e25-92a9-a8a7e2f3bbb8)

docker tag minha-app meuRegistroACR.azurecr.io/minha-app:v1
docker push meuRegistroACR.azurecr.io/minha-app:v1

![image](https://github.com/user-attachments/assets/97a7c315-4434-4640-b3c0-e8abd1e35f70)
