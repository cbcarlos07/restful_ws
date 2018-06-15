#  Comandos da `Série de cursos de Node JS`

Link para a play list criada: [Aqui](https://www.youtube.com/playlist?list=PLGuGdcwBzUZt10zvj6_xuDeasOnXdWWnx)

Aula ministrada por [Fábio Vedovelli](https://www.youtube.com/channel/UC1PUtdA_NktdtmRpF_UGG_w)

* > npm init -y

Gerar package.json

* >npm i restify eslint --save-dev
 
 Para instalar o eslint com restify
 
 **Restify** vai provar as rotas
 
 * >./node_modules/.bin/eslint --init
 
 Inicializar o ESLint escolher a opçao 
   * Usar Guia de estilo popular ( Use a popular style guide )
   
   Escolhe a opção Standar

* >./node_modules/.bin/eslint src/index.js

Verificar arquivo com eslint
   
* >npm run dev  

  Serve para rodar aplicação

* >npm i -g nodemon

Reiniciar o serviço em cada alteração do projeto

Alterar na linha

     "dev": "node src/index.js"
     
  Para
  
     "dev": "nodemon src/index.js" 

* > nodemon src/index.js

Para ficar rodando e mostrar alterção sempre que salvar ou qualquer momento rodar o comanso rs e dar enter

* > rs

Reinicar o nodemon
    
* > npm i
  
  Serve para instalar dependências do node
  
 * >npm test 
 
 Serve rodar arquivo de teste da aplicação
 
 
 
 * >npm test -- --watch 
 
 Serve para ficar rodando testes em tempo real
 
  
    
 
 * >npm i --save-dev sha1
 
 Serve para instalar a criptografia sha1
 
 Usa-se assim:
   > const sha1 = require('sha1')

   
* >npm i --save-dev jsonwebtoken

Retornar um token para login e senha

Usa-se assim:
> const jwt = require('jsonwebtoken')

>  const token = jwt.sign({email, id}, 'macarrão', { expiresIn: 60 * 60 * 24 })

### Ubuntu

Liberar porta no Ubuntu no terminal no firewal

>$ ufw allow 3456

Verificar status de porta 

>$ ufw status

Executar aplicação

>$ node src/index.js

Instalar pm2 para deixar aplicação disponível no servidor

>$ npm i -g pm2

Rodar aplicação

>$ NODE_ENV=production pm2 start src/index.js --name=RESTFUL

Criar subdomínio nginx

    server{
       listen 80
       server_name restful.nomedodominio.com.br www.restful.nomedodominio.com.br;
       access_log /var/log/ngix/restful.nomedodominio.com.br;
       location / {
          proxy_set_header X-Real-IP $remover_addre;
          proxy_set_header HOST $http_host;
          proxy_set_header X-NgiX-Proxy true;`
     
          proxy_pass http://127.0.0.1:3456;
          proxy_redirect off;
        } 
    }

Criar na pasta do servidor

> vi /etc/nginx/sites-available/restful.nomedodominio.com.br

Avessar a pasta e criar link simbolico

>cd /etc/ngix/sites-enabled/

>ln -s ../etc/nginx/sites-available/restful.nomedodominio.com.br

Reinicar servico web nginx

>service nginx reload

## JWT
https://jwt.io/ 

Para arquivo base64 gerado


## SHA1 Online
http://www.sha1-online.com/ 

Para gerar uma string do tipo sha1 criptografada
