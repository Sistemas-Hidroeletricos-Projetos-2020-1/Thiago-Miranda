# Simulação de rompimento de barragem


## Introdução

As barragens são estruturas de concreto utilizadas de diversas formas em processos produtivos, energéticos, pesca e até mesmo recreação e lazer. Comumente no Brasil, devido à elevada disponibilidade de minérios e bacias hidrográficas, as barragens controlam o fluxo de água ou dejetos de forma artificial. São alguns tipos de barragens utilizadas:

- Barragens de terra batida
- Barragem de enroncamento com face de concreto
- Barragem de contraforte
- Barragem em arco

O rompimento de barragens é uma modalidade de desastres consideravelmente reincidente na história da humanidade e recente na história brasileira. Segundo Mota, dois são os principais fatores que podem ser apontados como causa primária desse evento, o advento de um fenômeno natural intenso responsável por abalar a estrutura da barragem ou o mau planejamento dessa estrutura. A simulação do comportamento do fluido em superfícies livres é importante para conhecer as características deste escoamento e posteriormente...

## Objetivo

## Metodologia

Durante o início da simulação, é pré-determinado que o fluido está em confinamento entre duas colunas estabelecidas com condições de contorno em equílibrio hidroestático. Ao retirar as duas colunas pode-se avaliar variando o tempo o escoamento do fluido.

![3 materiais](https://user-images.githubusercontent.com/54566885/99905421-780dc780-2caf-11eb-9c28-c6ef66e3d48c.PNG)

Será utilizado o método Volume od Fluids (VOF) como modelagem de superfície livre em regime transiente. Optando pela forma implícita melhora-se a convergência da solução levando em consideração o equilíbrio parcial do gradiente de pressão e as forças do corpo nas equações do momento.

![2 multiphase model ](https://user-images.githubusercontent.com/54566885/99905508-efdbf200-2caf-11eb-9100-3ed3a6e17ff4.PNG)

Definindo as propriedades como massa específica e viscosidade do ar e água a serem simulados, bem como as fases primárias e secundárias. O ar é definido como fase primária e água como fase segundária.

![4 fase primaria sec](https://user-images.githubusercontent.com/54566885/99905424-793ef480-2caf-11eb-9fbb-20ba1872ef5b.PNG)




## Conclusão
