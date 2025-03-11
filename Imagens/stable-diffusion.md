📌 `imagem/stable-diffusion.md`  

# Stable Diffusion

## 🔹 Descrição
Stable Diffusion é um modelo de inteligência artificial de código aberto capaz de gerar imagens a partir de descrições textuais. Desenvolvido pela Stability AI, ele é amplamente utilizado para criar ilustrações, arte digital e imagens fotorrealistas.

## 🚀 Funcionalidades
- **Geração de imagens a partir de texto**  
- **Suporte para estilos variados e personalização**  
- **Possibilidade de rodar localmente ou via API**  
- **Técnicas de "inpainting" e "outpainting" para edição de imagens**  

## 📦 Instalação
Para rodar o Stable Diffusion localmente, utilize a versão da Stability AI:

```bash
pip install diffusers transformers accelerate
```

## 🛠️ Exemplo de Utilização via API
```python
from diffusers import StableDiffusionPipeline
import torch

pipe = StableDiffusionPipeline.from_pretrained("CompVis/stable-diffusion-v1-4")
pipe.to("cuda")  # Utilize GPU para melhor desempenho

prompt = "Uma cidade cyberpunk ao entardecer"
image = pipe(prompt).images[0]
image.show()
```

## 🔗 Ligações
- [Site Oficial](https://stablediffusionweb.com/)  
- [Repositório no GitHub](https://github.com/CompVis/stable-diffusion)  
- [Documentação da API](https://huggingface.co/docs/diffusers/index)  

---

## 🌟 Como Contribuir
1. Faça um **fork** do repositório.  
2. Crie um **branch** para a sua ferramenta: `git checkout -b minha-ferramenta`.  
3. Adicione um arquivo `.md` na categoria correta.  
4. Envie um **Pull Request**. 🎉  

## 📜 Licença
Este repositório está licenciado sob a **Licença CreativeML Open RAIL-M** (uso sujeito às diretrizes da Stability AI).  