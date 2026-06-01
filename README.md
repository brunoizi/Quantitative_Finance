# DCA na Queda — Estratégia de Compra em Quedas de BTC

Uma análise prática e intuitiva de estratégias de **Dollar-Cost Averaging (DCA)** aplicadas ao Bitcoin, comparando três abordagens:

1. **Só na Queda**: Compra apenas quando o BTC fecha o dia em queda
2. **Todo Dia**: Compra um valor fixo todos os dias
3. **Todo Dia + Dobro na Queda** ⭐: Compra todo dia e dobra o aporte quando há queda

## 📊 Resultados (desde 2020-01-01)

| Estratégia | Investido | BTC Acumulado | Preço Médio | Valor Atual | Lucro | ROI |
|---|---|---|---|---|---|---|
| Só na queda | $11,490 | 0.40 | $28,391 | $29,840 | $18,350 | 159.71% |
| Todo dia | $23,420 | 0.84 | $27,893 | $61,909 | $38,489 | 164.34% |
| **Todo dia + dobro na queda** | $34,910 | 1.24 | $28,055 | $91,749 | $56,839 | **162.82%** |

A estratégia **"Todo dia + dobro na queda"** gera o **maior lucro absoluto**, aproveitando as quedas para aumentar a quantidade de moeda comprada quando o preço está mais baixo.

## 🚀 Como Usar

### Pré-requisitos
```bash
pip install requests pandas numpy matplotlib
```

### Rodar a análise
```bash
jupyter notebook dca_btc_na_queda.ipynb
```

## 📝 Descrição da Estratégia

**Premissa**: Comprar Bitcoin todo o dia, aumentando o volume quando há quedas no mercado.

- **Período**: 2020-01-01 até hoje
- **Aporte base**: US$ 10 (configurável)
- **Dados**: BTCUSDT da Binance (API pública)
- **Regra**: 
  - Todo dia: compra `aporte_base`
  - Se `Close[dia] < Close[dia anterior]`: compra `2 × aporte_base` naquele dia

## 📈 Visualizações

O notebook gera:
- Gráfico de preço com pontos de compra discriminados
- Evolução do valor da carteira vs. investimento
- Comparação lado-a-lado das três estratégias
- Tabelas de resumo com métricas finais

## 💡 Insights

- **Timing não é tudo**: Comprar todo dia obtém melhor ROI (164.34%) do que só na queda (159.71%)
- **Volume importa**: Aumentar compras em quedas captura mais moeda aos preços mais baixos
- **Consistência vence**: A estratégia combinada gera o lucro absoluto mais alto ($56.8k vs $38.5k)

## 🔧 Customização

Edite os parâmetros na Célula 1:
- `SYMBOL`: Par de trading (padrão: "BTCUSDT")
- `START`: Data de início (padrão: "2020-01-01")
- `BUY_USD`: Aporte em dólares (padrão: 10.0)
- `USE_SYNTHETIC`: Use dados falsos para teste (padrão: False)

## 📚 Tecnologias

- **pandas**: Manipulação de dados
- **numpy**: Cálculos numéricos
- **matplotlib**: Visualizações
- **requests**: API da Binance

---

**Autor**: Estratégia DCA Adaptativa  
**Última atualização**: Maio 2026
