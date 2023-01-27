# Sistema de Recomendação - Netflix
![netflix-3733812](https://user-images.githubusercontent.com/98356094/191376358-e0fb3df9-f6b4-4db8-ac5f-ea8bd67cb156.jpg)

Este é um projeto pessoal realizado com dados privados disponibilizados pela empresa Netflix.


## 1. Problema de Negócio
A Netflix para não perder espaço para seus concorrentes, pensa em investir em sistemas de recomendação com o objetivo de reter seus clientes e diminuir o número de churn.


## 2. Entendimento do Negócio
#### Motivação
A netflix requisitou esse sistema ao perceber uma diminuição de conteúdos assistidos por seus usuários.

#### Causa Raiz do Problema
Perda de interesse dos clientes e aumento de churn de clientes.

#### Quem é o Stakeholder
o CEO da Netflix.

#### Formato da Solução
* Análise das preferências de conteúdo do usuário,
* Sistema de recomendacão,
* Predições acessadas via celular.
 
 
## 3. Metodologia de Desenvolvimento do Projeto
 O projeto foi desenvolvido através da técnica CRISP-DM
 * Versão END-TO_END da solução,
 * Velocidade na entrega de valor,
 * Mapeamento de todos os possíveis problems.


##### Passo 01 - Descrição dos dados: Conhecimento dos dados, tipos, métricas estatísticas para identificar outliers, analise das métricas estatísticas e ajustes em features do dataset (preenchimento de NA's).


##### Passo 02 - Feature Engineering: Desenvolvimento de mapa mental para analisar o fenômeno, as variáveis e os principais aspectos que impactam cada uma delas. 


##### Passo 03 - Filtragem dos dados: Filtragem das linhas e excluir as colunas que não são relevantes para o modelo ou não fazem parte do escopo do negócio. EX: Dias em que as lojas estavam fevhadas ou inoperantes.


##### Passo 04 - Análise Exploratória dos dados: Exploração dos dados para encontrar insights.


##### Passo 05 - Preparação dos dados: Preparação para as aplicações de modelos de machine learning.


##### Passo 06 - Seleção de Features: Seleção dos melhores atributos para treinar o modelo.


##### Passo 07 - Modelagem de Machine Learning: Foram realizados testes e treinamentos de alguns modelos de machine learning, para possibilitar a comparação da performance e escolha do modelo ideal para o projeto. Foi utilizada a técnica de Matriz de confusão para garantir a performance real sobre os dados selecionados.


##### Passo 08 - Hyperparameter Fine Tunning: Análise pelo método Random Search, em cima do algoritmo escolhido TfidfVectorizer, para escolha dos melhores valores de cada parâmetro do modelo.


##### Passo 09 - Tradução e interpretação de erros: Aqui entendemos a performance do modelo para comunicar ao CEO as preferências de conteúdo do usuário. Foram usadas as métricas: MAE (Mean Absolute Error), MAPE (Mean Absolute Percentage Error) e RMSE (Root Mean Squared Error).


##### Passo 10 - Deploy do modelo em produção: Publicação em um ambiente de nuvem. Foi escolhida a plataforma XXXXX.


##### Passo 11 - Bot do Telegram: Aqui realizamos a criação do bot no Telegram, o qual possibilita a consulta das recomendações.


## 4. Entendendo os Dados
* Dados privados disponibilizados pela empresa Netflix. 

| VARIÁVEL  |  DEFINIÇÃO  |
| ------------------- | ------------------- |
|Profile Name |  o nome do perfil usado para assistir.|
|Start Time |  a data e a hora (UTC) do início da visualização.|
|Duration |a duração da sessão.|
|Attributes |esta coluna mostra detalhes adicionais das interações com o conteúdo acessado, quando disponíveis: Autoplayed:user action: None - assinante não interagiu; Autoplayed:user action: Unspecified - assinante interagiu clicando na imagem da caixa e visualizou a página da série ou filme enquanto é apresentado o conteúdo automático ou o assitiu por mais d 2 minutos; Autoplayed:user action: User_Interaction - o assinante interagiu com a sérieou filme clicamdo nos controles do player ou atalhos do teclado; View was hidden - Filme foi ocultado do histórico assistido; Has branched playback - assinante pode escolher opçõesenquanto assiste ao título, para controlar o que acontece em seguida.|
|Title |Filme ou serie assistido.|
|Supplemental Video Type |Videos que não sejam filmes e series, como: Trailers ou montagens.|
|Device type |Tipo de de aparelho utilizado para acessae a série ou o filme.|
|Bookmark |a posicão de visualização mais recente.|
|Latest Bookmark |indica se o marcador é a posicão de visualização mais recente.|
|Country |o país de onde a série ou filme foi assistido.|


## 5. Principais Insights

**Hipótese 1**


**Hipótese 2**


**Hipótese 3**


## 6. Performance do Modelo

A estratégia foi efetivar um modelo de recomendação baseado no conteúdo de filmes e series (Content Based), no qual filmes/series com maior probabilidade de serem semelhantes são recomendados ao usuário. Foi utilizado o modelo TF-IDF (Term Frequency-Inverse Document Frequency), que adota um cálculo estatístico capaz de medir os termo mais relevantes para um tópico, analisando a frequência com que aparecem nos dados, em comparação à sua frequência em um conjunto maior de dados.

O cálculo faz uma ponderação de termos para entender a importância de palavras específicas nos dados fornecidos.
Então, quanto maior for a frequência no documento (TF), maior será a importância do termo, e quanto maior a frequência no conjunto de dados (IDF), diminui o peso dos termos que ocorrem com muita frequência nesse conjunto e aumenta o peso dos termos que ocorrem raramente.


Para a realização desta etapa do projeto, foi aplicado o seguinte modelo:

* TfidfVectorizer


### Comparação da performance dos modelos

Imagem a ser disponibilizada

### Performance final do modelo escolhido após Hyperparameter Fine Tuning

Imagem a ser disponibilizada


## 7. Resultado Final
Obtivemos bons resultados no sistema de recomendação, o qual o CEO da empresa poderá oferecer acesso às recomendações de conteúdo por meio de um DashBoard pelo Streamlit.
A performance do modelo pode ser constatada na análise da relação dos titulos assistidos e a descrição do conteúdo:

Imagem da performance a se disponibilizada


## - Conclusão
 
O sistema de recomendacão content based (por conteúdo) estão sendo projetadas com sucesso. Sendo assim, a usuária poderá consultar de qualquer lugar as recomendações de filmes e series, por meio da Aplicação Web Streamlit, podendo escolher novos conteúdos por meio da análise e entendimento do gosto pessoal da usúaria da plataforma Netflix.


**Para acessar os resultados do sistema de recomendação, basta acessar o link: xxxxxx.**
**P.S. link ainda será disponibilizado**
