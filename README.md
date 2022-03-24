# Docker Studies

<hr/>

## CMD vs RUN

| CMD                                                                                     | RUN                                   |
| --------------------------------------------------------------------------------------- | ------------------------------------- |
| Runtime                                                                                 | Buildtime / Compilação                |
| Executa comandos em contêineres durante a inicialização                                 | Compila e adiciona camadas às imagens |
| Equivalente à `docker run <argumentos> <comando>` / `docker run <argumentos> /bin/bash` | Usado pra instalar aplicações         |
| Somente um por Dockerfile                                                               | Vários por Dockerfile                 |

| Shell Form                                                     | Exec Form                                            |
| -------------------------------------------------------------- | ---------------------------------------------------- |
| Comandos são expressos da mesma forma que os comandos de shell | JSON Array style `["command", "arg1"]`               |
| Os comandos são apendados com: `/bin/sh -c`                    | Contêineres não precisam de shell                    |
| Expansão de variáveis                                          | Sem funcionalidades de Shell                         |
|                                                                | Garante que a string não seja sobrescrita pelo Shell |
