# 📦 Testes Automatizados - PokeAPI

Este projeto contém testes automatizados criados com Postman para validar diversos aspectos da [PokeAPI](https://pokeapi.co), utilizando abordagens diferentes em cada endpoint, com foco em qualidade de dados, estrutura de resposta e integridade das informações.

---

## 🎯 Objetivo

Demonstrar conhecimento técnico em automação de testes de APIs REST utilizando o Postman, com cobertura de múltiplos tipos de validação e análise de comportamento esperado para diferentes endpoints públicos.

---

## 📚 Endpoints testados

- `/pokemon`
- `/ability`
- `/type`
- `/location`
- `/move`

Cada endpoint contém **5 testes únicos**, abordando desde respostas válidas e inválidas (404), até:

- Validação de estrutura e tipos de dados
- Consistência de valores
- Relacionamentos entre entidades (`generation`, `region`)
- Campos descritivos multilíngues
- Verificação de listas (`types`, `moves`, `areas` etc.)

---

## 🚀 Como executar os testes

### 🔹 Postman (Interface Gráfica)

1. Baixe o arquivo: `pokeapi-testes.postman_collection.json`
2. Abra o **Postman**
3. Vá em **Import > File** e selecione o JSON
4. Clique em **Run Collection** para executar todos os testes

---

### 🔹 Newman (Linha de Comando com relatório HTML)

#### 🛠️ Pré-requisitos:
- Node.js instalado
- Newman + htmlextra:

```bash
npm install -g newman newman-reporter-htmlextra
```

#### ▶️ Executar com relatório visual:

```bash
mkdir -p report
newman run "pokeapi-testes.postman_collection.json" --reporters cli,htmlextra --reporter-htmlextra-export "report/pokeapi-relatorio.html" --reporter-htmlextra-title "Relatório de Testes - PokeAPI"
```

Depois disso, abra o arquivo `report/pokeapi-relatorio.html` no navegador para ver os resultados com visual amigável.

---

## 📁 Estrutura de Diretórios

```
pokeapi-api-tests/
├── pokeapi-testes.postman_collection.json   # Collection com os testes
├── report/
│   └── pokeapi-relatorio.html               # Relatório (gerado após execução)
└── README.md                                # Este arquivo
```

---

## 👨‍💻 Autor

**Adan Barroso**  
📧 adan.barroso90@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com)
