# 🍦 Prevendo Vendas de Sorvete com Machine Learning

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Latest-orange)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

## 📊 Sobre o Projeto

Este projeto utiliza técnicas de Machine Learning para prever vendas de sorvete com base em fatores como temperatura, umidade, dia da semana, sazonalidade e eventos especiais. O modelo ajuda proprietários de sorveterias a otimizar seu estoque, escalar a produção e maximizar receitas.

## 🎯 Objetivos

- Analisar os fatores que influenciam as vendas de sorvete
- Desenvolver modelos preditivos para previsão de demanda
- Criar visualizações que demonstrem padrões de consumo
- Fornecer insights acionáveis para proprietários de negócios

## 🧠 Modelos Utilizados

- Regressão Linear
- Random Forest
- XGBoost
- Redes Neurais (LSTM para análise temporal)

## 📂 Estrutura do Repositório

```
.
├── data/                      # Dados brutos e processados
├── notebooks/                 # Jupyter notebooks com análises
├── src/                       # Código fonte em Python
│   ├── preprocessing/         # Scripts para processamento dos dados
│   ├── modeling/              # Implementação dos modelos
│   ├── evaluation/            # Métricas e avaliação
│   └── visualization/         # Código para visualizações
├── models/                    # Modelos treinados salvos
├── results/                   # Resultados e visualizações
├── requirements.txt           # Dependências do projeto
├── setup.py                   # Script de instalação
└── README.md                  # Este arquivo
```

## 🔍 Features Principais

O modelo considera diversos fatores que influenciam as vendas de sorvete:

- **Temperatura:** Fator primário que impacta diretamente a demanda
- **Umidade:** Influencia a percepção térmica e conforto
- **Dia da Semana:** Padrões de consumo diferentes entre dias úteis e fins de semana
- **Sazonalidade:** Variações mensais e trimestrais
- **Feriados e Eventos:** Impacto de feriados e eventos locais nas vendas
- **Localização:** Diferenças geográficas nas preferências de consumo

## 📈 Resultados

O modelo XGBoost apresentou o melhor desempenho com:
- **RMSE:** 12.3 unidades
- **R²:** 0.87
- **MAE:** 9.2 unidades

![Previsão vs Realidade](results/prediction_vs_actual.png)

## 💡 Insights Principais

- Aumento de 1°C na temperatura resulta em aproximadamente 5% de aumento nas vendas
- Fins de semana apresentam vendas 30% maiores em comparação aos dias úteis
- Feriados podem aumentar vendas em até 45% dependendo da região
- Umidade acima de 80% impacta negativamente as vendas, mesmo em dias quentes

## 🚀 Como Usar

1. Clone o repositório:
```bash
git clone https://github.com/paulo-santos-ds/prevendo_vendas_sorvete.git
cd prevendo_vendas_sorvete
```

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

3. Execute o notebook de análise:
```bash
jupyter notebook notebooks/analise_exploratoria.ipynb
```

4. Para previsões com o modelo treinado:
```python
from src.modeling.predictor import IceCreamSalesPredictor

predictor = IceCreamSalesPredictor(model_path='models/xgboost_model.pkl')
predictions = predictor.predict(new_data)
```

## 📚 Próximos Passos

- [ ] Incorporar dados meteorológicos em tempo real
- [ ] Desenvolver API para integração com sistemas de inventário
- [ ] Adicionar previsão para diferentes tipos de sorvete
- [ ] Implementar análise de sentimento de redes sociais como variável preditora
- [ ] Expandir para previsão regionalizada com fatores demográficos

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

1. Faça um fork do projeto
2. Crie sua branch de feature (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas alterações (`git commit -m 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.


