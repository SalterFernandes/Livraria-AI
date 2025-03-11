📌 `PLN/openai-gpt.md`

```md
# OpenAI GPT-4

## 🔹 Descrição
O GPT-4 é um modelo de IA desenvolvido pela OpenAI para gerar texto de forma inteligente e contextualizada.

## 🚀 Funcionalidades
- Geração de texto avançada  
- Resumo e reescrita de textos  
- Tradução automática  

## 📦 Instalação
```bash
pip install openai
```

## 🛠️ Exemplo de Utilização
```python
import openai

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[{"role": "user", "content": "O que é IA?"}]
)
print(response["choices"][0]["message"]["content"])
```

## 🔗 Ligações
- [Documentação Oficial](https://platform.openai.com/docs)
```

---

## 🌟 Como Contribuir
1. Faça um **fork** do repositório.
2. Crie um **branch** para a sua ferramenta: `git checkout -b minha-ferramenta`.
3. Adicione um arquivo `.md` na categoria correta.
4. Envie um **Pull Request**. 🎉

## 📜 Licença
Este repositório está licenciado sob a **Licença MIT**.
