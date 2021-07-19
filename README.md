# Guia graph-tool

Breves anotações do estudo da ferramenta [**graph-tool**](https://graph-tool.skewed.de/static/doc/index.html) para seu uso básico e entendimento de algumas de suas funcionalidades.

## Instalação do ambiente

A instalação da ferramenta é pouco diferente de soluções que utilizam simplesmente a linguagem Python, não havendo formas de realizar sua instalação somente com o gerenciador de pacotes _pip_.

É possível realizar a instalação da ferramenta em diferentes ambientes e/ou sistemas operacionais. Alguns exemplos são citados abaixo:

- MacOS
```bash
brew install graph-tool
```

- Ubuntu (bionic)
```bash
add-apt-repository "deb [ arch=amd64 ] https://downloads.skewed.de/apt bionic main"
apt-key adv --keyserver keys.openpgp.org --recv-key 612DEFB798507F25
apt-get update
apt-get install python3-graph-tool
```

- Arch Linux
```bash
pikaur -S python-graph-tool
```

- Gentoo Linux
```bash
emerge graph-tool
```

- Docker (Windows/Linux/MacOS)
```bash
docker pull tiagopeixoto/graph-tool
```

## Mecanismos alternativos

Foi adicionado um arquivo de _environment_ para instalação em ambientes que utilizem os gerenciador como o _conda_ e o _mamba_.
```bash
conda env create -f environment.yml
conda activate exemplo
```

Foram adicionados também dois arquivos para utilização do _Docker_ para que se produza uma imagem baseado em _Ubuntu (focal)_. Neste ambiente já se instalou o _graph-tool_ e outras ferramentas como o _Networkx_ e o _igraph_.

```bash
docker build -t ubuntu-tool -f files/ubuntu-focal.dck
docker run -itd --name ubuntu-graph -p 8888:8888 -v /home/ronaldoalves/Documentos/mestrado/aulas/:/home/user/labs ubuntu-tool 
```



