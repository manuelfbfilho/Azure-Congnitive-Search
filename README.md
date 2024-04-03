<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="50px" src="https://github.com/manuelfbfilho/Burcador_CEP/blob/main/Fernandes.png?raw=true"></a>
    <span> 
Azure Cognitive Search: Utilizando AI Search para indexação e consulta de Dados</span>
</h1>

Repositório criado para treinamento de aprendizado de mais uma funcionalidade do Azure AI, preparatório para a certificação Microsoft Azure AI Fundamentals (+AI-900).

O desafio propõe que seja criada uma pesquisa que funcione juntamente com um serviço de inteligência artificial para identificar palavras-chave, sentimentos, utilizando também o serviço de armazenamento do azure.

[Documentação Oficial](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)

## Passo 1: Criando recurso do Asure AI Search:     

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/01%20-%20config%20da%20busca.gif" width=""/> ...  

## Passo 2: Criando recurso do Azure AI services:      

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/02%20-%20config%20do%20servi%C3%A7o%20de%20IA.gif" width=""/> ... 

## Passo 3: Criando o storage:      

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/03%20-%20Cria%C3%A7%C3%A3o%20do%20storage.gif" width=""/> ... 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/04%20-%20deploy%20completo.png" width=""/> ...
...

## Passo 4: Permitindo acesso anônimo ao Blob:      

Como nosso laboratório é apenas didático, para aprender os princípios da inteligência artificial com o Azure precisamos permitir o acesso anônimo ao blob para simplificar e facilitar nossas implementações. Após criar o seu Storage, acesse-o e navegue até a guia SETTINGS > CONFIGURATION seguindo os passos abaixo:

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/05%20-%20permitindo%20acesso%20anonimo%20de%20blob.gif" width=""/> ... 


## Passo 5: Criando o Container:      

Navegue até a guia DATA STORAGE > CONTAINERS, para criar o container dentro do storage e adicionar as pesquisas que seraão analisadas pelo AI SERVICE.

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/06%20-%20criando%20container.gif" width=""/> ...   
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/07%20adicionando%20pesquisas%20ao%20container.gif" width=""/> ...  

## Passo 6: Importação e indexação de dados para o AI SEARCH:      

Neste ponto você precisa linkar / importar os dados que você inseriu e configurou no seu STORAGE, volte para o AI SEARCH e siga os passos abaixo:

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/08%20-%20importando%20os%20dados.gif" width=""/> ... 

Esta é a parte mais importante de todo o processo, assim como o bootcamp fala são muitos passos que você precisa seguir à risca.

Ao seguir a [Documentação](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html) você chegará em INDEX DOCUMENTS, o qual o gif acima mostra o início do processo, siga os tópicos até chegar na sessão 4:

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/09%20-%20observa%C3%A7%C3%A3o.png" width=""/> ... 

**4. In the Attach Cognitive Services section, select your Azure AI services resource.**

Note que a instrução manda que selecionemos o recurso AI SERVICE configurado, porém, para mim, não mostrou nenhum, apenas uma informação dizendo que meu acesso era gratuito e que as configurações são limitadas, não se preocupe pode passar para o passo 5. In the Add enrichments section.

Siga todas as configurações terminando no passo 17. Select the indexer name to see more details.

## Passo 7: Consultando o índice:      

Feitas todas as configurações vamos voltar ao AZURE AI SERVICES, entrar no nosso serviço, e através do SEARCH EXPLORER testar se tudo foi indexado e se a consulta esta funcionando, utilizando os comandos:

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/11%20-%20testando%20a%20pesquisa.png" width=""/> ... 

```
search=*&$count=true    (  verifica se a indexação está funcionando e mostra os documentos )
```
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/12%20-%20testando%20a%20pesquisa.png" width=""/> ... 

```
search=locations:'Chicago' ( Consulta as ocorrências acontecidas em Chicago )
```
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/13.png" width=""/> ... 

```
search=sentiment:'negative' ( Consulta as ocorrências com sentimento negativo )
```
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP04%20-%20Intelig%C3%AAncia%20de%20documentos%20e%20minera%C3%A7%C3%A3o%20de%20conhecimento/14.png" width=""/> ... 


## Observações finais:      

As ferramentas de inteligência artificial do Azure facilitam a consulta em documentos, pesquisas e depoimentos, agilizando ainda mais a consulta de satisfação de empresas sobre seus produtos e serviços.

<b>OBS.:</b> <i>Imagens e parte da formatação deste README, utilizando da da mesma estrutura do nosso colega [Alex Lopes (alexklenio)](https://github.com/alexklenio).</i>


---

## Contatos 
[![Linkedin](https://img.shields.io/badge/Linkedin-000?style=for-the-badge&logo=linkedin&logoColor=30A3DC)](https://www.linkedin.com/in/manuelfbfilho)
<br>
[![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=30A3DC)](https://github.com/manuelfbfilho)
