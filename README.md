<h1 align="center">
  <img src="https://www.projectbuilder.com.br/wp-content/uploads/2022/06/blogpostimagem.png" alt="EBAC-SHOP" height="100" width="200">
  <br>
</h1>
 
<div style="display: flex; justify-content: center;">
<a href="https://github.com/GustavoAvila123/desafio-api-QA.git"><img src="https://img.shields.io/badge/-GITHUB-0b6baa?style=for-the-badge&logo=github&logoColor=white" width="100" height="22" style="margin-right: 5px;"/></a>
<a href="https://serverest.dev/"><img src="https://img.shields.io/badge/-Swagger UI-004d40?style=for-the-badge&logo=internet-explorer&logoColor=white" width="100" height="22" style="margin-right: 5px;"/></a>
</div>
 
---
 
<h4 align="center" style="color: white; font-size: 20px;">
  🚧 AUTOMAÇÃO DE TESTES | BACK-END 🚧
</h4>
 
---
 
## <font color="white">💻 SOBRE O PROJETO</font>
 
<p style="color: white;">O projeto consiste em uma suíte abrangente de testes automatizados para assegurar a funcionalidade e a integridade da API Serverest, disponibilizada via Swagger.</strong><br>

Ele cobre diversos cenários, desde a criação e autenticação de usuários até a validação de respostas e mensagens de erro, garantindo que todos os endpoints se comportem conforme esperado.<br>

<strong>A estrutura dos testes segue uma abordagem detalhista,</strong> visando verificar cada aspecto da API, incluindo tempos de resposta, status codes e consistência dos dados, com o objetivo de manter um serviço confiável e robusto.<br>

O Serverest busca oferecer uma experiência <strong>SEGURA</strong> e previsível aos usuários da API, e este projeto de testes contribui diretamente para alcançar essa excelência.</p>
 
---
 
## <font color="white">🛠️ TECNOLOGIAS UTILIZADAS</font>
 
<font color="white">O projeto foi desenvolvido utilizando as seguintes tecnologias:</font>
 
