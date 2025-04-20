# 📦 Testes Automatizados - PokéAPI

Este projeto contém testes automatizados criados com Postman para validar diversos aspectos da [PokéAPI](https://pokeapi.co), utilizando abordagens diferentes em cada endpoint, com foco em qualidade de dados, estrutura de resposta e integridade das informações.

## 🎯 Objetivo

Demonstrar conhecimento técnico em automação de testes de APIs REST utilizando o Postman, com cobertura de múltiplos tipos de validação e análise de comportamento esperado para diferentes endpoints públicos.

## 📚 Endpoints testados

- `/pokemon`
- `/ability`
- `/type`
- `/location`
- `/move`

Cada endpoint contém **5 testes únicos**, abordando desde respostas válidas, respostas inválidas (404), até validações de campos específicos, consistência entre valores, estrutura de objetos e relacionamentos.

---

## 🚀 Como executar os testes

### 🔹 Postman (Interface Gráfica)

1. Baixe o arquivo da collection: `pokeapi-testes.postman_collection.json`
2. Abra o Postman e clique em **Import**
3. Selecione o arquivo `.json` e importe
4. Execute os testes clicando em **Run Collection**

### 🔹 Newman (Linha de Comando)

> Pré-requisito: Node.js instalado

1. Instale o Newman:
```bash
npm install -g newman
```

2. Execute os testes:
```bash
newman run pokeapi-testes.postman_collection.json
```

---

## ✅ Estrutura de testes

- Validação de status HTTP (`200 OK`, `404 Not Found`)
- Checagem de campos obrigatórios e tipos de dados
- Consistência entre ID e nome de recursos
- Validação de listas (`types`, `abilities`, `moves`, `pokemon`)
- Verificação de relacionamentos (`generation`, `region`)
- Análise de campos de descrição em múltiplos idiomas (`effect_entries`)

---

## 👨‍💻 Autor

**Adan Barroso**  
📧 adan.barroso90@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com)
