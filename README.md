# Classificação de Pokemons da Primeira Geração 

Este projeto consiste no desenvolvimento de um sistema de classificação multiclasse de granularidade fina para identificar as 151 espécies de Pokémon da Primeira Geração, utilizando técnicas avançadas de Visão Computacional e Deep Learning.

O trabalho foi desenvolvido para a disciplina de **Tópicos Especiais em Matemática Aplicada (Deep Learning)** na **FCTE/UnB**.

---

## Apresentação do Projeto
Assista ao vídeo explicativo com os detalhes da implementação e demonstração dos resultados:
[Link para o vídeo no YouTube](https://youtu.be/g1IpM8G3unE)

---

## Resumo do Projeto

O desafio central foi processar um dataset de mais de 10.000 imagens com alta variabilidade visual. A solução utilizou **Transfer Learning** e **Fine-Tuning** sobre a arquitetura **ResNet18**, alcançando excelentes métricas de generalização.

### Estrutura do Pipeline:
1.  **Preparação de Dados:** Uso de Data Augmentation (rotação, flip horizontal, brilho/contraste) para aumentar a robustez.
2.  **Arquitetura:** Modelo ResNet18 pré-treinado no ImageNet, adaptado para 150 classes específicas.
3.  **Otimização:** Uso do otimizador Adam com taxa de aprendizado controlada e função de perda CrossEntropyLoss.
4.  **Inferência Real:** Implementação de um critério de confiança (threshold) para detectar imagens que não pertencem ao domínio (não-Pokémon).

---

## Resultados Obtidos

O modelo demonstrou um aprendizado sólido e consistente, conforme as métricas abaixo:

| Métrica | Resultado |
| :--- | :--- |
| **Acurácia Top-1** | **83.99%** |
| **Acurácia Top-5** | **96.81%** |

### Visualização de Performance
> **Dica:** Adicione aqui imagens dos seus gráficos gerados na Célula 6 e 7 (Loss/Accuracy e Matriz de Confusão).

---

## Tecnologias e Ferramentas

* **Linguagem:** Python 3
* **Deep Learning Framework:** PyTorch
* **Visão Computacional:** Torchvision, PIL (Pillow)
* **Análise de Dados:** NumPy, Pandas, Scikit-learn
* **Visualização:** Matplotlib, Seaborn
* **Dataset:** Kaggle (Pokemon Generation One)

---

## Autores (Equipe UnB)

* **Felipe Junior Duarte da Silva**
* **Rafael Welz Schadt**
* **Othavio Araujo Bolzan**
* **Professor:** Vinicius Rispoli

---

## Como Executar
1. Abra o arquivo `.ipynb` no Google Colab.
2. Certifique-se de ativar a GPU em `Ambiente de Execução > Alterar tipo de ambiente de execução > GPU`.
3. Execute as células em ordem para baixar o dataset via `kagglehub` e iniciar o treinamento/avaliação.
