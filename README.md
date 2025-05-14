# Teste Técnico: Senior Platform Engineer

Olá! Estamos muito animados com o seu interesse na vaga de Senior Platform Engineer e gostaríamos de propor um teste técnico prático para avaliarmos suas habilidades em um cenário que envolve o Google Cloud Platform (GCP), TypeScript e Terraform.
  
Este teste tem como objetivo simular um desafio real, onde você precisará provisionar uma infraestrutura básica no GCP e construir uma API simples para interagir com ela. Acreditamos que ele nos dará uma boa base para uma conversa técnica mais aprofundada sobre suas experiências e conhecimentos.

## O Desafio

Você deverá criar um projeto no Google Cloud Platform (GCP) e utilizar Terraform para provisionar alguns recursos essenciais. Em seguida, você desenvolverá uma API utilizando TypeScript e o framework Express (Node.js) para ser executada nessa infraestrutura.

## As Etapas

### 1. Provisionamento no GCP com Terraform:
- Crie uma rede VPC com um nome de sua preferência.
- Dentro dessa VPC, defina uma sub-rede com um range de IP adequado.
- Provisione uma instância de Compute Engine (Linux) nessa sub-rede. Para este teste, uma configuração básica (n1-standard-1, por exemplo) é suficiente. Certifique-se de permitir tráfego HTTP (porta 80) para esta instância.
- **Opcional (Diferencial)**: Como um ponto extra, você pode incluir a criação de um tópico e uma subscription do Pub/Sub.

### 2. Desenvolvimento da API com TypeScript e Express:
- Construa uma API simples em TypeScript utilizando o framework Express (Node.js).
- A API deve expor um endpoint HTTP na porta 80 (ou outra de sua escolha, desde que bem documentada).
- Ao receber uma requisição GET nesse endpoint, a API deve retornar uma mensagem simples (por exemplo, "Olá do GCP com TypeScript e Express!").
- **Diferencial**: Se você optar por trabalhar com o Pub/Sub, inclua uma rota adicional (como `/consume`) que tente consumir mensagens da subscription criada. A lógica de consumo pode ser básica, como apenas exibir a mensagem no console ou em um log.

### 3. Implantação na Compute Engine:
- Implante a API TypeScript na instância do Compute Engine que você provisionou. Você pode escolher o método de implantação que preferir (SSH e execução direta, PM2, etc.).
- Garanta que a API esteja acessível através do endereço IP público da sua instância.

### 4. Documentação:
Crie um arquivo README.md na raiz do seu projeto. Este arquivo é crucial e deve conter:
- Os comandos Terraform que você utilizou para provisionar a infraestrutura.
- Instruções claras e detalhadas de como executar a API na instância do Compute Engine, incluindo quaisquer dependências (por exemplo, como instalar o Node.js, dependências do projeto com npm install) e os comandos para build (se necessário, como npm run build) e para iniciar a aplicação (como npm start).
- Se houver variáveis de ambiente necessárias para a execução da sua API (por exemplo, configurações para o Pub/Sub), explique quais são e como devem ser configuradas na instância.
- O endereço IP público da instância e o endpoint principal da sua API.
- Se você implementou a funcionalidade do Pub/Sub, inclua o endpoint para consumir mensagens e quaisquer passos adicionais para testá-lo (por exemplo, como publicar uma mensagem no tópico utilizando a CLI do GCP).
- Compartilhe suas considerações sobre o processo e quaisquer desafios que você tenha encontrado.

## Entrega

Para a entrega, pedimos que você crie um repositório privado no GitHub e nos conceda acesso de leitura ao usuário `clucasmedeiros@gmail.com`. O repositório deverá conter todos os arquivos do seu projeto:
- Os arquivos de configuração do Terraform (.tf).
- O código da API TypeScript (utilizando Express) (.ts, package.json, tsconfig.json, etc.).
- O arquivo README.md.

## Avaliação e Próximos Passos

Avaliaremos seu teste com base na organização e funcionalidade do código Terraform, na estrutura e clareza da API em TypeScript e Express, na sua capacidade de implantar a aplicação, na qualidade da documentação e, se aplicável, na implementação da interação com o Pub/Sub.

Após a análise do seu teste, entraremos em contato para agendar uma conversa técnica. Durante essa conversa, poderemos aprofundar em suas escolhas de implementação, discutir os desafios encontrados e explorar seus conhecimentos sobre os serviços do GCP e práticas de desenvolvimento de plataforma.

Este teste é uma oportunidade para você demonstrar suas habilidades práticas e seu raciocínio técnico. Dedique o tempo necessário e, em caso de dúvidas, sinta-se à vontade para nos informar.

---

Agradecemos desde já o seu tempo e dedicação! Estamos ansiosos para ver o seu trabalho. 
