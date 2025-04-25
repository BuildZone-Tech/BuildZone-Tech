BuildZone API

API para análise de compatibilidade de peças de PC Gamer.

Requisitos

Node.js (v18 ou superior)

npm


Instalação

git clone https://github.com/seu-usuario/buildzone-api.git
cd buildzone-api
npm install

Como rodar o servidor

npm start

Servidor rodando em: http://localhost:3000

Rotas disponíveis

GET /api/parts

Retorna a lista de todas as peças disponíveis.

POST /api/compatibility

Verifica se as peças selecionadas são compatíveis.

Body esperado:

{
  "cpu": "AMD Ryzen 5 5600X",
  "motherboard": "ASUS TUF Gaming B550M-Plus",
  "gpu": "NVIDIA GeForce RTX 3060",
  "ram": "Corsair Vengeance LPX 16GB (2x8GB) 3200MHz",
  "storage": "Samsung 980 1TB NVMe",
  "psu": "Corsair CV550 550W 80 Plus Bronze",
  "case": "NZXT H510"
}

Resposta:

{
  "compatible": true,
  "messages": [
    "CPU e Placa-mãe são compatíveis.",
    "Fonte de alimentação é suficiente para a GPU."
  ]
}

Estrutura de pastas

├── data
│   └── parts.json
├── routes
│   ├── compatibility.js
│   └── parts.js
├── utils
│   └── compatibility.js
├── server.js
└── package.json

Autor

BuildZone - 2025

