🩺 Pima Indians Diabetes — Machine Learning Notebook
📌 Descrição do Projeto
Este projeto desenvolve um modelo de Machine Learning para prever a presença de diabetes em pacientes, utilizando o dataset Pima Indians Diabetes Database.

O classificador principal é o Support Vector Machine (SVM), com foco em:

Otimização de hiperparâmetros via GridSearchCV
Comparação entre KFold (10) e StratifiedKFold (3)
O objetivo é mostrar como a escolha da validação cruzada pode impactar o desempenho, especialmente em datasets desbalanceados, garantindo estimativas mais confiáveis e um modelo final mais robusto.

⚙️ Metodologia
✔️ Carga e Divisão dos Dados

Dataset dividido em 80% treino / 20% teste, de forma estratificada.
✔️ Pipeline de Pré-processamento

Imputação de valores ausentes com SimpleImputer (mediana).
Padronização das features com StandardScaler.
✔️ Otimização com GridSearchCV

Busca exaustiva pelos melhores hiperparâmetros (kernel, C, gamma).
Comparação entre:
KFold (10) → validação padrão
StratifiedKFold (3) → mantém proporção de classes em cada fold
✔️ Treinamento e Avaliação

Melhor configuração encontrada:
{'clf__kernel': 'rbf', 'clf__C': 10, 'clf__gamma': 0.01}
Avaliação com métricas como acurácia, matriz de confusão, precisão, recall e F1-score.
✔️ Visualização

Fronteira de decisão gerada a partir de duas features relevantes (Glucose e BMI), destacando os vetores de suporte.
🔧 Pré-requisitos
📍 Recomendado rodar no Google Colab (ambiente já pronto).

Requirements
pandas
numpy
scikit-learn
matplotlib
📊 Resultados
Melhor configuração: rbf, C=10, gamma=0.01
Acurácia no teste: ~75,32%
Bom equilíbrio entre precisão e recall
Recall da classe diabético é destaque (importância clínica).
Matriz de Confusão
matriz de confusao

Curvas ROC e Precision-Recall
Comparação entre SVM Linear (KFold=10) e SVM RBF (StratifiedKFold=3):

ROC AUC: 0.83 (ambos)
AP (Precision-Recall): RBF levemente superior (0.72 vs 0.71)
🛠️ Ferramentas Utilizadas
Linguagem: Python 3
Bibliotecas: pandas, numpy, scikit-learn, matplotlib
📌 Projeto feito para estudo de Machine Learning aplicado a dados biomédicos.
