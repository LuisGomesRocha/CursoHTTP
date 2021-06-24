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


<p align="justify"> :robot: Para o processo de cadastro temos duas opções de verbos HTTP para utilziar sendo elas GET e POST. Quando utilizamos o GET, os parâmetros são passados no cabeçalho da requisição. Por isso, podem ser vistos pela URI, sendo esse verbo o padrão para enviar dados quando submetemos um formulário HTTP, podendo alterar alterar esse comportamento dizendo para o formulário qual do método (method) ele deve usar.  :robot: </p>

<p align="justify"> :robot: No caso de formulários web, é muito comum que esse método seja o POST, tendo esse como caracteristica o envio dos parâmetros no corpo da requisição HTTP. Escondendo eles da URI. É pertinente salientar que se utilizarmos o método POST protegemos os dados submetidos pelo formulário, já que eles não aparecem na URI? Não exatamente. A única coisa que o POST faz é enviar os parâmetros no corpo da requisição. Se inspecionarmos a requisição, conseguimos acesso a eles.
  
  Se quisermos proteger, de fato, nossa aplicação, precisamos utilizar a "versão segura" do HTTP, o HTTPS. Com ela, conseguimos criptografar os dados enviados.

Ambos os verbos são muito utilizado em formulários na web e possuem algumas outras diferenças entre si.

Como o GET envia os dados no cabeçalho da requisição, ele tende a ser, não é uma regra,um pouco mais performático que o POST.

Porém, por enviar os dados no cabeçalho da requisição, o GET tem um tamanho máximo de dados que podem ser enviados, que no geral é de 255 caracteres. Com POST, podemos enviar informações um pouco maiores, como imagens. Ou seja, se tentarmos passar uma grande quantidade de informações via GET, algumas partes podem ser perdidas no caminho.

Com isso você pode estar pensando que utilizar o POST é o melhor caminho já que ele encapsula os dados no corpo da requisição e consegue transportar mais dados que o GET, portanto, vamos utilizar o POST em todo lugar.

Porém, se existem dois verbos diferentes, é porque eles foram feitos para serem utilizados em locais diferentes.

As requisições do tipo GET são recomendadas para obter dados de um determinado recurso. Como em um formulário de busca ou em uma listagem de todos os produtos cadastrados.

Já as requisições POST são mais utilizadas para para enviar informações para serem processadas, como por exemplo, criar algum recurso, como um produto, ou um cliente.
  
  :robot: </p>
