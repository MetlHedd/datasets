# Dados sobre o COVID19 em São Carlos

## Detalhes
O arquivo `dataset.csv` contém os dados distribuidas pela Prefeitura de São Carlos em seus orgãos oficias de comunicação (instagram e telegram) sobre a epidemia do COVID19.

### Convenções utilizadas
- **Casos suspeitos notificados ou em isolamento domicial:** A prefeitura identificava casos (a partir de 25/03/2020 até 05/04/2020) suspeitos com sintomas leves do vírus primeiramente como "casos suspeitos em isolamento domilicar", a partir 27/03/2020 começou a dar os casos suspeitos tanto de COVID19 como Sindrome Gripal (já que em seus sintomas leves eles possuem suas semelhanças), como unicamente como "Isolamento Domicial (Sindrome Gripal)". Dias depois (especificamente 11/04/2020) a prefeitura adotou a forma de distribuir os dados de forma separada, como: "Sindrome Gripal (notificações)" e "Síndrome Gripal (ainda em isolament
o domiciliar)", é importante que seja notato que essa convenção foi utilizada de acordo com o protocolo do ministério de saúde.
- - No dataset esses dados são apresentados de forma unificada na coluna: `FLU-NOTISO`;
- - Casos suspeitos em isolamento domiciliar e notificações de sindrome gripais foram sumados juntos unicamente para essa coluna, junto com os casos suspeitos em isolamento domiciliar de COVID19.
- **Casos em internados, em enfermaria e UTI:** apenas a partir de 07/04/2020 a prefeitura começou a disponibilizar os casos separados nessa três categorias, anteriormente (por falta de presença de dados, ou por não ter nenhum suspeito nesses casos) a prefeitura disponibilizava apenas o número de internados e agora é divulgado nas três categorias.

### Colunas
- **Data:** Apresenta a data dos dados presentes na linha atual;
- **CV19-CSI:** Casos suspeitos em interação de COVID19;
- **CV19-CSE:** Casos suspeitos em enfermaria de COVID19;
- **CV19-CSUTI:** Casos suspeitos em UTI de COVID19;
- **CV19-CONF:** Casos confirmados de COVID19;
- **CV19-DESC:** Casos descartados de COVID19;
- **CV19-MINV:** Óbitos em investigação de COVID19;
- **CV19-MDESC:** Óbitos descartados de COVID19;
- **CV19-MCONF:** Óbitos confirmados de COVID19;
- **FLU-NOTISO:** Casos suspeitos de Sindrome Gripal (pode ocorrer de ser COVID19, já que o teste não é efetuado nesses casos).

### Erros encontrados no dataset
Como os dados são colocados de forma manual é possível que se haver um error do operador na hora de inserir novos/atualizar dados.
- 16/04/2020: A ordem das colunas **CV19-MDESC** e **CV19-MCONF** estava incorreta (deveria ser ao contrário), corrigdo em: https://github.com/MetlHedd/datasets/commit/e0ba00b39c0c50df05de2f10d8ee8570c2b88e73.
- 19/04/2020, 20/04/2020 - Em 19/04 a prefeitura notificou o n° de óbitos descartados por COVID19 como 11, no dia seguinte mudou esse número para 10, para o dia 19/04 foi alterado para 10 o n° de óbitos descartas, a prefeitura não notificou a causa do erro nos dados.

### Ultima atualização
Atualizações são feitas diaramente, normalmente no período noturno.

**Data da última atualização:** 27/04/2020
