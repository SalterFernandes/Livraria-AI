📌 `imagem/deep-dream.md`  

# Deep Dream

## 🔹 Descrição
Deep Dream é uma ferramenta de inteligência artificial desenvolvida pela Google para transformar imagens comuns em criações artísticas psicodélicas. Utilizando redes neurais convolucionais, o modelo realça padrões e formas ocultas nas imagens, gerando efeitos únicos.

## 🚀 Funcionalidades
- **Transformação de imagens com efeitos psicodélicos**  
- **Geração de arte baseada em redes neurais**  
- **Ajuste de intensidade e estilo da transformação**  
- **Suporte para diversas resoluções de imagem**  

## 📦 Acesso
Deep Dream pode ser acessado via navegador ou implementado com TensorFlow.

🔗 [Experimente Online](https://deepdreamgenerator.com/)

## 🛠️ Exemplo de Utilização via Código
```python
import tensorflow as tf
import numpy as np
import PIL.Image

# Carregar imagem
def load_image(path):
    img = PIL.Image.open(path)
    img = np.array(img).astype(np.float32) / 255.0
    return img

# Aplicar Deep Dream
def deep_dream(image):
    model = tf.keras.applications.InceptionV3(include_top=False, weights='imagenet')
    dream_image = model(image)
    return dream_image

img = load_image("minha_imagem.jpg")
dreamed_img = deep_dream(img)
```

## 🔗 Ligações
- [Site Oficial](https://deepdreamgenerator.com/)  
- [Repositório no GitHub](https://github.com/google/deepdream)  
- [Documentação TensorFlow](https://www.tensorflow.org/tutorials/generative/deepdream)  

---

## 🌟 Como Contribuir
1. Faça um **fork** do repositório.  
2. Crie um **branch** para a sua ferramenta: `git checkout -b minha-ferramenta`.  
3. Adicione um arquivo `.md` na categoria correta.  
4. Envie um **Pull Request**. 🎉  

## 📜 Licença
Este repositório está licenciado sob a **Licença Apache 2.0** (uso sujeito às diretrizes do Google).  