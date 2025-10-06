# 6_PFC_Boost_Converter

O objetivo deste trabalho foi o design, simulação, conceção e teste de um protótipo funcional de um conversor de potência, a apresentar no final do semestre. No caso do nosso grupo, foi-nos atribuída a responsabilidade de desenvolver um Conversor CA-CC do tipo Boost PFC.

O conversor contava, primeiramente, com um estágio CA-CC, constituído por um transformador abaixador e uma ponte retificadora de díodos (retificação síncrona), seguido de um estágio CC-CC, baseado na topologia de um conversor Boost com carga resistiva. Este último operava sob um método de controlo denominado PFC (Power Factor Correction), que tinha como objetivo corrigir o fator de potência e reduzir a potência reativa no sistema.

O nosso grupo decidiu implementar um protótipo em larga escala, sem recurso ao desenho de PCB. Para tal, foi utilizada uma tábua de madeira onde foram fixados os principais componentes:

1. Um transformador 230 V / 30 V, responsável por reduzir a tensão da rede;
2. Um disjuntor tetrapolar (utilizado como bipolar) para proteção e acionamento da rede elétrica do protótipo;
3. Um módulo de ponte retificadora (ref. GBPC40);
4. Uma protoboard com o estágio de potência e o circuito de acionamento (gate driver);
5. Dois módulos de sensores de tensão de efeito Hall, desenhados no laboratório da Universidade (GEPE);
6. Um módulo de sensor de corrente de efeito Hall, desenhado no laboratório da Universidade (GEPE);
7. Uma caixa dedicada ao acondicionamento de sinal, desenhada no laboratório da Universidade (GEPE);
8. Uma placa de desenvolvimento NUCLEO-F767ZI;
9. Um indutor;
10. E, externamente à tábua, uma carga resistiva.

Todo o design foi previamente concebido e verificado em ambiente de simulação (PSIM), tanto a nível de hardware de potência como da teoria de controlo aplicada. Importa destacar que o controlo era não linear (o sinal na gate do IGBT não apresentava frequência fixa), sendo gerado pela comparação entre a corrente de referência e a corrente medida: se a corrente medida fosse inferior à de referência, o sinal na gate era “1”; caso contrário, era “0”. O conversor era assim controlado pela corrente de referência no lado da rede e pela tensão de referência no barramento CC, tendo como base a teoria de Fryze-Buchholz-Depenbrock (FBD).

O circuito de potência (Boost) foi montado e soldado numa protoboard, interligado por conectores aos restantes componentes fixados na tábua de madeira.

Os resultados obtidos foram bastante satisfatórios e promissores, especialmente tratando-se de um protótipo implementado em larga escala.

Neste repositório, é possível encontrar:

Um PDF com toda a documentação do projeto: design, simulação e conceção.

Dois vídeos que mostram o resultado geral do protótipo.

Um ficheiro PPT com a apresentação do projeto.

Um ficheiro ZIP com o código em C utilizado para a STM32.

Um PDF com anexos relativos à configuração da STM32.

Uma pasta com fotos dos principais elementos constituintes do protótipo.

Este trabalho foi fundamental para consolidar conhecimentos em diversas áreas da eletrónica e da automação, unindo conceitos analógicos e digitais. Foi exigente e desafiante, mas extremamente gratificante.

Um grande obrigado aos colegas que me acompanharam nesta jornada: Diego Brandão, João Santos, João Martins e Rui Pedroso.
