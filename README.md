# Detecção de Fraude

[Notebook](https://github.com/RailanDeivid/ML_Deteccao_fraude/blob/main/Notebook/Detec_Fraude.ipynb)


A base de dados qua será usadas paras as analises e modelagem faz parte de de um conjunto de dados do Kaggle chamada [Fraud Detection Example](https://www.kaggle.com/gopalmahadevan/fraud-detection-example) e ela tem uma fração de dados do [PaySim](https://github.com/EdgarLopezPhD/PaySim), um simulador de dados financeiros feito exatamente para detecção de fraude.


## Referencias

Os aprendizados aplicados nesse projeto fazem parte de um dos curso ministrados pela [Sthefanie Monica Premebida](https://www.linkedin.com/in/sthefanie-monica/) junto a [Alura](https://cursos.alura.com.br/course/modelos-preditivos-dados-deteccao-fraude).


## Conjunto de dados

**Variáveis do dataset**

* **step** - mapeia uma unidade de tempo no mundo real. Neste caso, 1 passo é 1 hora de tempo. Total de etapas 744 (simulação de 30 dias).

* **type** - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER. 
(caixa-de-entrada, caixa-de-saida, débito, pagamento e transferência)

* **amount** - valor da transação em moeda local.

* **nameOrig** - cliente que iniciou a transação

* **oldbalanceOrg** - saldo inicial antes da transação

* **newbalanceOrig** - novo saldo após a transação

* **nameDest** - cliente que é o destinatário da transação

* **oldbalanceDest** - destinatário do saldo inicial antes da transação. 
Observe que não há informações para clientes que começam com M (Comerciantes).

* **newbalanceDest** - novo destinatário do saldo após a transação. Observe que não há informações para clientes que começam com M (Comerciantes).

* **isFraud** - São as transações feitas pelos agentes fraudulentos dentro da simulação. Neste conjunto de dados específico, o comportamento fraudulento dos agentes visa lucrar ao assumir o controle das contas dos clientes e tentar esvaziar os fundos transferindo para outra conta e depois sacando do sistema.

* **isFlaggedFraud** - O modelo de negócios visa controlar transferências massivas de uma conta para outra e sinaliza tentativas ilegais. Uma tentativa ilegal neste conjunto de dados é uma tentativa de transferir mais de 200.000 em uma única transação.


**OBS: Como o objetivo deste projeto é usar ML para detecção de fraude, não foquei em fazer um analise exploratoria manual. optei por usar o `Pandas Profiling`para fazer as analises de variáveis.**
