# analise-credito-ds
Análise exploratória das variáveis financeiras do dataset Default of Credit Card Clients. Estatísticas descritivas, histogramas e transformação logarítmica com Python, Pandas, NumPy e Matplotlib.
# 📊 Explorando as Características Financeiras do Dataset de Crédito

Análise exploratória das variáveis financeiras do dataset **Default of Credit Card Clients**, realizada como atividade prática da disciplina de Ciência de Dados.

---

## 📁 Sobre o Dataset

O dataset contém informações de **30.000 clientes** de cartão de crédito de uma instituição financeira de Taiwan, com dados de pagamentos, faturas e inadimplência entre abril e setembro de 2005.

| Coluna | Descrição |
|---|---|
| `BILL_AMT1` a `BILL_AMT6` | Valor da fatura nos últimos 6 meses |
| `PAY_AMT1` a `PAY_AMT6` | Valor do pagamento realizado nos últimos 6 meses |
| `default payment next month` | Variável-alvo: 1 = inadimplente, 0 = adimplente |

---

## 🧪 Exercícios Desenvolvidos

### Exercício 1 — Criação de listas de características
Organização das colunas financeiras em listas separadas (`bill_feats` e `pay_feats`) para facilitar a manipulação ao longo da análise.

### Exercício 2 — Estatísticas descritivas das faturas
Uso do `.describe()` para examinar média, desvio padrão, mínimo e máximo das colunas `BILL_AMT`. Os dados revelam forte assimetria: valores negativos (estornos/créditos) e máximos acima de 900.000, com desvio padrão muito elevado.

### Exercício 3 — Histogramas das faturas (grade 2×3)
Visualização da distribuição de cada coluna de fatura com 20 bins. Os gráficos confirmam a assimetria positiva: a maioria dos clientes possui faturas baixas, com uma cauda longa à direita.

### Exercício 4 — Estatísticas descritivas dos pagamentos
`.describe()` aplicado às colunas `PAY_AMT`. A mediana próxima de zero em vários meses indica que grande parte dos clientes não realizou pagamentos, enquanto poucos efetuaram pagamentos muito altos.

### Exercício 5 — Histogramas dos pagamentos com rotação de rótulos
Grade 2×3 de histogramas para as colunas de pagamento, com `rotation=45` no eixo x para evitar sobreposição. Os gráficos evidenciam a concentração extrema próxima ao zero.

### Exercício 6 — Máscara booleana para pagamentos zerados
Identificação da proporção de pagamentos exatamente iguais a 0 em cada mês. Resultado: entre **20% e 30%** dos clientes não realizaram pagamentos em cada período — o que explica a barra dominante nos histogramas anteriores.

### Exercício 7 — Transformação logarítmica dos pagamentos
Filtrando os zeros e aplicando `np.log10` via `.apply()`, as distribuições passam a se aproximar de uma curva normal. Isso confirma que os pagamentos seguem uma **distribuição log-normal**: a maioria dos valores não-nulos se concentra entre 1.000 e 100.000.

---

## 🛠️ Tecnologias Utilizadas

- Python 3
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

## ▶️ Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/Natan-Murillo/SEU_REPOSITORIO.git
```

2. Instale as dependências:
```bash
pip install pandas numpy matplotlib xlrd jupyter
```

3. Coloque o arquivo `.xls` do dataset na mesma pasta do notebook.

4. Abra o notebook:
```bash
jupyter notebook trabalho_credit_card.ipynb
```

Ou abra diretamente no **Google Colab** pelo botão abaixo:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

---

## 👤 Autor

**Natan Murillo**  
Estudante de Análise e Desenvolvimento de Sistemas — Afya Unigranrio  
[LinkedIn](https://linkedin.com/in/natanmfg) • [GitHub](https://github.com/Natan-Murillo)
