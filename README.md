# CursoHTTP

<h1 align="center">
    <a href="https://www.alura.com.br/curso-online-http-fundamentos">🔗 HTTP: Entendendo a web por baixo dos panos </a>
</h1>
<p align="center">🚀 Formulário de proposta de solução - HTTP 🚀 </p>

### Features

 <p align="justify"> :robot: Você ficou responsável por definir o melhor uso do protocolo HTTP para possibilitar a criação de uma API que realiza pesquisas de passagens de avião e cadastro de compradores. :robot: </p>

- [x] Para a parte de cadastro, nos diga qual verbo http você vai utilizar
- [x] Como vai passar os argumentos no momento da requisição
- [x] Esse endereço pode receber dados via formulário normal(form-url-encoded) ou JSON
- [x] Como você vai adicionar essa flexibilidade (form-url-encoded) ou JSON
- [x] Como é possível a comunicação seja feita com os dados criptografados. O que você sugeriria aqui e por que?

<h3 align="center">
Para a parte de cadastro, nos diga qual verbo http você vai utilizar
</h3>

<p align="justify"> :robot: Para o processo de cadastro temos duas opções de verbos HTTP para utilizar sendo elas GET e POST. Quando utilizamos o GET, os parâmetros são passados no cabeçalho da requisição. Por isso, podem ser vistos pela URI, sendo esse verbo o padrão para enviar dados quando submetemos um formulário HTTP, podendo alterar esse comportamento dizendo para o formulário qual do método (method) ele deve usar.  :robot: </p>

<p align="justify"> :robot: No caso de formulários web, é muito comum que esse método seja o POST, tendo esse como característica o envio dos parâmetros no corpo da requisição HTTP. Escondendo eles da URI. É pertinente salientar que se utilizarmos o método POST protegemos os dados submetidos pelo formulário. :robot: </p>

<h3 align="center">
Como vai passar os argumentos no momento da requisição
</h3>

<h3 align="center">
Esse endereço pode receber dados via formulário normal(form-url-encoded) ou JSON
</h3>

<h3 align="center">
Como você vai adicionar essa flexibilidade (form-url-encoded) ou JSON
</h3>
    

<p align="justify"> :robot: Em uma solicitação POST geralmente é enviada por meio de um formulário HTML e resulta em uma alteração no servidor. Nesse caso, o tipo de conteúdo é selecionado colocando a string adequada no atributo enctype do elemento <form>; application/x-www-form-urlencoded: as chaves e valores são codificados em tuplas de valor-chave separadas por '&', com um '='  entre a chave e o valor. Porem é pertinente salientar que uma API REST, ao disponibilizar um endpoint, "necessita" de um JSON (JavaScript Object Notation) como forma de transporte de informações (JSON é somente uma forma bem leve de representação e troca de informações).  <a href="https://www.treinaweb.com.br/blog/rest-nao-e-simplesmente-retornar-json-indo-alem-com-apis-rest">🔗 HTTP | JSON </a> :robot: </p>

<p align="justify"> :robot: Desta forma vamos padronizar nossa aplicação Content-Type: application/json, definindo que vamos Solicitar/Responder apenas usando formato JSON.:robot: </p>

<p align="justify"> :robot: Caso seja necessário ter a flexibilidade para receber via formulário normal (application/x-www-form-urlencoded: as chaves e valores são codificados em tuplas de valor-chave separadas por '&', com um '='  entre a chave e o valor), pretendo criar outro endpoint especifico para esse "serviço". :robot: </p>

<h3 align="center">
Como é possível a comunicação seja feita com os dados criptografados. O que você sugeriria aqui e por que?
</h3>
    
<p align="justify"> :robot: Quando a requisição POST é enviada através de um método diferente de um formulário HTML - como por meio de um XMLHttpRequest - o corpo pode assumir qualquer tipo, no nosso caso definimos como JSON; ao utilizar esse formato com método POST os dados trafegados não aparecem na URI? Não exatamente. A única coisa que o POST faz é enviar os parâmetros no corpo da requisição. Se inspecionarmos a requisição, conseguimos acesso a eles. Se quisermos proteger, de fato, nossa aplicação, precisamos utilizar a "versão segura" do HTTP, o HTTPS. Com ela, conseguimos criptografar os dados enviados.
