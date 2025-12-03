📘 README — Projeto de Análise Exploratória e Pré-Processamento dos Dados da Olist
👥 Integrantes do Grupo
João Pedro Lima Barbosa
Rodolfo Dheymison Ferreira Silva
🔗 Base de Dados Utilizada
Os dados utilizados pertencem ao Brazilian E-Commerce Public Dataset by Olist, disponível em:
➡ https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce
Datasets usados no projeto:
olist_orders_dataset.csv
olist_order_items_dataset.csv
olist_products_dataset.csv
🎯 Objetivo do Projeto
Aplicar um processo completo de análise exploratória (EDA) e pré-processamento de dados, incluindo:
investigação e compreensão dos datasets
identificação e tratamento de problemas
criação de novos atributos
análise gráfica
preparação dos dados para futuras etapas de modelagem
O objetivo final é entender o comportamento dos pedidos da Olist e seus fatores logísticos, além de gerar insights úteis sobre atrasos, preços, categorias e fretes.
🧹 Descrição do Processo de Tratamento dos Dados
✔ 1. Análise de valores ausentes
Preenchimento de datas com moda (quando aplicável).
Remoção de colunas irrelevantes com excesso de nulos.
Imputação de valores numéricos com mediana.
✔ 2. Duplicatas
Verificação em todos os datasets.
Nenhuma duplicata exata encontrada.
✔ 3. Inconsistências
Foram detectados e tratados:
pesos e dimensões impossíveis
fretes incompatíveis
categorias duplicadas ou incoerentes
preços fora de padrão
✔ 4. Outliers
Métodos utilizados:
IQR
análise visual com histogramas e boxplots
Tratamento:
remoção de valores impossíveis
cap para valores exagerados porém possíveis
✔ 5. Conversão de tipos
Datas convertidas para datetime
Colunas numéricas padronizadas
Textos normalizados (case/acentos)
✔ 6. Codificação e Normalização
Label Encoding para categorias maiores
One-Hot Encoding para categorias menores
MinMaxScaler e Z-Score aplicados conforme distribuição das variáveis
✔ 7. Feature Engineering
Foram criadas novas variáveis como:
tempo de entrega
atraso de entrega
valor total do item
ano/mês da compra
volume do produto
🚧 Principais Desafios Encontrados
forte presença de outliers financeiros e logísticos
inúmeras inconsistências nas dimensões/dados de produtos
categorias pouco padronizadas
necessidade de sincronizar datas entre datasets
junção dos três arquivos para criar um dataset único coerente
diversas colunas com dados faltantes de forma irregular
pesos e medidas que exigiram validação direta para evitar distorções
📌 Principais Conclusões
Fretes altos possuem forte relação com dimensões e distância do cliente.
Algumas categorias apresentam mais atrasos e valores mais extremos.
A limpeza dos dados corrigiu distorções significativas nas distribuições, tornando a análise mais confiável.
A criação de variáveis derivadas (como tempo e atraso de entrega) mostrou padrões logísticos importantes.
O conjunto final está mais consistente, padronizado e ideal para futuras análises preditivas.
