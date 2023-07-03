#### Uma ideia é fazer um robo de scalper no Canal_Regress 8Pt
- um scalper de 80 pontos que vende no fechamento acima e sai no fechamento abaixo
- se colocar heikinash no 8 pt será que ele pega pernadas

### 

#### Estratégia NOVA Gradiente no Bot_Canal_Regress
- Colocar trailing stop (tem na Bot_Canal_Regress)

#### Estratégia Scalper Canal Regress 265 periodos 1,70
- dos extremos para o meio da para buscar 8 corpos a favor (8*40) no 8Pt
- pernadas no 8pt chegam 500pts retornos des 300
- no retorno da para pegar 6 (6*40) corpos a favor no 8Pt
- dá para colocar um stop do SellPrice + 3 corpos


Stop Loss - 160 do BuyPrice 
ou se ((Fechamento - BuyPrice) > 100pts) e (SinalVenda = True)

-- dá colocar uma flag se andou 5 box a favor colocar o stop loss se voltar 5.
-- Outra ideia que pode ser é ver qual a foi a mínima dos últimos 5 candles se voltar 160 pontos deste ponto seria um bom stop?



#### Minimas
- colocar 3 compras na Bot_M2_Scalper50_Inverso apenas se a tendencia de duas tilson for verdadeira



#### Ideias para melhorar
- ValorDoPreço := Fechamento
- Acabou de comprar atribui BuyPrice para ValorDaCompra
- Se ValorDoPreço < 150pts do ValorDaPrimeiraCompra e estou comprado : Encerra tudo a mercado.
- Se Position = 2 colocar stolLoss 150pts atrás de ValorSegundaCompra
- Sniper hora neotrader pode ser a opção para encerrar as 1750

- Usar o sistema de flag para zerar a variavel segunda compra e demais
#### Material para iniciantes:


https://neotraderbot.com/docs/material-iniciantes/programando-estrategias/exemplos-de-codigos/ordens-administracao-trade/


close[1] é só do candle anterior do tempo grafico que esta usando... Utilize o Priorcote|0| Priorcote|1|pra maxima e minima do dia anterior .... Use Opend(1) e  Closed(1) pra retornar a abertura e o fechamento do dia anterior