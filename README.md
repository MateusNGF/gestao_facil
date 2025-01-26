



# CRIAR USUARIO MONGO (AS VARIAVEIS INIT_MONGO N ESTA FUNCIONANDO)

> rodar esse comando: 
`docker exec -it gestao_facil-mongodb-1 mongosh --eval 'db.getSiblingDB("admin").createUser({ user: "admin", pwd: "senha_forte", roles: [{ role: "root", db: "admin" }] })'`
