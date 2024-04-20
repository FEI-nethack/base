# Nethack Learning Environment - Base

Este repositório contém a base para a configuração do ambiente que será utilizado para o desenvolvimento do projeto. Ele possui apenas algumas formas de instalação do que é necessário, mas não contém nenhuma informação sobre as pesquisas realizadas sobre o ambiente

# Uso do docker
Para criar a imagem:
```shell
docker build -t nle .
```
## Abrir python no docker depois de buildado
1)Abrir o container
```
docker run -it --rm nle bash
```
1.1)Abrir container com os arquivos alocados na pasta "nle"
```
docker run --rm -it -v $(pwd):/nle nle bash
```

2)abrir o conda environment no container
```
conda activate nle
```

Agora você esta dentro do ambiente conda que está com o nle e minihack instalado basta usar  ```python``` para abrir o terminal do python.


## Criação de ambiente Conda (miniconda3)
Usando o arquivo [environment.yml](environment.yml) (consultar [Explicação Environment](Documentação/environment.md)) é possível criar um ambiente padronizado no anaconda, com o seguinte comando:

```
conda env create -f environment.yml 
```



