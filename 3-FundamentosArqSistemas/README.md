# Fundamentos da Arq de Sistemas

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
- Estruturas de chave - valor , listas
- Status Code: estado da operação solicitada (de 100 a 500)
- https://developer.mozilla.org/pt-PT/docs/Web/HTTP/Status
  - 100 - Information responses (apenas um aviso)
  - 200 - Success responses (recebeu e processou, criou...)
  - 300 - Redirection messages
  - 400 - Erro do cliente
  - 500 - Erro do servidor
  
  
