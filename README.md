# Simulação de rompimento de barragem


## Introdução

As barragens são estruturas de concreto utilizadas de diversas formas em processos produtivos, energéticos, pesca e até mesmo recreação e lazer. Comumente no Brasil, devido à elevada disponibilidade de minérios e bacias hidrográficas, as barragens controlam o fluxo de água ou dejetos de forma artificial. São alguns tipos de barragens utilizadas:

- Barragens de terra batida
- Barragem de enroncamento com face de concreto
- Barragem de contraforte
- Barragem em arco

O rompimento de barragens é uma modalidade de desastres consideravelmente reincidente na história da humanidade e recente na história brasileira. Segundo Mota, dois são os principais fatores que podem ser apontados como causa primária desse evento, o advento de um fenômeno natural intenso responsável por abalar a estrutura da barragem ou o mau planejamento dessa estrutura. A simulação do comportamento do fluido em superfícies livres é importante para conhecer as características deste escoamento e posteriormente...

## Metodologia

Durante o início da simulação, é pré-determinado que o fluido está em confinamento entre duas colunas estabelecidas com condições de contorno em equílibrio hidroestático. Ao retirar as duas colunas pode-se avaliar variando o tempo o escoamento do fluido.

![3 materiais](https://user-images.githubusercontent.com/54566885/99905421-780dc780-2caf-11eb-9c28-c6ef66e3d48c.PNG)

Será utilizado o método Volume od Fluids (VOF) como modelagem de superfície livre em regime transiente. Optando pela forma implícita melhora-se a convergência da solução levando em consideração o equilíbrio parcial do gradiente de pressão e as forças do corpo nas equações do momento.

![2 multiphase model ](https://user-images.githubusercontent.com/54566885/99905508-efdbf200-2caf-11eb-9100-3ed3a6e17ff4.PNG)

Definindo as propriedades como massa específica e viscosidade do ar e água a serem simulados, bem como as fases primárias e secundárias. O ar é definido como fase primária e água como fase segundária.

![4 fase primaria sec](https://user-images.githubusercontent.com/54566885/99905424-793ef480-2caf-11eb-9fbb-20ba1872ef5b.PNG)

Em Operation Conditions coloca-se a pressão de operação e massa específica de operação, não admitindo variação de temperatura durante a operação e colocando a massa específica do fluido menos denso.

![5  operation conditions](https://user-images.githubusercontent.com/54566885/99905425-793ef480-2caf-11eb-8880-55482c91f973.PNG)

Nas condições de contorno defina-se a pressão de saída "pressure outlet" para a água, para reproduzir as condições ideais posteriormente ao rompimento da barragem, devemos anular qualquer ação de retorno do fluido, uma vez que não reversidade no escoamento do fluido.

![5 1pressure outlet](https://user-images.githubusercontent.com/54566885/99905426-79d78b00-2caf-11eb-9bcf-d98930faa032.PNG)

Nos métodos de solução, como o escoamento é transiente o acoplamento pressão velocidade é dado pelo algoritmo PISO, para a pressão utilizamos o PRESTO, para o momento o First Order Upwind. Podem ser determinados valores de relaxamento do fluido e quando o ciclo será executado no valor de terminação da pressão.

![6 solution controls](https://user-images.githubusercontent.com/54566885/99905427-79d78b00-2caf-11eb-99b6-686be516a8a3.PNG)

Para escolher o que será plotado na simulação de rompimento, foram escolhidos os seguintes critérios:

![8  residual monitors](https://user-images.githubusercontent.com/54566885/99905429-7b08b800-2caf-11eb-8e23-040d651ca2ba.PNG)

## Conclusão

Os resultados da simulação foram registrados alterando o intervalo de passos de tempo e fixando a quantidade máxima de interações da simulação.
![9 2 scaled](https://user-images.githubusercontent.com/54566885/99905434-7ba14e80-2caf-11eb-8369-1a790bac311c.PNG)

Plotando o vetor velocidade da mistura, temos o seguinte resultado:

![9 4 vector velocity](https://user-images.githubusercontent.com/54566885/99905439-7cd27b80-2caf-11eb-952f-6b57e3a5e6b1.PNG)

Plotando a massa de água ainda estática entre a barragem temos o seguinte resultado:

![12  concentração de agua inicio](https://user-images.githubusercontent.com/54566885/99905445-7e9c3f00-2caf-11eb-8806-82b1e36246a2.PNG)

Já para a concetração da água no instante final da simulação temos o deslocamento do fluido, fisicamente previsto.

![12  concentração de agua final](https://user-images.githubusercontent.com/54566885/99905444-7e03a880-2caf-11eb-9ae9-fa362a329638.PNG)

Atenta-se para as pressões do ar e água para no instante final da simulação, pós rompimento da barragem.

![11 pressao final ar](https://user-images.githubusercontent.com/54566885/99905442-7d6b1200-2caf-11eb-9b08-7b3079ead96b.PNG)

A importância do estudo do escoamento do rompimento é primordial para entendimento dos impactos sociais, ambientais e econômicos em casos de falhas construtivas na barragem. Além das considerações aqui feitas para simulação é necessário caracterização do solo à jusante da barragem, uma vez que as declividades e largura de escoamento também influenciam o escoamento. Por conseguinte, as condições meteorólogicas no momento do rompimento também interferência os resultados finais da simulação.
