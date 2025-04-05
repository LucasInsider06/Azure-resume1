# Azure OpenAI

Este projeto foi feito com o intuito de comprovar meus aprendizados sobre Azure OpenAI no Playground. A seguir, apresentarei os conceitos e macetes aprendidos ao longo do curso.

### Deploy

Para fazer o deploy desse projeto, verifique se você possui o acesso de Admin OU se tem acesso o suficiente para lançar o recurso OpenAI no Azure

Após isso, será possível acessar o Playground, uma UI facilitada com o intuito de explorar os recursos. Os recursos são o desenvolvimento de prompt e o preparo de modelos especializados a alguma função.

obs: o mesmo prompt pode ter resultados diferentes, pois modelos de linguagem são estocásticos

### Tokenização

para configurar os tokens, é preferível que se utilize da língua inglesa. Isso, uma vez que o português consome mais tokens que o inglês na maioria dos casos. Ademais, a ferramenta usada para converter Tokens é a [TikToken](https://platform.openai.com/tokenizer) 

### Principais variáveis:
- Temperatura
- Top-P
- Tokens máximos
- Penalidades
- Sistema de mensagens

### Configurando o Playground
De início, use o System Message para definir o contexto inicial, instuções iniciai e manipular o comportamento

Formas de fazer um bom System Message: Zero-shot e One-shot

Zero-shot:
- sem exemplos
- respostas diretas e sem bifurcações no raciocínio
- baseado APENAS no prompt
- Não possui muita capacidade para formatar a partir da adição de exemplos novos

One-shot:
- Utiliza exemplos
- Resposta ampla 
- Baseia-se no prompt e, também, em outras fontes
- Pode ser formatado com mais facilidade a partir da adição de exemplos

## Aprofundando as variáveis:

### Top-P x Temperatura

Temperatura: Pega um número x de palavras e Controla quão aleatório são as ligações 

Temperatura 0: Respostas previsíveis e deterministas
Temperatura 1: Respostasmuito improváveis, a maioria sem sentido

Top-P: Controla quais palavras podem ser usadas na possível escolha, ou seja, filtra as opções escolhidas pela tempetratura

Top-P 0.1: só considera o primeiro grupo de palavras até dar o eixo de 10% das possibilidades

Top-P 0.9: considera palavras até dar o eixo de 90% das possibilidades

#### Obs:

Top-P alto + Temperatura alta = criatividade máxima
Top-P alto + Temperatura baixa = variedade controlada
Top-P baixo + Temperatura alta = criatividade limitada
Top-p baixo + Temperatura baixa = máxima previsibilidade

como são alterações bruscas, altere Top-P OU Temperatura. Raramente será bom alterar os dois simultaneamente.

### Frequency/Presency

Frequency Penalty: defini quanto o algorítmo punirá a repetição de tokens

Presency Penalty: penalidade por diversidade temática

### Criar boas imagens usando o Dall-E 

para gerar imagens condizentes com a ideia inicial, alguns passo a passos devem ser obecidos. 
1) O prompt deve ter clareza e especificidade
2) O contexto da imagem idealizada deve ser bem detalhado
3) O prompt precisa de uma estrutura concisa

OBS: utilizar o Dall-E SOMENTE para prototipar coisas, é muito fácil identificar algo feito por IA



### Melhores práticas com prompts:



- começar com defaults
- ajustar um parâmetro por vez
- documentar os resultados 
- alterar baseado em feedback


#### Exemplos



Você guia a IA assistente a partir de uma situação exemplo e molda a forma que ela vai responder.



Use os exemplos como uma forma de auxiliar o prompt, ou seja, de preferência, modifique o prompt para atender cada exemplo que você quer aplicar



###Aplicações Práticas 



Criar e conversar com um Blob
Fazer prompt engineering
Testar chat em CLI 
Gerar imagens

Blob: crie um container (storage account); faça um upload dos arquivos; depois, crie um search service; use o pricing tier, estourando o limite, no STANDARD; indexe direito pois o blob ocupa muitos dados.

## Referência

 - [Bootcamp DIO: Microsoft AI for Tech - OpenAI Services](https://web.dio.me/track/microsoft-azure-open-ai)


