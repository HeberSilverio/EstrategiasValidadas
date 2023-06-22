Inicio
  Se (Fechamento > Abertura) e (Minima < Abertura[1]) e (Fechamento > MediaExp(30,Close)[1]) e (Fechamento > HILOACTIVATOR(37)[1]) então
    PaintBar(clVerdeLimão)
  Senão Se (Fechamento < Abertura) e (Maxima > Abertura[1]) e (Fechamento < MediaExp(30,Close)[1]) e (Fechamento < HILOACTIVATOR(37)[1]) então
    PaintBar(clPreto)
  Senão Se (Fechamento > MediaExp(30,Close)) e (Fechamento > HILOACTIVATOR(37)[1]) então
    PaintBar(clTeal)
  Senão Se (Fechamento < MediaExp(30,Close)) e (Fechamento < HILOACTIVATOR(37)[1]) então
    PaintBar(clMarrom);
Fim;



e (Fechamento > HILOACTIVATOR(37)[1])
e (Fechamento < HILOACTIVATOR(37)[1])

//MarteloTor
Inicio
  Se (Fechamento > Abertura) e (Minima < Abertura[1]) então
    PaintBar(clVerde)
  Senão Se (Fechamento < Abertura) e (Maxima > Abertura[1]) então
    PaintBar(clVermelho)
  Senão Se (Fechamento > MediaExp(20,Close)) então
    PaintBar(clVerde)
  Senão Se (Fechamento < MediaExp(20,Close)) então
    PaintBar(clVermelho);
Fim;


//MarteloThorHB

Inicio
  Se (Fechamento > Abertura) e (Minima < Abertura[1]) e (Fechamento > MediaExp(20,Close)) então
    PaintBar(clVerdeLimão)
  Senão Se (Fechamento < Abertura) e (Maxima > Abertura[1]) e (Fechamento < MediaExp(20,Close)) então
    PaintBar(clVermelho)
  Senão Se (Fechamento > MediaExp(20,Close)) então
    PaintBar(clTeal)
  Senão Se (Fechamento < MediaExp(20,Close)) então
    PaintBar(clMarrom);
Fim;


//MarteloThorPlus
Inicio
  Se (Fechamento > Abertura) e (Minima < Abertura[1]) e (Fechamento > MediaExp(30,Close)[1]) então
    PaintBar(clVerdeLimão)
  Senão Se (Fechamento < Abertura) e (Maxima > Abertura[1]) e (Fechamento < MediaExp(30,Close)[1]) então
    PaintBar(clPúrpura)
  Senão Se (Fechamento > MediaExp(30,Close)) então
    PaintBar(clTeal)
  Senão Se (Fechamento < MediaExp(30,Close)) então
    PaintBar(clMarrom);
Fim;

//  IMPEDIMENTOS
NÃO COMPRAR
- Abaixo do Hilo Vermelho
- Histograma abaixo de zero (MESMO QUE SEJA VERDE)

(Martelos longe da média de 21 podem ser final de movimento ou levar a movimentos pequenos. A menos que a tendência esteja muito forte)
NÃO VENDER COM O INVERSO


// STOP
Stop inicial é do tamanho de 3 corpos.
- Apos andar vira stop movel 25 pontos abaixo da mínima dos dois últimos.


// Operacional do dólar
Hilo Activator 7 períodos
Descendo triscou no verde vende
Subindo triscou no vermelho compra
Alvo de 6pts
Stop de 5pts 