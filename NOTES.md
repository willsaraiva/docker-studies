# Notes

## Iniciando com Docker

Aqui estão algumas anotações a respeito da minha apredizagem sobre o docker

### Alguns comandos importantes do Docker

- ps: lista todos os containers que estão rodando
```
docker ps 
```

- ps -a: lista todos os containers
```
docker ps -a
```

- start <nome_container>: starta um container que não está em execução.
```
docker start <nome_container>
```

- run -it <nome_container> bash: habilita o modo iterativo(-i) e modo para receber comandos(-t). Por fim, *bash* refere-se ao interpretador d shell que deseja executar dentro do container.
```
docker run -it <nome_container> bash
```

Caso eu deseje remover um container após sua execução parar, basta assinalar com *--rm*. Por exemplo:
```
docker run -it --rm <nome_container> bash
```

Como faço para realizar o mapeamento da porta do meu container para porta do meu host?
```
docker run -p <porta_host:porta_container> <nome_container> 
```

Como faço para o terminal não ficar travado no processo do container? O *-d* habilita o modo *detached*, que basicamente executa o container em segundo plano.
```
docker run -d <nome_container> 
```