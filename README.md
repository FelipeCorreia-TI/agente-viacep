## Respostas da atividade

1. Como as ferramentas externas ajudam os agentes a executarem ações reais em um sistema?
R: As ferramentas externas permitem que os agentes superem as limitações de seus modelos de linguagem (que são estáticos e limitados ao processamento de texto), concedendo a eles a capacidade de interagir com o mundo real. Elas possibilitam consultar dados em tempo real, realizar cálculos precisos, acessar bancos de dados, integrar com APIs externas e executar ações práticas (como enviar e-mails, salvar arquivos ou manipular sistemas).

2. Qual arquivo é a ferramenta? Qual é o agente? Qual é a orquestração?
R: Como o código ou projeto específico não foi fornecido no enunciado, a divisão conceitual padrão é:

Ferramenta (Tool): O módulo ou arquivo responsável por executar uma função específica e isolada (ex: um script que consome uma API externa).

Agente (Agent): O componente inteligente (geralmente impulsionado por um LLM) que analisa a entrada do usuário e decide qual ferramenta usar e com quais parâmetros.

Orquestração (Orchestration): O fluxo de controle ou framework (como o loop principal ou um gerenciador de estados) que coordena a interação entre o usuário, o agente e as ferramentas, lidando com chamadas de funções e retornos.

3. O que aconteceria se o agente respondesse sem chamar a ferramenta?
R: O agente dependeria exclusivamente de sua memória interna (dados de treinamento). Caso a pergunta exigisse dados atualizados, informações em tempo real ou consultas a bancos de dados privados, o agente provavelmente geraria uma resposta imprecisa, inventada (alucinação) ou diria que não possui a informação, falhando na execução correta da tarefa.

4. Qual é o fluxo percorrido quando você digita um CEP?
R: Entrada: O usuário digita o CEP no sistema.

Interpretação: O agente recebe o texto, entende a intenção de consultar um endereço e identifica que precisa usar uma ferramenta específica para isso.

Chamada de Ferramenta: O agente invoca a função de consulta de CEP, passando o número como argumento.

Requisição: A ferramenta faz uma chamada HTTP para uma API de CEP (como o ViaCEP) ou consulta um banco de dados interno.

Retorno de Dados: A API/serviço retorna os dados do endereço (logradouro, bairro, cidade, estado) em formato estruturado (ex: JSON).

Resposta Final: O agente recebe os dados da ferramenta, processa a informação e gera uma resposta clara e natural para o usuário.