# 🧠 Retinografia AI – Diagnóstico Precoce de Glaucoma com Deep Learning

## 📌 Sobre o Projeto

O **Retinografia AI** é um sistema de **visão computacional aplicado à saúde ocular**, desenvolvido inicialmente como Trabalho de Conclusão de Curso em Engenharia da Computação. O objetivo é **detectar precocemente o glaucoma** em imagens de fundo de olho (retinografia) usando **redes neurais convolucionais (CNNs)** e técnicas modernas de **aprendizado profundo**.

O projeto foi expandido para evoluir de protótipo acadêmico para uma **solução prática e escalável**, capaz de apoiar médicos, clínicas e comunidades em exames rápidos, acessíveis e de baixo custo.

---

## 🚨 Por que Glaucoma?

* O glaucoma é uma das **principais causas de cegueira no mundo**, afetando mais de 80 milhões de pessoas.
* A **detecção precoce** é fundamental para preservar a visão, mas os métodos tradicionais são caros, demorados e sujeitos a erros manuais.
* Uma solução automática baseada em IA pode aumentar a **precisão, acessibilidade e rapidez** no diagnóstico.

---

## ⚙️ Tecnologias Utilizadas

* **Linguagem:** Python 3.x
* **Deep Learning:** TensorFlow / Keras (CNNs – ResNet, DenseNet, GoogLeNet, EfficientNet etc.)
* **Visão Computacional:** OpenCV
* **Análise de Dados:** NumPy, Pandas, Matplotlib, Seaborn
* **Avaliação de Modelos:** Scikit-learn (matriz de confusão, ROC, F1-score etc.)

---

## 📂 Estrutura do Projeto

```
retinografia-master/
│── data/                # Datasets (REFUGE, ORIGA, G1020)
│── notebooks/           # Experimentos em Jupyter
│── src/
│   ├── preprocessing/   # Pré-processamento e segmentação das imagens
│   ├── models/          # Implementação das CNNs e arquiteturas testadas
│   ├── training/        # Scripts de treinamento com validação cruzada
│   ├── inference/       # Pipeline de inferência (classificação em imagens novas)
│   └── evaluation/      # Geração de métricas e relatórios
│── results/             # Resultados experimentais (gráficos, matrizes de confusão)
│── requirements.txt     # Dependências
│── README.md            # Documentação
```

---

## 📊 Metodologia

1. **Datasets usados:**

   * **REFUGE** – Imagens de fundo de olho em alta resolução.
   * **ORIGA** – Repositório público para análise de glaucoma.
   * **G1020** – Conjunto com 1020 imagens rotuladas (glaucoma vs normal).

2. **Divisão dos dados:**

   * Treinamento: 60%
   * Validação: 20%
   * Teste: 20%

3. **Modelos testados:**

   * ResNet, DenseNet, GoogLeNet, MobileNet, EfficientNet, VGG, AlexNet, SENet, Xception, SqueezeNet.

4. **Métricas utilizadas:**

   * **Acurácia**
   * **Precisão**
   * **Recall**
   * **F1-Score**
   * **Curvas ROC/PR**

---

## 📈 Resultados

* Os modelos que apresentaram **melhor desempenho** foram:

  * **DenseNet** → robustez contra overfitting e boa generalização.
  * **ResNet** → equilíbrio entre profundidade e precisão.
  * **GoogLeNet** → adaptação eficiente a diferentes variações de imagens.

* Desafios encontrados:

  * Desbalanceamento de classes (poucos casos positivos de glaucoma).
  * Overfitting em arquiteturas mais complexas.
  * Alto consumo de memória e tempo de treinamento.

---

## 🚀 Melhorias Futuras

* [ ] Implementar **mixed precision training** para acelerar e reduzir memória.
* [ ] Testar **modelos leves** (EfficientNetV2, MobileViT) para deploy em mobile/edge.
* [ ] Adicionar **Grad-CAM/LIME** para interpretabilidade clínica.
* [ ] Criar **API em FastAPI/Flask** para integração com sistemas de saúde.
* [ ] Expandir para **outras doenças oculares** (retinopatia diabética, catarata, degeneração macular).
* [ ] Disponibilizar modelo em **TensorFlow Lite/ONNX** para rodar em dispositivos portáteis.

---

## 🧪 Como Executar

1. Clone o repositório:

```bash
git clone https://github.com/usuario/retinografia-ai.git
cd retinografia-ai
```

2. Crie o ambiente virtual e instale dependências:

```bash
python3 -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
pip install -r requirements.txt
```

3. Execute o treinamento:

```bash
python src/training/train.py --dataset REFUGE --model ResNet
```

4. Realize uma inferência em nova imagem:

```bash
python src/inference/predict.py --image exemplo.jpg
```

---

## 👨‍💻 Autores

* João Lucas Bueno da Silva Pinheiro ([joaobuenopinheiro@gmail.com](mailto:joaobuenopinheiro@gmail.com))
* Kevin Nicolas Costantino
* Orientador: Dr. Hemerson Pistori

---

## 📜 Licença

Este projeto é de uso acadêmico e de pesquisa. Para fins comerciais, entre em contato com os autores.

---
