
#### Minimas
- Colocar trailing stop (tem na Bot_Canal_Regress)
- Não comprar acima ifr 60 não vender abaixo ifr35
- Ou no lugar do ifr colocar a flag para não comprar duas vezes na mesma direção até porque o trailing stop deve aproveitar a maior parte do movimento

- colocar 3 compras na Bot_M2_Scalper50_Inverso apenas se a tendencia de duas tilson for verdadeira

#### Estratégia NOVA Gradiente no Bot_Canal_Regress

#### Estratégia NOVA WapBands com estocástico lento de 14 (Stormer)
- Quadrante á a região entre wapBands
- Se quadrante anterior é igual ao atual, se estocástico virar pra cima compra.
- 10r e 5 minutos // alvo duas vezes o risco // pode talves usar o true range para definir o alvo

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