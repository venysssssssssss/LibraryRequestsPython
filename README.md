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

## 2. Instalar a Requests do Python

## 3. Primeira solicitação

## 4. Códigos de Status

## 5. Cabeçalhos

## 6. Texto de resposta

## 7. Usando a API de tradução

## 8. Casos de erro da API de tradução

## 9. Conclusão
