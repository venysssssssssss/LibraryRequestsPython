# LibraryRequestsPython <!-- omit in toc -->
![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/b1db6e38-bb9a-4763-adbc-6d63943c9474) 

## Introdução <!-- omit in toc -->
- Em vários aplicativos Web, é comum conectar-se a vários serviços de terceiros usando APIs. Ao usar essas APIs, você tem acesso a dados como informações meteorológicas, placares esportivos, listas de filmes, tweets, resultados de mecanismo de busca e fotos. Também é possível usar as APIs para adicionar funcionalidades ao seu app. Exemplos dessas funcionalidades são pagamentos, agendamentos, e-mails, traduções, mapas e transferência de arquivos. Se você tivesse que criar qualquer uma dessas funcionalidades por contra própria, levaria muito tempo, mas com as APIs pode levar somente alguns minutos para se conectar a uma funcionalidade e acessar seus recursos e dados.

- Aprenderemos sobre a biblioteca Requests (Solicitações) do Python, que permite que você envie solicitações HTTP em Python.

- Uma vez que o uso de uma API implica em enviar solicitações HTTP e receber respostas, a biblioteca Requests permite que você utilize APIs no Python. Vamos demonstrar o uso de uma API de tradução de idioma aqui para você veja um exemplo de como ela funciona.

## Visão geral rápida de solicitações HTTP <!-- omit in toc -->

- As solicitações HTTP consistem na maneira como a Web funciona. Toda vez que você navega para uma página Web, seu navegador realiza várias solicitações para o servidor da página da Web. Então, o servidor responde com todos os dados necessários para renderizar a página e, na sequência, o seu navegador renderiza a página para que a veja.

- O processo genérico é o que segue: um cliente (como um navegador ou um script Python usando as Requests) enviará alguns dados para um URL e, em seguida, o servidor localizado no URL irá ler os dados, decidir o que fazer com os dados e retornar uma resposta para o cliente. Por fim, o cliente pode decidir o que fazer com os dados na resposta.

- Parte dos dados que o cliente envia em uma solicitação representa o método da solicitação. Alguns métodos de solicitação comuns são o GET, POST e o PUT. Normalmente, as solicitações GET são somente para leitura de dados, sem alterar nada, ao passo que as solicitações POST e PUT são geralmente usadas para modificar os dados no servidor. Por exemplo, a API Stripe permite que você utilize as solicitações POST para criar uma nova cobrança para que um usuário possa comprar algo do seu app.

- Ao enviar uma solicitação de um script Python ou uma solicitação dentro de um app Web, caberá a você - o desenvolvedor - decidir o que será enviado em cada solicitação e o que será feito com a respectiva resposta. Assim, vamos explorar isso enviando primeiro uma solicitação para o Scotch.io e, depois, usando uma API de tradução de idiomas.

