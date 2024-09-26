# Nethack Learning Environment - Base

Este repositório contém a base para a configuração do ambiente que será utilizado para o desenvolvimento do projeto. Ele possui apenas algumas formas de instalação do que é necessário, mas não contém nenhuma informação sobre as pesquisas realizadas sobre o ambiente

# Uso pelo docker <img align="left" alt="Docker" width="40px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original-wordmark.svg" />
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
O código acima pode não funcionar as vezes, Quando for o caso, usar o código abaixo:
```
docker run --rm -it -v "$(pwd):/nle" nle bash
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

# Uso da instalação direta pelo Linux <img align="left" alt="Linux" width="50px" style="padding-right:10px;" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" />

## 1. Instalar Python 3 e Pip
  ```  
  sudo add-apt-repository ppa:deadsnakes/ppa
  sudo apt update
  sudo apt install python3
  sudo apt install python3.10
  python3 --version
    
  sudo apt install -y python3-pip
  python3 --version
  ```
## 2. Instalar Miniconda (baixar o .sh do site do miniconda) 
  ```bash
  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O /opt/miniconda-installer.sh
  #ignorar a primeira linha acima caso ja tenha baixado o .sh do site
  bash /opt/miniconda-installer.sh #(COLOCAR O LOCAL DO INSTALADOR BAIXADO)
  ```  
## 3. Ambiente conda e git
  ```
  conda create -n minihack python=3.8
  conda activate minihack
  sudo apt update
  sudo apt install git
  git --version
  ```
## 4. Pacotes
  ```
  sudo apt install cmake
  cmake --version

  sudo apt install libbz2-dev
  sudo apt install bison flex
  ```
## 5. Instação NLE e Minihack
  ```
  pip install nle
  pip install minihack
  ```

