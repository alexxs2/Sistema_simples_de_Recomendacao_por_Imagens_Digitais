# Sistema de Recomendação por Similaridade de Imagens

Neste projeto, desenvolvi um sistema simples de recomendação de produtos de moda baseado em visão computacional. A seguir, destaco os principais pontos:

## 1. Dataset  
- **Fashion-MNIST** (Keras): 70 000 imagens em tons de cinza, 28×28 px, distribuídas em 10 classes de vestuário.

## 2. Arquitetura da Rede  
- CNN leve “manual” de três blocos **Conv → ReLU → MaxPool**.  
- Camada densa final para gerar um **embedding** de 128 dimensões.

## 3. Indexação de Features  
- Após o treinamento, extraí os embeddings de todo o conjunto de treino.  
- Esses vetores compõem o índice de características para as comparações.

## 4. Métrica de Similaridade  
- **Similaridade de cosseno** (scikit-learn) entre embeddings.  
- Para cada imagem de teste, o sistema retorna as N imagens de treino mais similares como visto abaixo no resultado:
  
  <img width="1489" height="295" alt="image" src="https://github.com/user-attachments/assets/52d4b3fc-73ed-4202-aba4-20b9b645d125" />


## 5. Motivação e Trade-offs  
- Optei por uma CNN pequena e treinada do zero devido às **restrições de tempo e recursos** no Colab.  
- Estudei arquiteturas mais robustas, como **ResNet-50**, mas elas exigem maior poder computacional e tempo de treinamento.

## 6. Resultados  
- O sistema exibe, para cada consulta, as 5 imagens de moda mais semelhantes, facilitando na recomendação de produtos semelhantes.  
- Há margem para melhorias, como otimização de hiperparâmetros, uso de modelos pré-treinados e técnicas de compressão, porém a ideia eu consegui entender bem.

---
