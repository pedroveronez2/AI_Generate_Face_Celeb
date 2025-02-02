# DCGAN - Gerando Imagens Falsas de Celebridades

Este projeto é uma implementação da Deep Convolutional Generative Adversarial Network (DCGAN) do zero, utilizando PyTorch para treinar um modelo capaz de gerar imagens falsas de celebridades.

## Fonte do Projeto
O projeto foi desenvolvido seguindo o passo a passo do vídeo do YouTube:
[Implementing DCGAN from Scratch](https://youtu.be/IZtv9s_Wx9I?list=PLhhyoLH6IjfwIp8bZnzX8QR30TRcHO8Va)

## Estrutura do Projeto
- `model.py`: Contém a implementação das redes **Discriminador** e **Gerador**.
- `train.py`: Responsável pelo treinamento do modelo, utilizando a base de dados CelebA.

## Como Funciona

### 1. Estrutura das Redes Neurais
O projeto implementa duas redes neurais:

#### Discriminador (`Discriminator`)
- Uma rede convolucional profunda que recebe uma imagem como entrada e tenta classificá-la como **real** ou **falsa**.
- Utiliza camadas convolucionais seguidas de funções de ativação `LeakyReLU` e uma camada final `Sigmoid`.

#### Gerador (`Generator`)
- Uma rede convolucional transposta que recebe um vetor de ruído como entrada e gera uma imagem falsa.
- Utiliza camadas `ConvTranspose2d` e `ReLU`, com uma camada final `Tanh` para normalizar os valores de saída.

### 2. Inicialização dos Pesos
Os pesos são inicializados de acordo com a recomendação do artigo original do DCGAN, utilizando uma distribuição normal com média 0 e desvio padrão 0.02.

### 3. Treinamento (`train.py`)
- O dataset CelebA é carregado e processado.
- Um ruído aleatório é passado pelo gerador para criar imagens sintéticas.
- O discriminador é treinado para distinguir entre imagens reais e geradas.
- O gerador é treinado para enganar o discriminador.
- Durante o treinamento, métricas são registradas e imagens geradas são salvas para visualização.

## Como Executar o Treinamento
### 1. Instalar Dependências
Certifique-se de ter o Python e PyTorch instalados. Depois, instale os pacotes necessários:
```bash
pip install torch torchvision tensorboard
```

### 2. Baixar e Preparar o Dataset
Baixe o dataset CelebA e extraia as imagens para a pasta `celeb_dataset` dentro do diretório do projeto.

### 3. Rodar o Treinamento
```bash
python train.py
```

Isso iniciará o treinamento e salvará as imagens geradas ao longo do tempo.

## Resultados
Após algumas épocas de treinamento, o gerador começa a produzir imagens realistas de rostos de celebridades. O progresso pode ser monitorado utilizando o TensorBoard:
```bash
tensorboard --logdir=logs
```

## Conclusão
Este projeto demonstra como construir e treinar uma DCGAN do zero para gerar imagens falsas realistas. O treinamento pode ser ajustado aumentando o número de épocas ou alterando os hiperparâmetros para obter melhores resultados.

---
Desenvolvido seguindo o tutorial do YouTube [Implementing DCGAN from Scratch](https://youtu.be/IZtv9s_Wx9I?list=PLhhyoLH6IjfwIp8bZnzX8QR30TRcHO8Va).

