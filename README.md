# youtube_API
Olá! Recentemente, realizei uma análise utilizando a API do YouTube, e foi uma experiência incrível! Através dela, consegui explorar diversos dados sobre o canal oficial da Fórmula 1 e suas playlists. Esse projeto me permitiu aprimorar significativamente meus conhecimentos tanto em Python quanto em Power BI. 

Este projeto tem como objetivo coletar, analisar e exportar dados dos vídeos de highlights publicados no canal oficial Fórmula 1 no YouTube durante o ano de 2024. Através da API do YouTube, foram coletadas métricas como visualizações, curtidas, comentários e engajamento, permitindo análises comparativas entre os vídeos.


#  Como Rodar o Projeto  ?  

1. Primeiro passo é instale dependencias para ultilizar a API do google 

    **pip install google-api-python-client pandas openpyxl**

2. O segundo passo é importar a função ue é usada para construir uma conexão com a API do Google 

    **from googleapiclient.discovery import build**

 3. O terceiro passo consiste em você colocar a sua chave da API do youtube 
  

4. O quarto passo é  criar o cliente da API do YouTube

  **youtube = build("youtube", "v3", developerKey='AIzaSyD877MaanmjiisQFwP9AsmE6QAhze7vwjc')**


5. E quinto e ultimo passo é instalar a biblioteca pandas e a openpyxl para importação 

   **pip install pandas openpyxl**






Ultilizei o google colab para fazer minhas análises pois foi mais fácil pra mim porque eu pude acessar meu projeto e desenvolver ele em qualquer lugar. 
Fiz Separação de funções para melhorar a organização do código.
Ultilizei  parâmetros como channelId, publishedAfter, **q="highlights"** para análises específicas.
Criei funções como get_channel_info, get_highlight_videos, get_video_details para modularizar o código, facilitando a manutenção e reutilização.
Usei .get("campo", "Não disponível") para tratar situações em que a API não retorna certas métricas (como likes ou comentários).
Priorizei métodos como channels().list, search().list e videos().list para obter dados do youtube.
Optei por salvar os dados em Excel para facilitar o uso no Power BI, então fiz o máximo de análise que eu pude no google colab.





**Principais análises Feitas**

Informações gerais do canal (número de inscritos, visualizações, vídeos, descrição).
Top 10 vídeos mais visualizados.
Comparação entre inscritos e visualizações.
Identificação de vídeos com títulos que incluem "highlights".








Apesar de ter sido um projeto em que consegui aprimorar meus conhecimentos em Python e no Power BI, enfrentei alguns desafios importantes durante o desenvolvimento. Em determinado momento, comecei a me confundir com os dados que estava gerando estava coletando muitas informações sem entender completamente o que cada dado representava, o que acabou dificultando o meu entendimento do código.
Além disso, tive dificuldade em entender a lógica de funcionamento da API do YouTube, foi necessário estudar a documentação e ver tutoriais realizar de forma correta e extrair os dados que realmente fariam sentido para a análise.
Outro ponto que me gerou confusão foi a organização dos dados para integração com o Power BI como acabei fazendo todo a análise no python na hora de passar para o BI fiquei um pouco perdida com as informações que tinha gerado e tive que ajustar o formato e estrutura dos dados para que a visualização no Power BI fosse realmente eficiente e útil para gerar insights.


















