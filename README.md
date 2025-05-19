# Feature Selection com Permutation Importance 🔀

Este repositório demonstra como aplicar **seleção de variáveis** utilizando o método de **importância por permutação** com `scikit-learn`.

## 💡 Sobre o projeto

A ideia principal é utilizar um método **simples, intuitivo e modelo-agnóstico** para identificar as variáveis com maior poder preditivo. Diferente de métodos baseados em coeficientes (como regressão linear) ou importância de árvores (como random forests), a **importância por permutação** avalia diretamente a variação na performance do modelo ao embaralhar cada feature individualmente.

Este método é:
- Independente do tipo de modelo utilizado;
- Baseado apenas na **métrica de desempenho**;
- Útil para avaliar a contribuição real de cada variável.

## 🧪 Como funciona

1. Um modelo é treinado com as features originais.
2. Cada feature é embaralhada individualmente.
3. O impacto dessa alteração na **acurácia (ou outra métrica)** é medido.
4. Quanto maior a queda no desempenho, mais importante é a feature.

⚠️ Atenção:
- Pode apresentar viés com **features altamente correlacionadas**.
- Precisa de um **modelo supervisionado** (com rótulo).
- Modelos sobreajustados podem distorcer a avaliação.

## 🛠️ Instruções de uso

### 1. Clonar o repositório

```bash
git clone https://github.com/raulward/feature_selection_permutation_importance.git
cd feature_selection_permutation_importance
