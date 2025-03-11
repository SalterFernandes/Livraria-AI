📌 `visao_computacional/pytorch.md`

# PyTorch

## 🔹 Descrição
PyTorch é uma biblioteca de aprendizado profundo desenvolvida pela Meta. Ela é amplamente utilizada para pesquisa e criação de protótipos devido à sua flexibilidade e facilidade de uso.

## 🚀 Funcionalidades
- **Treinamento de modelos de aprendizado profundo**
- **Suporte a redes neurais convolucionais (CNNs) e redes neurais recorrentes (RNNs)**
- **Integração com outras bibliotecas de aprendizado de máquina**
- **Ferramentas para visualização e depuração de modelos**

## 📦 Instalação
Para instalar o PyTorch, utilize o seguinte comando:

```bash
pip install torch
```

## 🛠️ Exemplo de Utilização via API
Aqui está um exemplo de como usar PyTorch para treinar uma rede neural simples:

```python
import torch
import torch.nn as nn
import torch.optim as optim
import torch.nn.functional as F
from torchvision import datasets, transforms

# Definir transformações para os dados
transform = transforms.Compose([transforms.ToTensor()])

# Carregar dados de exemplo
train_dataset = datasets.MNIST(root='./data', train=True, download=True, transform=transform)
train_loader = torch.utils.data.DataLoader(dataset=train_dataset, batch_size=64, shuffle=True)

# Definir modelo
class SimpleNN(nn.Module):
    def __init__(self):
        super(SimpleNN, self).__init__()
        self.fc1 = nn.Linear(28*28, 128)
        self.fc2 = nn.Linear(128, 10)

    def forward(self, x):
        x = x.view(-1, 28*28)
        x = F.relu(self.fc1(x))
        x = self.fc2(x)
        return x

model = SimpleNN()

# Definir função de perda e otimizador
criterion = nn.CrossEntropyLoss()
optimizer = optim.Adam(model.parameters(), lr=0.001)

# Treinar modelo
for epoch in range(10):
    for images, labels in train_loader:
        outputs = model(images)
        loss = criterion(outputs, labels)
        optimizer.zero_grad()
        loss.backward()
        optimizer.step()

print('Treinamento concluído')
```

## 🔗 Ligações
- Site Oficial
- Documentação
