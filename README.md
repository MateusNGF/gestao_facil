



# CRIAR USUARIO MONGO (AS VARIAVEIS INIT_MONGO N ESTA FUNCIONANDO)
Passo a passo para realizar deploy.

1. Primeiro comando: `docker compose -f docker-compose.yml up -d --build`
2. Segundo comando: `docker compose -f docker-compose.app.yml -d --build`

> Verifique se todos os serviços estão funcionando.

Agora, devemos adicionar o usuario admin no mongo (Note que o nome do banco pode variar )
3. `docker exec -it gestao_facil-mongodb-1 mongosh --eval 'db.getSiblingDB("admin").createUser({ user: "admin", pwd: "admin", roles: [{ role: "root", db: "admin" }] })'`

> Agora precisamos rodas as seeds, teremos que entrar em cada container e executar o seguinte comando:
4. `npm run prisma:seed`


Quando realizarmos