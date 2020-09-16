** Aviso! ** A otimização pode não convergir em algumas GPUs. Nós pessoalmente enfrentamos problemas nas GPUs Tesla V100 e P40. Ao executar o código, certifique-se de obter resultados semelhantes aos do papel primeiro. Mais fácil de verificar usando o bloco de notas com pintura de texto. Tente definir o modo de precisão dupla ou desligar o cudnn.

# Recuperação de Fotografias

Notebooks Jupyter com código python para recuperar fotografias:

Projeto de 2018 original:
> **Deep Image Prior**

> CVPR 2018

> Dmitry Ulyanov, Andrea Vedaldi, Victor Lempitsky


[[paper]](https://sites.skoltech.ru/app/data/uploads/sites/25/2018/04/deep_image_prior.pdf) [[supmat]](https://box.skoltech.ru/index.php/s/ib52BOoV58ztuPM) [[project page]](https://dmitryulyanov.github.io/deep_image_prior)

![](data/teaser_compiled.jpg)

Aqui nós fornecemos hiperparâmetros e arquiteturas, que foram usados para gerar as figuras. A maioria deles está longe de ser ideal. Não hesite em alterá-los e ver o efeito.

Expandiremos este README com uma lista de hiperparâmetros e opções em breve.

# Instalação:

### se você não tem GPU (placa de vídeo) em sua máquina

no linux
```bash
export CUDA_VISIBLE_DEVICES=""
```
no windows
```cmd
set CUDA_VISIBLE_DEVICES=""
```

### Dependências

Aqui está a lista de bibliotecas que você precisa instalar para executar o código:
- python = 3.6
- [pytorch](http://pytorch.org/) = 0.4
- numpy
- scipy
- matplotlib
- scikit-image
- jupyter


Todos estes pacotes podem ser instalados através do sistema anaconda: `conda` (`anaconda`), e.g.
```
conda install jupyter
```


ou crie um env conda com todas as dependências via arquivo de ambiente

```
conda env create -f environment.yml
```

## Imagem usando o Docker

Como alternativa, você pode usar uma imagem Docker que expõe um Notebook Jupyter com todas as dependências necessárias. Para construir esta imagem, certifique-se de ter o [docker] (https://www.docker.com/) e [nvidia-docker] (https://github.com/NVIDIA/nvidia-docker) instalados e, em seguida, execute

```
nvidia-docker build -t deep-image-prior .
```

Após a construção, você pode iniciar o contêiner como

```
nvidia-docker run --rm -it --ipc=host -p 8888:8888 deep-image-prior
```

você receberá uma URL por meio da qual pode se conectar ao bloco de notas Jupyter.

## Google Colab

Para executá-lo usando o Google Colab, clique [aqui] (https://colab.research.google.com/github/DmitryUlyanov/deep-image-prior) e selecione o bloco de notas a ser executado. Lembre-se de descomentar a primeira célula para clonar o repositório no ambiente do colab.


# Como citar o trabalho do pessoal do **Deep Image Prior** no Latex
```
@article{UlyanovVL17,
    author    = {Ulyanov, Dmitry and Vedaldi, Andrea and Lempitsky, Victor},
    title     = {Deep Image Prior},
    journal   = {arXiv:1711.10925},
    year      = {2017}
}
```
