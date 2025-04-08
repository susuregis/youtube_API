# youtube_API


Este projeto tem como objetivo analisar os vídeos de highlights das corridas de Fórmula 1 publicados no canal oficial da F1 no YouTube, com foco no ano de 2024. Através da API do YouTube, foram coletadas métricas como visualizações, curtidas, comentários e taxa de engajamento, permitindo análises comparativas entre os vídeos e insights sobre o desempenho do canal ao longo do tempo.

**Objetivo**

Criar um painel de visualização no Power BI com dados dos vídeos de highlights do canal oficial da Fórmula 1, promovendo análises sobre engajamento e desempenho dos vídeos publicados em 2024.

--------------------------------------------------------------------------------------



Power Bi : https://app.powerbi.com/view?r=eyJrIjoiZmY3NTI0YzMtMTAyZC00ZmVhLThkZWMtMDIyOTQzYjNkODc4IiwidCI6IjRhMjJmMTE2LTUxY2UtNGZlMy1hZWFhLTljNDYxNDNkMDg4YiJ9






**Funcionalidades**

- Coleta automatizada de dados via API do YouTube (YouTube Data API v3)

- Filtragem por palavra-chave (“highlights”) para garantir a relevância dos vídeos coletados

- Exportação dos dados para Excel para facilitar a integração com o Power BI

- Análises comparativas e visuais no Power BI (total de visualizações, curtidas, comentários, engajamento etc.)

- Dashboard interativo com filtros por data, taxa de engajamento, vídeos mais vistos e mais comentados
- 
--------------------------------------------------------------------------------------
  

**Tecnologias e Ferramentas**

- Python (Google Colab): para coleta, tratamento e exportação dos dados

- YouTube Data API v3: para acessar informações dos vídeos do canal

- Pandas + Openpyxl: para manipulação e exportação dos dados

- Power BI: para visualização e análise interativa dos dados

--------------------------------------------------------------------------------------

**Como Executar o Projeto**

Instale as dependências necessárias:

  - **pip install google-api-python-client pandas openpyxl**

Importe a biblioteca para acessar a API do YouTube:

 -  **from googleapiclient.discovery import build**

Configure sua chave de API:

  - **youtube = build("youtube", "v3", developerKey="SUA_CHAVE_AQUI")**

Execute as funções de coleta e análise no Google ColabUtilizei o Google Colab por ser prático e acessível de qualquer lugar.

--------------------------------------------------------------------------------------

**Estrutura do Código**

Funções organizadas por responsabilidade:

 -  get_channel_id: obtém o ID do canal

 -  get_highlight_videos: filtra vídeos com base no termo "highlights" e na data

  - get_video_details: coleta métricas detalhadas de cada vídeo

  - Tratamento de dados faltantes com .get() para evitar erros de execução

  - Cálculo de métricas derivadas, como taxa de curtidas e engajamento

  - Exportação final em formato .xlsx para análise posterior no Power BI

--------------------------------------------------------------------------------------


**Principais Análises**

   - Top 10 vídeos com maior número de visualizações

   - Vídeos com maior taxa de curtidas

  - Comparativo entre total de visualizações e inscritos

  - Engajamento geral dos vídeos ao longo do tempo

  - Comparação entre anos (2023 x 2024)

   --------------------------------------------------------------------------------------


**Decisões Técnicas**

**API do YouTube**
  - Utilizei a biblioteca googleapiclient.discovery para consumir a API do YouTube, que permitiu acessar informações do canal oficial da Fórmula 1 com segurança e eficiência.
   
  - A autenticação foi realizada por meio de uma chave da API armazenada diretamente no script, mantendo o acesso simples durante os testes.
   
  - Usei parâmetros como channelId, publishedAfter, q="highlights" e type="video" para refinar a busca e coletar apenas os vídeos relevantes, como os highlights de corridas.
   
  - Criei funções específicas como get_channel_id, get_highlight_videos e get_video_details para modularizar e organizar melhor o processo de coleta.

**Visualização e Dashboard**
   Toda a visualização dos dados foi feita no Power BI, por meio de dashboards interativos que permitem analisar os dados por ano, por engajamento e por vídeo.
   
   Salvei os dados no formato Excel (.xlsx) para facilitar a importação no Power BI e permitir atualizações manuais rápidas.
   
   Priorizei gráficos que comparam visualizações, curtidas e comentários, além de métricas como taxa de curtida e engajamento, possibilitando análises completas.
   
   A escolha pelo Power BI se deu pela flexibilidade de filtros, interatividade e facilidade de uso.

**Organização do Código**

  - Separei o código em funções modulares para tornar o processo de coleta mais organizado e reutilizável.
   
  - Cada função tem uma responsabilidade única (ex: coletar dados do canal, buscar vídeos, detalhar vídeos), o que facilita a leitura e manutenção.
   
  - Trabalhei com Google Colab por sua acessibilidade e por permitir continuar o projeto de qualquer lugar com praticidade.
   
  - Usei tratamento de erros com .get("campo", "Não disponível") para evitar falhas quando a API não retorna algum dado (como likes ou comentários).

**Processamento de Dados**
  - Utilizei a biblioteca pandas para organizar os dados coletados em DataFrames, o que facilitou a limpeza, manipulação e exportação dos dados.
   
  - Realizei transformações como ordenação por visualizações ou taxa de curtida, e adicionei métricas derivadas como:
   
  - Taxa de Curtida (likes / views)
   
  - Taxa de Engajamento (likes + comentários / views)
   
  - Optei por salvar os dados em Excel ao invés de banco de dados ou CSV para garantir compatibilidade com o Power BI e facilitar o compartilhamento.


 --------------------------------------------------------------------------------------

   

**Desafios Encontrados**


  - Compreensão da lógica da API: A documentação exigiu estudo detalhado para entender como extrair os dados certos.
   
  - Excesso de dados irrelevantes: Foi necessário aplicar filtros inteligentes para manter apenas os vídeos relacionados às corridas.
   
  - Integração com o Power BI: Ajustei o formato e estrutura dos dados exportados para uma visualização clara e eficiente no dashboard.
   
  - Limites da API: Lidei com cotas diárias de requisições, otimizando chamadas para não ultrapassar o limite.
   
  - Tratamento de dados incompletos: Alguns vídeos não apresentavam todos os dados esperados (curtidas, comentários), o que exigiu lógica extra de tratamento.
   
   o.














