# Projeto de Análise e Visualização de Dados
### Brazilian E-Commerce Public Dataset by Olist
![sales](https://github.com/mariacdev/Projeto-New-York-City-Airbnb-Open-Data/assets/134116444/b1e45c7e-4b60-4fca-9f38-ad99c87eb99d) 

#### Acesse o Dashboard: [Power BI](https://app.powerbi.com/links/f9X1pwJdoF?ctid=e5d658d7-a357-4ac1-a718-5ce049b564e6&pbi_source=linkShare) 

O projeto 'Brazilian E-Commerce Public Dataset by Olist' é uma simulação de análise de dados em uma empresa de e-commerce, para extrair insights que possam melhorar as operações de negócios, otimizar a logística e oferecer uma melhor experiência ao cliente. utilizando o conjunto de dados público disponivel no  [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). 

## 1. Questões de Negócio
O Olist, é uma startup brasileira fundada em 2015, atua no segmento de tecnologia para varejo, oferecendo soluções que facilitam a gestão de lojas off-line e online, bem como uma solução de aceleração de vendas dentro de marketplaces. A empresa, sediada em Curitiba, Brasil, tem como missão fortalecer o comércio no mundo, proporcionando oportunidades reais de crescimento para pequenos, médios e grandes comércios.

### 1.1. Problemática
Abordaremos três problemas principais:
#### 1. Melhorar a Recomendação de Produtos e Personalizar a Experiência do Cliente;
#### 2. Otimizar a Gestão de Inventário e Operações Logísticas;
#### 3. Visualização de Dados para Decisões Estratégicas e Operacionais.

### 1.2. Objetivo
Nosso objetivo principal é oferecer uma melhor experiência ao cliente, otimizando a gestão de inventário, melhorando as operações logísticas e aprimorando as recomendações de produtos. Auxiliar através da visualização de dados as tomadas de decisões estratégicas e operacionais.  

## 2. Premissas de negócio
O "Brazilian E-Commerce Public Dataset by Olist" consiste em um conjunto de tabelas que oferecem uma visão abrangente das transações de comércio eletrônico. Abordarei em detalhes algumas das principais tabelas e seus campos.
![organização_dados](https://github.com/mariacdev/Projeto-New-York-City-Airbnb-Open-Data/assets/134116444/a2bc0e8e-fc31-4752-b3af-44a8a36df671)


Os atributos do conjunto de dados são:

 Tabela "olist_orders_dataset"
| Atributos  | Descrição |
| --- | --- |
| order_id | Identificador único para cada pedido |
| customer_id | Status do pedido |
| order_purchase_timestamp | Data e hora da compra |
| order_approved_at | Data e hora da aprovação do pedido |
| order_delivered_carrier_date | Data de envio do pedido pelo transportador |
| order_delivered_customer_date | Data de entrega do pedido ao cliente | 
| order_estimated_delivery_date | Data estimada de entrega do pedido |

Tabela "olist_order_items_dataset" 
| Atributos  | Descrição |
| --- | --- | 
| order_id | Identificador único para cada pedido | 
| order_item_id | Identificador único para cada item no pedido |
| product_id | Identificador único para cada produto |
| seller_id | Identificador único para cada vendedor |
| shipping_limit_date | Data limite para envio do item |
| price | Preço do item |
| freight_value | Valor do frete para o item | 

Tabela "olist_products_dataset" 
| Atributos  | Descrição |
| --- | --- |  
| product_id | Identificador único para cada produto |
| order_item_id | Identificador único para cada item no pedido |
| product_id | Identificador único para cada produto |
| seller_id | Identificador único para cada vendedor |
| shipping_limit_date | Data limite para envio do item |
| price | Preço do item |
| freight_value | Valor do frete para o item | 

Tabela "olist_products_dataset" 
| Atributos  | Descrição |
| --- | --- |   
| product_id | Identificador único para cada produto |
| product_category_name | Nome da categoria do produto |
| product_name_length | Comprimento do nome do produto |
| product_description_length | Comprimento da descrição do produto | 
| product_photos_qty | Quantidade de fotos do produto | 
| product_weight_g | Peso do produto em gramas | 
| product_length_cm | Comprimento do produto em centímetros | 
| product_height_cm | Altura do produto em centímetros |
| product_width_cm | Largura do produto em centímetros | 

Tabela "olist_customers_dataset" 
| Atributos  | Descrição |
| --- | --- | 
| customer_id |  Identificador único do cliente |
| customer_unique_id | Identificador único e anônimo do cliente |
| customer_zip_code_prefix | Código postal do cliente  |
| customer_city | Cidade do cliente | 
| customer_state | Estado do cliente | 

Tabela "olist_sellers_dataset" 
| Atributos  | Descrição |
| --- | --- |  
| seller_id | Identificador único do vendedor |
| seller_zip_code_prefix | Código postal do vendedor  |
| seller_city | Cidade do vendedor | 
| seller_state | Estado do vendedor | 

Tabela "olist_order_reviews_dataset" 
| Atributos  | Descrição |
| --- | --- | 
| review_id | Identificador único para cada avaliação |
| order_id |  Identificador único para cada pedido associado à avaliação |
| review_score | Pontuação atribuída pelo cliente à avaliação | 
| review_comment_title | Título do comentário da avaliação |
| review_comment_message | Mensagem do comentário da avaliação | 
| review_creation_date | Data de criação da avaliação |
| review_answer_timestamp | Data de resposta à avaliação |

Tabela "olist_order_payments_dataset" 
| Atributos  | Descrição |
| --- | --- |  
| order_id | Identificador único para cada pedido |
| payment_sequential | Número sequencial para indicar a ordem dos pagamentos para o mesmo pedido |
| payment_type | Método de pagamento utilizado |
| payment_installments | Número de parcelas do pagamento | 
| payment_value | Valor do pagamento |

Tabela "olist_geolocation_dataset" 
| Atributos  | Descrição |
| --- | --- |  
| geolocation_zip_code_prefix | Código postal da localização |
| geolocation_lat | Latitude da localização | 
| geolocation_lng | Longitude da localização |
| geolocation_city | Cidade da localização |
| geolocation_state | Status da localização | 

Tabela "product_category_name_translation"
| Atributos  | Descrição |
| --- | --- |  
| product_category_name | Nome original da categoria de produto em português |
| product_category_name_english | Tradução do nome da categoria para o inglês | 

- Neste projeto realizei uma análise descritiva e exploratória, a fim de compreender alguns fenômenos, além de gerar hipóteses úteis para as tomadas de decisões.
- Toda a análise seguiu uma estrutura simples e direta, bem detalhada em todos os tópicos.

## 3. Planejamento da solução 

### 3.1. Produto final
- Entregar Insights para as áreas de logística e negócio;
- Dashboard para visualização dos dados.

### 3.2. Ferramentas
**Liguagem de programção:**
- Python
**Estatística:**
- Média, moda, mediana e desvio padrão
**API:**
- Kaggle
**IDE ( Ambiente de Desenvolvimento Integrado ):**
- Visual Studio Code
**Visualização de Dados:**
- Power BI

## 4. Análise Exploratória 
Nosso objetivo principal com a análise exploratória é entender a estrutura, padrões, relações e características dos dados, que nos forneçam insights iniciais e orientando a direção da análise mais aprofundada, realizada no início do ciclo de vida de um projeto. 

### Objetivos da Análise Exploratória de Dados:
1. Ter uma visão geral dos dados para identificar padrões e características adversas.
2. Detectar outliers, valores ausentes e outras irregularidades nos dados.
3. Explorar relações entre diferentes variáveis, identificando potenciais correlações e padrões.
4. Compreender a distribuição de cada variável no conjunto de dados.
5. Calcular estatísticas descritivas, como médias, medianas, desvios padrão, etc.
6. Utilizar gráficos e visualizações para representar os dados de forma compreensível.











