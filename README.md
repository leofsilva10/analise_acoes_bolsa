# analise_acoes_bolsa
<b>PROJETO: ANÁLISE DE COTAÇÕES DE AÇÕES PARA INVESTIMENTO</b>

Já pensou em investir em ações na Bolsa de Valores?

Esse projeto de análise tem por objetivo identificar as melhores ações para investimento tendo como base o histórico das cotações dos ativos.

Fonte de dados: https://br.financas.yahoo.com

Segue abaixo o passo-a-passo do processo de análise dos dados.

<b>Importação dos Dados</b>

Importando biblioteca Yahoo Finance.

Definindo os ativos a serem analisados: Índice Bovespa, Petrobras, Itaú, BB, Bradesco, Dólar.

Obtendo cotações.

<b>Tratamento dos Dados</b>

Excluindo colunas desnecessárias.

Removendo valores nulos.

<b>Análise Gráfica</b>

Analisando a tendência dos preços.

![image](https://github.com/leofsilva10/analise_acoes_bolsa/assets/114931860/3bafde65-64fc-4582-9ba9-776207380752)

As médias móveis indicam a direção a tendência, sendo a média móvel de 20 períodos a que melhor representa esse comportamento. Analisando a MM20 no gráfico abaixo, observamos que a inclinação da média para baixo sugere venda, enquanto a inclinação para cima sugere compra do ativo.

![image](https://github.com/leofsilva10/analise_acoes_bolsa/assets/114931860/704c777e-53d0-460e-809b-22adfb0a1351)

Analisando a variação diária nos preços.

![image](https://github.com/leofsilva10/analise_acoes_bolsa/assets/114931860/a124d38d-08f7-46f8-b556-76ac930fcb87)

Analisando a Distribuição das cotações.

![image](https://github.com/leofsilva10/analise_acoes_bolsa/assets/114931860/86c80b4e-2dc3-4938-8252-7fc7e07383dc)

No gráfico acima observamos que os valores dentro da normalidade estão compreendidos abaixo da linha azul (curva normal) de cada gráfico. Já os valores muito extremos (distantes da curva normal) podem ser "outliers", ou seja, dados discrepantes.

Analisando as correlações através da Matriz de Dispersão:
- Na diagonal é possível ver a variação de preços de cada ativo.
- Fora da diagonal é possível ver como as ações se correlacionam entre si.

![image](https://github.com/leofsilva10/analise_acoes_bolsa/assets/114931860/1795e959-00a9-47e2-ba33-d6a447838b64)

Verificando a correlação entre os ativos.

![image](https://github.com/leofsilva10/analise_acoes_bolsa/assets/114931860/2f0d4dc6-8776-41b0-aadf-afe39934f9b8)

Resultados da Análise:
1. Analisando a tabela acima, observamos uma correlação positiva muito forte (acima de 0.9) entre o Índice Bovespa (BVSP) e o Itaú (ITUB4.SA), o que indica que altas nas ações do Itaú podem sugerir altas também no Índice Bovespa.
2. Podemos observar também correlações positivas fortes (entre 0.7 e 0.9) entre o Índice Bovespa (BVSP) e Petrobras (PETR4.SA), Bradesco (BBDC4.SA) e BB (BBAS3.SA), sugerindo que a alta em qualquer um dos últimos 3 ativos pode levar a altas no Índice Bovespa.
3. Pode-se verificar também uma correlação negativa forte (menor que -0.9) entre o Índice Bovespa, as ações das empresas (Itaú, Bradesco e BB) e o dólar. É possível observar que altas na cotação do dólar levam à quedas nas cotações tanto do Índice Bovespa quanto das ações das empresas citadas. Por outro lado, quedas no dólar podem gerar altas tanto no Índice quanto nas empresa.

Obs: as classificações das correlações foram realizadas de acordo com o "Coeficiente de correlação de Pearson".

Realizando a análise de Risco X Retorno para cada ativo.

![image](https://github.com/leofsilva10/analise_acoes_bolsa/assets/114931860/52194743-5eef-41c6-8769-7d55006e6025)

Resultado da Análise:

De acordo com o gráfico acima, percebemos que Itaú (verde) e BB (preto) são os melhores ativos para se investir, pois apresentam o menores riscos e o maiores retornos.

Já Bradesco (laranja) e Petrobras (azul) não apresentam relações "risco x retorno" tão interessantes que justifiquem um investimento no momento.






