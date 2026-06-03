# Projeto Avaliativo: Análise Exploratória de Dados - Base Varejo

- **Aluno:** Cássio Silva Souza
- **Curso:** Análise de dados com Python
- **Turma:** QA ADPY 2026/1 2

Este repositório contém a solução desenvolvida para o Mini-Projeto Avaliativo do Módulo 1 (Semana 07), focado na aplicação prática de técnicas de Análise Exploratória de Dados (AED), limpeza, transformação e estatística descritiva utilizando a biblioteca `pandas` em Python.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas
* **Linguagem:** Python 3.13+
* **IDE:** Visual Studio Code (VS Code)
* **Bibliotecas:** 
  * `pandas` (Manipulação e tratamento de dados)
  * `numpy` (Suporte matemático)
  * `warnings` (Otimização de exibição de logs do terminal)

---

## 🏃‍♂️ Como Executar o Projeto

### Pré-requisitos
Antes de rodar o script, certifique-se de ter o Python instalado e as dependências necessárias. Você pode instalá-las executando no terminal:
```bash
pip install pandas numpy
```
---

## 📈 Principais Insights e Decisões Técnicas

1. **Estrutura:** A base original possui 830.000 registros. Identificado que os registros repetidos de IDs de compras (`id_cupom`) e clientes (`id_cliente`) não se tratam de erros de duplicidade, mas sim de uma estrutura transacional, representando vários itens adquiridos em uma mesma jornada de compra.
2. **Colunas vazias:** Havia 4 colunas vazias no arquivo original (`Unnamed: 10` a `13`) totalmente preenchidas com valores nulos, as quais foram excluídas na limpeza inicial para otimização de memória e melhor análise.
3. **Coluna DATA:** Para melhor compreensão e buscando otimizar etapas futuras de análise cronológica, converti a coluna `DATA` de string para o formato `datetime`.
4. **Normalização de colunas e valores:** Buscando um melhor entendimento do dataframe, decidi renomear todas as colunas com títulos mais intuitivos. Normalizei os valores das colunas `nome_produto` e `categoria_produto`. Além disso, renomeei os valores da coluna `genero_cliente` para 'Masculino' quando 'M' e 'Feminino' quando 'F'. 
5. **Nulos e Duplicatas:** Só haviam nulos nas 4 últimas colunas que foram eliminadas. Os valores duplicados encontrados dizem respeito à estrutura transacional do dataframe, e por isso, foram mantidos.

---

## Conclusões

1. O produto que mais vende é o `Presunto Cozido`;

2. Identifiquei um volume grande de itens por compras, demostrando que os cliente costumam aproveitar a jornada de compra para levar muitos produtos de uma só vez, provavelmente priiorizando compras quinzenais ou mensais;

3. Os cliente do gênero masculino tendem a ter uma média maior de filhos;

4. Clientes do segmento B são os que mais compram, correspondendo a 64% do volume de compras;