- [<span style="color: #0b6baa;">Postman</span>](https://www.postman.com/)
- [<span style="color: #0b6baa;">VS Code</span>](https://code.visualstudio.com/)
 
<font color="white">Além disso, temos as seguintes dependências:</font>
 
- [<span style="color: #0b6baa;">Newman</span>](https://www.npmjs.com/package/newman)
 
---
 
## <font color="white">📂 COMO BAIXAR O PROJETO</font>
 
<pre>
<code class="language-bash">
<span style="color: #963d8f;"># Clonar o repositório</span>
$ https://github.com/GustavoAvila123/desafio-api-QA.git
 
<span style="color: #963d8f;"># Instalar o Newman</span>
$ npm install -g newman
 
<span style="color: #963d8f;"># Instalando extensão de Geração de Relatórios em HTML</span>
$ nnpm install -g newman-reporter-htmlextra

</code>
</pre>

---
 
## <font color="white">📂 COMO EXECUTAR O PROJETO</font>
 
<pre>
<code class="language-bash">
<span style="color: #963d8f;"># Execução o Newman</span>
$ newman run Postman-files/collection.json -e Postman-files/environment.json
 
<span style="color: #963d8f;"># Executando o reports</span>
$ newman run Postman-files/collection.json -e Postman-files/environment.json -r htmlextra

</code>
</pre>
 
## <font color="white">📝 RESUMO DA ESTRUTURA</font>
  
<p style="color: #FFFFFF;">
    ⚪ NEWMAN:<br>
    <font color="#0b6baa">&#10004;</font> Onde armazenamos a execução da nossa automação.<br>
</p>

<p style="color: #FFFFFF;">
    ⏯️ POSTMAN FILES:<br>
    <font color="#0b6baa">&#10004;</font> collection: Armazena todos os nossos testes referente aos ENDPOINTS DA API.<br>
    <font color="#0b6baa">&#10004;</font> enviroment: Armazena todas as nossas variáveis de ambientes.<br>
</p>
 
## <font color="white">🔍 OVERVIEW DOS TESTES</font>
<p style="color: #FFFFFF;">
    <strong style="color: #0b6baa;">🌟 SERVEREST:</strong><br>
 
<p style="color: #FFFFFF;">
<div style="display: flex; justify-content: left;">
<a href=""><img src="https://img.shields.io/badge/-POST Usuários-49cc90?style=for-the-badge&logo=internet-explorer&logoColor=white" width="100" height="22" style="margin-right: 5px;"/></a>
</div>
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 1</strong> - Cadastrar Usuário, os testes verificam se o tempo de resposta da API é inferior a 1000 ms, garantindo desempenho adequado; checam se o status code está entre 200 e 299 e especificamente se é “Created”, assegurando que a criação foi bem-sucedida; validam a mensagem de sucesso retornada para confirmar que o fluxo de cadastro ocorreu conforme esperado; e, finalmente, armazenam o ID do usuário criado em uma variável de ambiente, permitindo reuso em etapas posteriores.
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 2</strong> - Usuário Já Existente, os testes novamente medem o tempo de resposta, conferem que o status code está entre 400 e 499 e especificamente se é “Bad Request”, além de validar a mensagem de erro “Este email já está sendo usado”, garantindo que a API trata corretamente tentativas de cadastro duplicado.
    </p>
<p style="color: #FFFFFF;">
<div style="display: flex; justify-content: left;">
<a href=""><img src="https://img.shields.io/badge/-POST Login-49cc90?style=for-the-badge&logo=internet-explorer&logoColor=white" width="100" height="22" style="margin-right: 5px;"/></a>
</div>
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 3</strong> - Realizar Login, os testes verificam o tempo de resposta e se o status code está entre 200 e 299, validam que o código é “OK”, conferem a mensagem de sucesso do login, verificam se o campo authorization existe e começa com “Bearer” para garantir que o token foi emitido corretamente, e armazenam esse token em uma variável de ambiente, permitindo que ele seja utilizado em chamadas autenticadas subsequentes. Em conjunto, esses testes asseguram não apenas a funcionalidade básica da API, mas também a consistência das respostas, a performance, a segurança do login e a correta gestão de dados duplicados.
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 4</strong> - Logando com Senha Inválida tem como objetivo testar a resposta da API quando o usuário tenta realizar login utilizando uma senha incorreta. Primeiramente, o teste verifica se o tempo de resposta é inferior a 1000 ms, garantindo que a API responda rapidamente mesmo diante de tentativas de autenticação inválidas. Em seguida, confirma que o código de status retornado está entre 400 e 499, sendo especificamente “Unauthorized” (401), assegurando que a API impede o acesso não autorizado. Por fim, o teste valida a mensagem de erro retornada, garantindo que informe de forma clara que a senha ou e-mail fornecido é inválido, contribuindo para uma experiência de usuário consistente e segura.
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 5</strong> - Logando com Email Inválido verifica o comportamento da API quando o login é realizado com um e-mail inexistente ou incorreto. O teste primeiramente confirma que o tempo de resposta permanece abaixo de 1000 ms, garantindo desempenho adequado. Em seguida, valida que o código de status está dentro da faixa de erro do cliente (400–499), especificamente “Unauthorized” (401), reforçando a proteção contra acessos indevidos. Por fim, o teste checa a mensagem de erro retornada, assegurando que informe corretamente que o e-mail e/ou a senha são inválidos, promovendo transparência na comunicação e garantindo que o sistema responda de forma consistente a credenciais incorretas.
<div style="display: flex; justify-content: left;">
<a href=""><img src="https://img.shields.io/badge/-GET Produtos-61affe?style=for-the-badge&logo=internet-explorer&logoColor=white" width="100" height="22" style="margin-right: 5px;"/></a>
</div>
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 6</strong> - Lista de Produtos Cadastrados tem como objetivo validar a resposta da API ao solicitar a lista completa de produtos disponíveis. O teste assegura que o tempo de resposta seja inferior a 1000 ms, garantindo desempenho adequado, e verifica que o código de status esteja entre 200 e 299, especificamente “OK”, confirmando que a requisição foi bem-sucedida. Além disso, valida a presença dos campos quantidade e produtos, assegurando que a estrutura do retorno esteja correta, e que o valor de quantidade corresponda ao número real de produtos listados. Cada produto é verificado quanto à existência de campos essenciais como nome, preco, descricao, quantidade e _id. Por fim, o teste identifica um produto específico, “Samsung 60 polegadas”, e salva seu _id para uso em testes subsequentes, garantindo rastreabilidade e consistência de dados entre etapas.
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 7</strong> - Lista de Produto ID valida o retorno da API ao consultar um produto específico pelo seu _id. O teste verifica que o tempo de resposta permaneça abaixo de 1000 ms e que o código de status esteja entre 200 e 299, sendo “OK”. Confirma a presença do campo quantidade e do _id no retorno, garantindo que a estrutura da resposta esteja correta. Além disso, valida que o _id retornado corresponde ao produto previamente salvo no Passo 6, assegurando consistência de dados, e que o nome do produto seja exatamente “Samsung 60 polegadas”, garantindo que a API retorne informações corretas e específicas para cada item consultado.
<div style="display: flex; justify-content: left;">
<a href=""><img src="https://img.shields.io/badge/-GET Carrinho-61affe?style=for-the-badge&logo=internet-explorer&logoColor=white" width="100" height="22" style="margin-right: 5px;"/></a>
</div>
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 8</strong> - Cadastro de Carrinho realiza a validação do processo de criação de um novo carrinho de compras na API. O teste verifica que o tempo de resposta é inferior a 1000 ms, garantindo desempenho adequado, e que o código de status está entre 200 e 299, especificamente “Created”, confirmando que a requisição foi bem-sucedida e que o recurso foi criado corretamente. Ele valida a existência do campo _id no retorno, assegurando que o carrinho foi registrado com sucesso, e também verifica a mensagem de sucesso “Cadastro realizado com sucesso”, garantindo que a API esteja comunicando corretamente o resultado da operação. Além disso, este teste utiliza o _id do produto previamente salvo, garantindo a consistência de dados e integridade da sequência de testes.
<div style="display: flex; justify-content: left;">
<a href=""><img src="https://img.shields.io/badge/-DEL Carrinho-f93e3e?style=for-the-badge&logo=internet-explorer&logoColor=white" width="100" height="22" style="margin-right: 5px;"/></a>
</div>
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 9</strong> - Cancelar Compra valida o processo de cancelamento de um carrinho de compras na API, assegurando que o tempo de resposta seja inferior a 1000 ms, garantindo desempenho rápido, e que o código de status esteja entre 200 e 299, especificamente “OK”, confirmando que a operação foi bem-sucedida. O teste também verifica a mensagem de sucesso “Registro excluído com sucesso. Estoque dos produtos reabastecido”, garantindo que a API esteja corretamente revertendo o carrinho e ajustando o estoque dos produtos, mantendo a integridade dos dados do sistema.
<div style="display: flex; justify-content: left;">
<a href=""><img src="https://img.shields.io/badge/-DEL Usuários-f93e3e?style=for-the-badge&logo=internet-explorer&logoColor=white" width="100" height="22" style="margin-right: 5px;"/></a>
</div>
    </p>
    <p style="text-align: justify; margin-left: 50px;">
    <strong>Passo 10</strong> - Excluindo Usuário Gerado realiza a validação da remoção de um usuário previamente criado na aplicação. Ele verifica que o tempo de resposta está abaixo de 1000 ms e que o status code retornado está entre 200 e 299, especificamente “OK”, confirmando que a exclusão foi executada corretamente. Além disso, o teste valida a mensagem de sucesso “Registro excluído com sucesso”, garantindo que a API confirme a operação e que não haja dados residuais do usuário, mantendo a consistência do ambiente de testes e prevenindo impactos em execuções futuras.
</p>
 
<h2 style="color: white;">✍ AUTOR</h2>
 
  <table>
  <tr>
          <td align="center">
      <a href="https://serverest.dev/">
        <img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/132934043?s=400&u=d70e99353630191829cdfbc95f9f48c0a66299e8&v=4" width="100px;" alt=""/>
        <br />
         <sub style="color: white;"><b>Gustavo Ávila</b></sub>
      </a>
      <br />
      <a title="SERVEREST"><sub style="color: white;"><b>Analista de Qualidade<b></a>
      <br/>
      <br/>
      <a href="mailto:gustavotoiansk@icloud.com">
        <img src="https://img.shields.io/badge/-gustavotoiansk@icloud.com-0b6baa?style=flat-square&logo=Gmail&logoColor=white" alt=""/>
      </a>
    </td>
  </tr>
</table>