Desafio 3 - API de Pagamentos Segura com Azure API Management

Criação de App Services

O Azure App Service é uma plataforma PaaS (Platform as a Service) que permite hospedar aplicações web, APIs REST e backends móveis sem se preocupar com a infraestrutura subjacente.

Exemplo prático:

Você pode criar um App Service para hospedar uma API em Node.js com o seguinte comando:

![image](https://github.com/user-attachments/assets/6e140630-fe77-4b1e-b080-5af4ab702e26)

Depois disso, você pode fazer o push do seu código via Git diretamente para o App Service.

Boas práticas de endpoints

Endpoints são os caminhos expostos por uma API para que clientes possam interagir com os recursos. Boas práticas garantem clareza, escalabilidade e segurança.

Boas práticas recomendadas:

- Use substantivos no plural: /clientes, /produtos
- Evite verbos: prefira GET /pedidos a GET /getPedidos
- Use HTTP verbs corretamente: GET, POST, PUT, DELETE
- Utilize versionamento: /api/v1/produtos
- Implemente status codes apropriados: 200 OK, 201 Created, 404 Not Found
- Adote filtros e paginação: /produtos?categoria=livros&page=2

Exemplo prático:

![image](https://github.com/user-attachments/assets/1e8782a5-17b4-4f8b-87e6-824062d03322)

Esse endpoint retorna todos os pedidos do cliente com ID 123.

Criação de autenticação com JWT

JWT (JSON Web Token) é um padrão para autenticação segura entre cliente e servidor. Ele carrega informações codificadas e assinadas digitalmente, como o ID do usuário e permissões.

Exemplo prático (Node.js + Express):

![image](https://github.com/user-attachments/assets/1562e374-a743-4a2d-b428-a0e0519bdca8)

const jwt = require('jsonwebtoken');
const token = jwt.sign({ userId: 42, role: 'admin' }, 'segredo123', { expiresIn: '1h' });

Uso no cabeçalho da requisição:

![image](https://github.com/user-attachments/assets/17e26251-ec57-48b3-84f6-add74ac19408)

Validação no backend:

![image](https://github.com/user-attachments/assets/7d45f74c-2052-4f46-9628-36b76186fa93)

Graphic_Art

{
  "prompt": "An Azure cloud native architecture diagram showing an App Service hosting a REST API with well-structured endpoints, secured by JWT authentication. The diagram includes a client sending a request with a JWT token, the App Service validating the token, and accessing protected resources. The style is clean, modern, and educational, using Azure branding colors.",
  "transparent_background": false,
  "response_text": "Aqui está uma imagem que representa como esses conceitos se conectam em uma arquitetura Azure Cloud Native:"
}
