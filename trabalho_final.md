Trabalho Final
================
Julia Marques, Letícia Dufloth, Pedro Paulo Polastri e Rodrigo Prates
18/07/2020

### Introdução

O presente trabalho se configura como o trabalho final da disciplina de
Análise e Visualização de Dados com R, do Curso Superior de
Administração Pública da Escola de Governo Professor Paulo Neves de
Carvalho da Fundação João Pinheiro, referente ao primeiro semestre de
2020. Neste trabalho, temos por objetivo analisar dados relativos às
bolsas concedidas pelo ProUni (Programa Universidade para Todos), bem
como o perfil de seus beneficiários.

O ProUni é um programa do Ministério da Educação que concede bolsas de
estudo em instituições de ensino superior particulares. Para as bolsas
integrais, os alunos precisam comprovar renda familiar bruta mensal per
capita de até 1,5 salário mínimo. Para as bolsas parciais (50%), os
estudantes têm que comprovar renda familiar bruta mensal per capita de
até 3 salários mínimos. Além disso, é necessário que o aluno não tenha
diploma de ensino superior, e que tenha realizado o Exame Nacional do
Ensino Médio (ENEM) mais recente (BRASIL, 2020).

As questões que orientarão as análises do presente trabalho são:

  - Qual o perfil demográfico dos bolsistas, no que se refere a gênero,
    raça, faixa etária e existência de deficiência?

  - Como se dá a distribuição geográfica dos bolsistas por unidade
    federativa?

  - Quais os 10 cursos que recebem mais bolsistas ProUni?

### Perfil dos bolsistas

Os dados disponíveis na base permitem fazer análises interessantes
quanto ao perfil dos beneficiários acerca do sexo, da faixa etária, da
raça e da existência de deficiência física.

No que se refere à faixa etária, foi necessário criar dois tipos de
gráficos. Isso porque verificou-se a existência de um outlier -
constava na base de dados uma pessoa com 11 anos de idade, sendo que
todos os outros beneficiários tinham 16 anos ou mais. Sendo assim,
primeiramente será mostrado o gráfico com a inclusão do outlier e,
posteriormente, será exibido o gráfico excluindo o outlier, para
evidenciar a mudança na visualização.

Ressalta-se que, nos gráficos em que a variável faixa etária não estiver
sendo analisada, o outlier será incluído, pois pressupõe-se que a única
informação errada referente a essa pessoa é a idade.

    ## png 
    ##   2

    ## png 
    ##   2

Observa-se que a maior parte dos beneficiários está na faixa etária
entre 16 a 20 anos, e o número de beneficiários a cada faixa etária
seguinte vai diminuindo.

Também é possível fazer visualizações a partir da combinação da variável
faixa etária com a variável sexo:

    ## png 
    ##   2

    ## png 
    ##   2

Nota-se, nesses gráficos, um comportamento semelhante aos gráficos
anteriores, sendo que o número de mulheres por faixa etária é quase
sempre maior do que o de homens. Os homens predominam apenas nas faixas
etárias de 66 a 70 anos e na de 71 anos ou mais.

No que se refere à variável “sexo” analisada individualmente, observa-se
a predominância de mulheres beneficiárias:

    ## png 
    ##   2

Ao relacionar as variáveis sexo e raça, observamos que as mulheres
beneficiárias predominam em todas as raças, exceto quando a raça não foi
informada (nesse caso, são 4 homens e 1 mulher):

    ## png 
    ##   2

Sendo assim, percebe-se que a maior parte dos beneficiários é mulher
parda, seguida de mulheres brancas, homens pardos e homens brancos.

Ao analisar a variável raça isoladamente, verifica-se que a raça parda é
a predominante dentre os beneficiários, seguida pela raça branca, preta,
amarela e indígena:

    ## png 
    ##   2

Quanto à análise de dados referentes aos beneficiários com deficiência
física, nota-se que eles são uma pequena parcela do total de
beneficiários:

    ## png 
    ##   2

Dessa forma, entende-se ser interessante filtrar somente os
beneficiários com deficiência para fazer algumas análises combinadas
com outras variáveis. No que se refere à raça, vemos que a predominante
dentre os beneficiários é a branca, seguida pela parda, preta e amarela:

![](trabalho_final_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

### Referências

BRASIL. Ministério da Educação. **ProUni - Programa Universidade Para
Todos**. Disponível em: <http://prouniportal.mec.gov.br/>. Acesso em 18
jul. 2020.
