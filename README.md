# Nethack Learning Environment - Base

Este repositório contém a base para a configuração do ambiente que será utilizado para o desenvolvimento do projeto. Ele possui apenas algumas formas de instalação do que é necessário, mas não contém nenhuma informação sobre as pesquisas realizadas sobre o ambiente

## Uso do docker
Para criar a imagem:
```shell
docker build -t nle .
```

## Criação de ambiente Conda (miniconda3)
Usando o arquivo [environment.yml](environment.yml) (consultar [Explicação Environment](Documentação/environment.md)) é possível criar um ambiente padronizado no anaconda, com o seguinte comando:

```
conda env create -f environment.yml 
```

=======


