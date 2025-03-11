📌 `visao_computacional/tensorflow.md`

# TensorFlow

## 🔹 Descrição
TensorFlow é uma plataforma de aprendizado profundo desenvolvida pelo Google. Ela é amplamente utilizada para construir e treinar modelos de IA, incluindo tarefas de visão computacional.

## 🚀 Funcionalidades
- **Treinamento de modelos de aprendizado profundo**
- **Classificação e detecção de objetos**
- **Segmentação de imagens**
- **Análise de vídeo**
- **Suporte a redes neurais convolucionais (CNNs)**

## 📦 Instalação
Para instalar o TensorFlow, utilize o seguinte comando:

```bash
pip install tensorflow
```

## 🛠️ Exemplo de Utilização via API
Aqui está um exemplo de como usar TensorFlow para classificar imagens:

```python
import tensorflow as tf
from tensorflow.keras import datasets, layers, models

# Carregar dados de exemplo
(train_images, train_labels), (test_images, test_labels) = datasets.cifar10.load_data()

# Normalizar dados
train_images, test_images = train_images / 255.0, test_images / 255.0

# Construir modelo
model = models.Sequential([
    layers.Conv2D(32, (3, 3), activation='relu', input_shape=(32, 32, 3)),
    layers.MaxPooling2D((2, 2)),
    layers.Conv2D(64, (3, 3), activation='relu'),
    layers.MaxPooling2D((2, 2)),
    layers.Conv2D(64, (3, 3), activation='relu'),
    layers.Flatten(),
    layers.Dense(64, activation='relu'),
    layers.Dense(10)
])

# Compilar e treinar modelo
model.compile(optimizer='adam',
              loss=tf.keras.losses.SparseCategoricalCrossentropy(from_logits=True),
              metrics=['accuracy'])

model.fit(train_images, train_labels, epochs=10, 
          validation_data=(test_images, test_labels))

# Avaliar modelo
test_loss, test_acc = model.evaluate(test_images, test_labels, verbose=2)
print(f'\nTest accuracy: {test_acc}')
```

## 🔗 Ligações
- Site Oficial
- Documentação

