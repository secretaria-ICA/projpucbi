### Otimização na Contrução e Envio de Informes Mensais de Fundos

Aluno: [Rafael Alcântara da Silva](https://github.com/alcraf)
Orientador: [Felipe Borges](https://github.com/FelipeBorgesC)

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

- [Link para o código](https://github.com/Projeto_Rafael_Alcântara_da_Silva.xlsm)

---

 ## Resumo

O presente trabalho surgiu da necessidade de otimizar o envio dos informativos mensais de fundos de investimento realizados por uma gestora de fundos. 
Atualmente são construídos e enviados via e-mail ou publicado no site da gestor em torno de 700 informativos. Os relatórios são construídos e enviados de forma manual através de Excel.
Os informes podem ser dividos em fundos de ações, multimercado e renda fixa, tendo ainda uma subvidisão por cada segmento de clientes, a saber varejo e private. E ainda surgiu a necessidade um terceiro segmento que seriam para os fundos exclusivos.
Dentre as inúmeras necessidades dos clientes e distribuidor a mais demandada é a velocidade na confecção e envio dos relatórios até no máximo no décimo dia útil do mês subsequente à data base.
Ainda, cabe destacar que existem prioridades de tipos de fundos e segmentos. Ou seja, alguns tipos de informativos devem ser encaminhados com a máxima prioridade sendo o prazo fatal o quinto dia útil do mês.
Então, para a solução do problema buscou-se a utilização de uma modelagem de otimização na ordem de construção e envio dos informativos obedecendo as prioridades apresentadas ao time que executa a atividade.
O resultado foi a entrega de todos os informes num prazo aceitável e desejável pelos clientes e distribuidor, considerando a mão-de-obra hoje disponível pelo time.

Abstract 

The present work arose from the need to optimize the sending of monthly information on investment funds carried out by a fund manager.
Currently, around 700 newsletters are built and sent via e-mail or published on the manager's website. Reports are built and sent manually through Excel.
The reports can be divided into equity, multimarket and fixed income funds, with a subdivision for each customer segment, namely retail and private. And yet the need arose for a third segment that would be for exclusive funds.
Among the numerous needs of customers and distributors, the most demanded is speed in preparing and sending reports up to the 10th business day of the month following the base date.
It is also worth noting that there are priorities for types of funds and segments. That is, some types of information must be sent with the highest priority, with the deadline being the fifth business day of the month.
So, in order to solve the problem, we tried to use an optimization model in the order of construction and sending of the newsletters obeying the priorities presented to the team that executes the activity.
The result was the delivery of all reports within an acceptable and desirable time frame for customers and distributors, considering the workforce available today by the team.

1. Introdução

xxxxxxxxxxxxxxxxxxxxxxxxxxxx
Os fundos foram classificados em ações, multimercado e renda fixa para os segmentos Varejo e Private. Além destes existem os fundos exclusivos com a mesma classificação (ações, multimercado, renda fixa)


2. Modelagem

Na busca de uma entrega mais assertiva e rápida dos informativos mensais utilizou-se a ferramenta solver do excel,considerando as seguintes premissas/restrições:

   a) O trabalho dever ser concluído até o 10º dia útil do mês;
   b) A construção dos informativos só pode ser iniciada a partir do 3º dia útil, data em que todos os insumos estão disponíveis;
   c) Fundos de Ações e Multimercado do segmento Private e Multimercado e Renda Fixa do segmento Varejo devem ser entregues até o 5º dia útil;
   d) Força total de trabalho consiste em 3 colaboradores disponíveis para a execução do trabalho durante 5 horas/dia; e
   e) O total de informativos a serem construídos é de 675 (data base fevereiro/22)

Na construção do modelo foram consideradas os seguintes cenários/modelagens:
   i)   Para o tempo total despendido para a construção de cada relatório foi utilizado a fórmula ALEATÓRIOENTRE(), onde os parametros foram: mínimo 80% da média para o tipo de fundo e máximo 120%;
   ii)  Foi gerado um índice de prioridade para cada tipo de fundo, considerando as necessidades comerciais hoje existentes;
   iii) As células variáveis do modelo solver são referentes a quantidade de informes de cada tipo que serão construídas/enviadas por dia;
   iv)  Posteriormente foi criada uma tabela para calcular o total de minutos gastos por dia para a construção e envio dos informes, a fim de obedecer a capacidade operacional do time;
   v)   Em seguida, construiu-se um índice multiplicando a prioridade pelo tempo a fim de se chegar a uma variável objetivo a ser utilizada pelo Solver.
   vi)  No modelo Solver foram utilizadas, então, as seguintes premissas:
        - Todas as variáveis deverão conter números inteiros;
        - Todas as variáveis deverão ser maior que 1;
        - Nos 4º e 5º dia úteis será consumida toda a capacidade operacional do time;
        - O total construído em determinado dia deve ser maior ou igual ao dia imediatamente seguinte;
        - É realizada a checagem no modelo se todos os informes sugeridos pelo solver via variável corresponde ao total de informes a serem enviados;
        - Construída, ainda, uma restrição para que determinados tipos sejam enviados até o 5º dia útil.
   vii)  O modelo utilizado foi para maximizar a função objetivo utilizando o método de solução Evolutionary
        
3. Resultados

xxxxxxxxxxxxxxxxxxx

4. Conclusões

O modelo se mostrou bastante interessante e assertivo, tendo em vista que proporcionou ao gestor uma melhor alocação da mão-de-obra disponível para que, assim, sejam realizadas as construções e envios de todos os informes mensais num prazo desejado por todos os demandantes.
Logo, tendo em vista a otimização da mão-de-obra do setor, o gestor poderá utilizar as horas então economizadas para a realização de diversas outras atividades sob responsabilidade do time.

Matrícula: 201.110.700

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*