## Contents <!-- omit in toc -->
- [1. Visão geral rápida de solicitações HTTP](#1-comandos-basicos)
- [2. Instalar a Requests do Python](#2-comandos-linux)
- [3. Primeira solicitação](#3-comandos-linux)
- [4. Códigos de Status](#4-comandos-linux)
- [5. Cabeçalhos](#5-comandos-linux)
- [6. Texto de resposta](#6-comandos-linux)
- [7. Usando a API de tradução](#7-comandos-linux)
- [8. Casos de erro da API de tradução](#8-comandos-linux)
- [9. Conclusão](#9-conclusão-rep)


## 1. Visão geral rápida de solicitações HTTP
- As solicitações HTTP consistem na maneira como a Web funciona. Toda vez que você navega para uma página Web, seu navegador realiza várias solicitações para o servidor da página da Web. Então, o servidor responde com todos os dados necessários para renderizar a página e, na sequência, o seu navegador renderiza a página para que a veja.

- O processo genérico é o que segue: um cliente (como um navegador ou um script Python usando as Requests) enviará alguns dados para um URL e, em seguida, o servidor localizado no URL irá ler os dados, decidir o que fazer com os dados e retornar uma resposta para o cliente. Por fim, o cliente pode decidir o que fazer com os dados na resposta.

- Parte dos dados que o cliente envia em uma solicitação representa o método da solicitação. Alguns métodos de solicitação comuns são o GET, POST e o PUT. Normalmente, as solicitações GET são somente para leitura de dados, sem alterar nada, ao passo que as solicitações POST e PUT são geralmente usadas para modificar os dados no servidor. Por exemplo, a API Stripe permite que você utilize as solicitações POST para criar uma nova cobrança para que um usuário possa comprar algo do seu app.

- Ao enviar uma solicitação de um script Python ou uma solicitação dentro de um app Web, caberá a você - o desenvolvedor - decidir o que será enviado em cada solicitação e o que será feito com a respectiva resposta. Assim, vamos explorar isso enviando primeiro uma solicitação para o Scotch.io e, depois, usando uma API de tradução de idiomas.

## 2. Instalar a Requests do Python
- Antes de fazermos qualquer coisa, precisamos instalar a biblioteca. Assim, vamos prosseguir com a instalação da requests, usando o pip. Se você ainda não tiver um ambiente virtual, é uma boa ideia criar um primeiro.

![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/e1140c51-5751-4da7-9d78-9bb1871f171c)
 
## 3. Primeira solicitação
- Para começar, vamos usar a Requests para solicitar o site Scotch.io. Crie um arquivo chamado script.py e adicione o seguinte código a ele. Neste artigo, não teremos muito código para trabalhar, de modo que, quando algo mudar, você somente poderá atualizar o código existente, em vez de adicionar novas linhas.

![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/d1ba05ae-e718-47e4-b92f-15f6ccdc0c43)

- Dessa forma, tudo o que esse código está fazendo é enviar uma solicitação GET para o Scotch.io. Esse é o mesmo tipo de solicitação que o seu navegador enviou para visualizar essa página. A única diferença, porém, é que a biblioteca Requests, na verdade, não consegue processar páginas em HTML. Assim, em vez de processar a página, você receberá apenas o HTML bruto e outras informações de resposta.

- Estamos usando a função .get() aqui, mas a Requests permite que você utilize outras funções, como .post() e .put() para também enviar essas solicitações.

- Você pode executá-la executando o arquivo script.py.

![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/cf245c9f-a5cc-4c0a-8faf-4220ec6ab13d)

Aqui está o que você recebe como resultado:

![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/a6f733b4-6636-47be-b0c7-355cdec6b0e4)

## 4. Códigos de Status

-A primeira coisa que podemos fazer é verificar o código de status. Os códigos HTTP variam de 1XX a 5XX. Os códigos de status comuns que você provavelmente viu são 200, 404 e 500.

-Aqui está uma visão geral rápida do que cada código de status significa:

-1XX - Informação
-2XX - Sucesso
-3XX - Redirecionar
-4XX - Erro de cliente (você cometeu um erro)
-5XX - Erro de servidor (eles cometeram um erro)
-Geralmente, o que você está procurando ao realizar suas próprias solicitações são os códigos de status próximos do código 200.

-A Requests reconhece que os códigos de status 4XX e 5XX são erros. Assim, se esses códigos de status forem retornados, significa que o objeto de resposta da solicitação retorna False.

-Você pode testar se uma solicitação respondeu com sucesso, verificando se a resposta é verdadeira. Por exemplo:

![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/359187e3-2d6e-4129-ac4b-04d006cb8657)

![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/d1805b2f-2d5e-4aa2-9ae7-3933f28824df)

-A mensagem “Houve falha na resposta” aparecerá apenas se um código de status de 400 ou 500 for retornado. Tente alterar o URL para algo sem sentido para ver a resposta falhar com um código 404.

-Você pode verificar o código de status diretamente, adicionando:

![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/93ab3208-18c1-42ad-ae23-322745ce6b26)

-Isso mostrará o código de status diretamente para que você mesmo possa verificar o número.

![image](https://github.com/venysssssssssss/LibraryRequestsPython/assets/99450704/026965db-93ad-45ed-ba00-b44b72c28f68)


## 5. Cabeçalhos

## 6. Texto de resposta

## 7. Usando a API de tradução

## 8. Casos de erro da API de tradução

## 9. Conclusão
