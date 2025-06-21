Desafio 5 - Instalação e Configuração do GitHub Copilot com o VS Code

Criação de jogo com diferentes LLMs (Large Language Models)

Criar jogos com LLMs significa usar modelos de linguagem (como GPT, Claude, etc.) para gerar conteúdo dinâmico, diálogos, regras ou até mesmo lógica de jogo. Isso permite experiências interativas e adaptativas, como RPGs baseados em texto, jogos de perguntas e respostas, ou aventuras com múltiplos caminhos.

Exemplo prático:

Imagine um jogo estilo Choose Your Own Adventure onde o jogador digita ações e o LLM responde com a continuação da história. Cada modelo pode ser usado para uma função diferente:

- GPT-4: gera narrativa e diálogos.
- Claude: cria regras e lógica de jogo.
- Azure OpenAI: reescreve instruções com estilo divertido e multilíngue.

Ferramentas envolvidas:

- Azure OpenAI Service
- Azure Functions (para lógica de backend)
- Azure Static Web Apps (para frontend do jogo)
- Azure Cosmos DB (para salvar progresso do jogador)

Criação de API em Node.js para buscar endereços em JSON

Uma API em Node.js pode ser usada para expor dados de endereços armazenados em um arquivo JSON ou em um banco de dados. Essa API pode receber uma requisição com um CEP ou nome de rua e retornar os dados correspondentes.

Exemplo prático:

![image](https://github.com/user-attachments/assets/58b503fd-1312-48aa-b776-928e6961aae5)

Exemplo de enderecos.json:
[
  { "cep": "12345-678", "rua": "Rua das Flores", "cidade": "Rio de Janeiro" },
  { "cep": "98765-432", "rua": "Av. Brasil", "cidade": "São Paulo" }
]

Exemplo de enderecos.json

[
  { "cep": "12345-678", "rua": "Rua das Flores", "cidade": "Rio de Janeiro" },
  { "cep": "98765-432", "rua": "Av. Brasil", "cidade": "São Paulo" }
]
