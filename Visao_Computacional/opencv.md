📌 `visao_computacional/opencv.md`

# OpenCV

## 🔹 Descrição
OpenCV (Open Source Computer Vision Library) é uma biblioteca de código aberto voltada para tarefas de visão computacional e processamento de imagem. Ela oferece uma ampla gama de algoritmos para análise de imagens e vídeos.

## 🚀 Funcionalidades
- **Processamento de imagem e vídeo**
- **Detecção e reconhecimento de objetos**
- **Análise de movimento**
- **Reconhecimento facial**
- **Integração com outras bibliotecas de aprendizado de máquina**

## 📦 Instalação
Para instalar o OpenCV, utilize o seguinte comando:

```bash
pip install opencv-python
```

## 🛠️ Exemplo de Utilização via API
OpenCV pode ser utilizado em diversos projetos de visão computacional. Aqui está um exemplo simples de detecção de bordas:

```python
import cv2
import numpy as np

# Carregar imagem
imagem = cv2.imread('imagem.jpg', 0)

# Aplicar detecção de bordas
bordas = cv2.Canny(imagem, 100, 200)

# Mostrar imagem original e com bordas
cv2.imshow('Imagem Original', imagem)
cv2.imshow('Bordas', bordas)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## 🔗 Ligações
- Site Oficial
- Documentação
