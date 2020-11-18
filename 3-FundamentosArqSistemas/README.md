# Fundamentos da Arq de Sistemas

# Vantagens e Desenvolvimento de Webservices

#### O que são serviços web
- webServises - São soluções para que aplicações se comuniquem independente da linguagem em que foram construídas (XML/JSON/...)
- webServices são APIs que se comunicam pela web, mas webServices não necessariamente são APIs
- XML -> marcação <tags>
- JSON -> chaves e aspas { }
  
#### SOAP - Simple Object Access Protocol
- Protocolo XML - HTTP
- independente de plataforma / linguagem 
- permite outros protocolos além do HTTP

## XML
- linguagem de marcação criada nos anos 90
- Facilita a separação de conteudo por causa das ``<tags>``
- SOAP Envelope (pai - encapsula toda a mensagem)
  - SOAP header (tolken..)
  - SOAP body (detalhes da mensagem)
- tags ilimitadas

#### WSDL - Web Services Description Language

- Contrato de serviço, descreve o webservice
- é um XML com as especificações do serviços
- 
#### XSD - XML Schema Definition
- Descreve como vai montar o XML
- Define o que é obrigatório
- documentaçã

## REST - Representational State Transfer
- Estado representcional do objeto naquele momento
- XML ou JSON
- arquitetura de fácil compreensão
- requisicão HTTP
- retorna um JSON, texto, xml...
- API: conjunto de rotinas e padronizações de webservices

## API - Application Programming Interface
- São conjuntos de rotinas documentados e disponibilizados por uma aplicação para que outras possam consumir suas funcionalidades
- Principais métodos HTTP: GET(select) POST(create) PUT(update) DELETE(delet e)


#### JSON - JavaScript Object Notation
- formatação mais leve
- utilizado para as mesmas coisas que o XML
- Estruturas de chave - valor{} , listas []
- Status Code: estado da operação solicitada (de 100 a 500)
- https://developer.mozilla.org/pt-PT/docs/Web/HTTP/Status
  - 100 - Information responses (apenas um aviso)
  - 200 - Success responses (recebeu e processou, criou...)
  - 300 - Redirection messages
  - 400 - Erro do cliente
  - 500 - Erro do servidor
- DICA: Request: HTTP for humans
  
  
# Conceitos de arquitetura em aplicações para a internet @jeffhsta

## Introdução à arquitetura de sistemas

1. Monolito
  - Uma aplicação única
  - Um banco de dados
  - com o aumento da demanda uma instância pode não ser suficiente
  - é melhor ter várias instâncias para se uma falhar as outras recebem
2. Microserviços 1
  - um serviço para cada operação
  - que podem acessar bancos de dados diferentes
  - cada caixa é como se fosse 1 monolito que conversa com o outro.
  - Pode se comunicar inclusive com outros serviços externos
2. Microsserviços 2
  - os serviços não se comunicam mais diretamente, existe um message broker
  - a plataforma inteira fica refém do message broker (problema)
3. Microsserviços 3
  - O Proxy em vez de redirecionar direto para o serviço, rediciona para um gerenciador de pipeline
  - Cada aplicação tem passos para seguir
  - se o gerenciador de pipeline sai do ar, a plataforma inteira está fora do ar.

## Gerenciamento de erros
- onde é mais complexo? - processos assíncronos (Microsserviços 2 e 3)
- como resolver 
  - ms2: dead letter queue (fila de mensagens que precisam ser reprocessadas)
  - ms2: tentar corrigir e processar a mensagem novamente
  - ms2: Filas de re-tentativas
  - ms3: se o processo der erro ele tem que saber corrigir todos os passos anteriores
  

