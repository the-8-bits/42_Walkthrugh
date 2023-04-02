# 42_Walkthrugh

*(future eng translation)*

O propósito da existência desse repo, assim como muitos outros, é documentar as expreriencias vividas dentro
da *42 (Porto)*.

---

|*|**Í N D I C E**
|-  |-|
|i  |[História](#i-História)|
|ii |[Dinâmica](#ii-Dinâmica)|
|iii|[Listas](#iii-listas)|
|iv |[Exames](#iv-exames)|


## i-História
Chegando aqui já deve ter ouvido falar de onde vem a inspiração para o nome e a ideia da Escola, como bons
nerds que somos, provavelmente ouviu falar do famoso, completo e detalhado **Guia do Mochileiro das Galáxias**.
Isso mesmo! Certifique-se da sua toalha pessoal, umas boas iscas para ratos e vamo nessa! :tumbsup:

## ii-Dinâmica
A ideia inicial era de se fazer um Diário conpartilhando nossas experiências que (achamos) que teríamos durante todo o processo
```markdown
  Dia #1
  Sem dúvidas, um dos dias mais loucos da minha vida! assim que chegamos lá, recebemos as instruções iniciais (o de sempre, poucas), e seguimos com a primeira lista Shell00 com dez exercícios com explicações básicas, mas nada como perguntar ao famoso pai Google, Youtube e StackOverflow.
  No início achamos que o limite de tempo de entrega das listas era de 24 horas, mas não amigos... O lema *DON'T PANIC!* não é mera coincidência. Pra entender do que eu tô falando, só mesmo **mergulhando na piscine**

  Dia #2
  Hoje o dia amanheceu chuvoso, mas bastante propício a um delicioso **mergulho**.
    Nada como um dia após o outro, e uma noite de sono no meio! Chegamos mais tranquilos ao cluster, e com isso, mais dispostos e propensos a trocas mais eficientes. É de se esperar que no primeiro dia as coisas não fluam lá tão bem, tem todo um background ne? nervosismo, ansiedade e afins. É *completamente* normal.
    Trocando em miúdos: pessolmente, praticamente tudo o que foi feito ontem, só foi fixado na mente (e no coraçãozinho) hoje. O que ontem parecia perdido, hoje fluiu desde o momento em que sentamos ao pc. O maior ensinamento de hoje foi, sem dúvidas, **a gente aprende enquanto ensina, e consegue ensinar enquanto está aprendendo**. Na dúvida, faz que nem a Dory e *continue a nadar, continue a nadar, nadar, para achar a solução, nadar!*
```
E foi isso, não tivemos cabeça pra continuar e já daí foi só ladeira a baixo. Mas a "dinâmica" da escola é baseada (até onde conseguimos entender, pode ser que estejamos completamente errados) basicamente na entrega de [Listas de Exercícios](#listas), realização de Avaliações, Exames Obrigatórios e Opicionais e a participação nos eventos.

### Mecanismos de Avaliação
A cada "projeto" ralizado que seja necessária a realiação de uma submição é realizada uma etapa de avalização dividida basicamente em dois elementos:

- Avalização dos seus colegars (peers), no mínimo dois para as listas e três para o BSQ. Para isso são gastos pontos de avaliação;
- Avaliação da **Moulinette** que testa automaticamente cada um dos exercícios enviados aplicando também a **Norminette**.

Quando um projeto é marcado como finalizado, é definida uma janela de tempo de 24h para a correção do trabalho, cada avaliação deve ser agendada (esteja sempre na escola durante avaliação), cada ponto gasto para agendamentos, pode ser ganho quando marcas disponibilidade e avalias projetos de outras pessoas. </br>
Ao final de duas avaliações (positivas ou não e, depois de dado o feedback à pessoa que avaliou) é realizada a da Moulinette, que é automática.

### Moulinette
Para tentar filtrar os resultados e testar as funções prototipadas nos exercícios segue logo abaixo a Fake, uma lista de funções `main()`, em cada pasta de exercício. </br>
Após a correção, é enviada para seu email o trace, do que foi encontrado como erro e o resultado (que também é apresentado no intra).

### Norminette
Basicamente uma avaliação da Norma, sua Lista pode estar entregando o resultado esperado, se não estiver de acordo com ela, a Moulinette vai identificar `Norme Error`, e seu trabalho irá pelo ralo.

Para chamar-la, basta abrir o terminal na pasta e digitar o código (com ou sem o nome do arquivo, opicional):
```bash
$ norminette [nome_do_arquivo]
```

É esperado que ela retorne o nome de cada arquivo com `OK!` ou a indicação da linha e coluna junto com a descrição da falha cometida.

**Critérios da Norminette**

- Identação e espaçamento do código </br>
esse é definitivamente o que mais se perde tempo no início. Na definição das funções e variáveis deve-se ter espaçamento de um tab, nos loops while deve-se ter um espaço depois da palavra especial, o valor do retorno deve sempre estar entre parênteses. No fim das contas você vai aprender pelo sofrimento.
```c
int/*tab*/function_name(/*if nothing*/void)
{/*in a new line*/
  int/*tab*/counter;
  /*enter*/
  counter = 0;
  while/*espace*/(condition)
  {/*in a new line*/
    //code in loop
    counter++;
  }/*in a new line*/
  return(counter);
}/*in a new line*/
```
- Passagem de no máx 4 parâmetros por função
```c
void  function_name(int arg1, int arg2, char arg3, char arg4)
{
  //code
}
```
- Definição de no máx 5 variáveis locais (ver [escopo de variáveis]()), em linhas separadas e sempre seguida de uma linha vazia.

*IMPORTANTE* Declarar variáveis globais não é permitido, pode-se contornar essa situação com o uso de [structs]().
```c
void  function_name(void)
{
  int   var1;
  int   var2;
  char  var3;
  char  var4;
  char  var5;

  //code...
}
```
- Limite máximo de 25 linhas de código dentro da função.
```c
void  function_name(void)
{
  //ln 1
  //...
  //ln 25
}
```

## iii-Listas
Cada lista é composta de uma série de exercícios que basicamente vão ser cobrados posteriormente, nas provas. O Shell tem como objetivo aprender os comandos básicos e necessários para lidar com a cópia (clone) de repositórios seus ou de pessoas que vão ser avaliadas por você e para o envio (submição) dos seus trabalhos. Em seguida vêm as listas em C, que basicamente são o tema da Piscine e das provas, ou seja, foque em C.

Algumas delas podem conter alguns erros que passaram despercebidos, ou seja, dê uma boa revisada antes de subemeter, é bom que tu aprende durante o processo (se ainda não tiver entendido, o que é comum).

Logo abaixo temos o README do repo de [eduardomosko](https://github.com/eduardomosko) que ajudou demais nos testes para as fuções que vamos criar no decorrer da piscine, dá uma moral lá, os cara são bons!

### [Fake Moulinnete](https://github.com/eduardomosko/fake-moulinnete)
  > by [eduardomosko](https://github.com/eduardomosko)

Testes que talvez funcionem corretamente para as listas da 42.

Neste arquivo criamos (emendes- & vgoncalv): testes que tentam checar as mesmas coisas que a Moulinette checa.

Atenção! Isto foi feito por outros campers e não é um programa oficial, é importante que você consiga entender o funcionamento de cada exercício e seja capaz de escrever seus próprios testes. Pense neste repositório como uma checagem extra antes de enviar seu projeto.

Existem 2 tipos de teste, um deles tem que ser compilado exercício por exercício e o outro testa a lista inteira de uma só vez (É necessário que todas as funções estejam definidas, mesmo que elas não façam nada).

Para executar os testes da lista inteira, compile da seguinte maneira:
(para rodar o `all.c` você precisa ter todas as funções da lista criadas)

```bash
$ cc -Wall -Wextra -Werror $(find -type f -name "*.c") all.c [flags adicionais]
```

Para testar um arquivo por vez, o comando é:

```bash
$ gcc -Wall -Wextra -Werror [seu arquivo] [ex**.c] [flags adicionais]
```

Avisos
---
- O C06 consiste de programas, então não fizemos testes para eles.
- Caso encontrem algum erro, favor nos comunicar no Discord (ão achei o link deles x.x ).

---

|__Listas__|__Percentual__|__X__|
|-|-|-|
|[Sh00](./Lists/sh00/)|-|-|
|[Sh01](./Lists/sh01/)|-|-|
||||
|[C00](./Lists/c00/)|-|-|
|[C01](./Lists/c01/)|-|-|
|[C02](./Lists/c02/)|-|-|
|[C03](./Lists/c03/)|-|-|
|[C04](./Lists/c04/)|-|-|
|[C05](./Lists/c05/)|-|-|
|[C06](./Lists/c06/)|-|-|
|[C07](./Lists/c07/)|-|-|
|[C08](./Lists/c08/)|Not Rated|:x:|
|[C09](./Lists/c09/)|Not Rated|:x:|
|[C10](./Lists/c10/)|Not Rated|:x:|
|[C11](./Lists/c11/)|Not Rated|:x:|
|[C12](./Lists/c12/)|Not Rated|:x:|
|[C13](./Lists/c13/)|Not Rated|:x:|

## iv-Exames
Lembre-se de se inscrever na lista de projetos e no evento da prova, se não, não será possível entrar na prova.

### Obrigatórios
Toda sexta-feira são realizados exames de longa duração, os primeiros de 4h cada e o último de 8h.

Os primeiros possuem 10 questões (ou níveis, do 0 ao 9), onde só se prode proceguir tendo acerdado a questão anterior. Cada uma vale 10 pontos e o mínimo é 25% da prova, ou seja, três questões.

O último é basicamente o acúmulo de todos os outros, com um nível de complexidade mais elevado (sim, esteja preparado). Cada questão vale 6 pontos, aumentando a quandidade de questões no total e para passar (5 quest).

|EXAME|FOCADO EM|
|-|-|
|Exam00|C00-C01|
|Exam01|C02-C03-C04-C06|
|Exam02|C05-C07-C08-C09|
|Exam03|TUDO ANTERIORMENTE|

Vale salientar que as primeiras questões são sempre mais tranquilas, em cada prova a progreção da dificuldade é mais rápida (e aleatória).

### Opcionais
São os Rushs e o BSQ. Se possível, faça o primeiro de preferência, os demais são perda de tempo, a menos que seu progresso seja excepcional ou você seja um superdotado ou já conheça C.

A inscrição (dos Rushs) é feita na sexta e o projeto so pode ser feito no fim de semana. Os grupos são definidos aleatoriamente. As defesas são realizadas nas Quartas-feiras ou nas Quintas.

Para o BSQ, os times são de duas pessoas e podem ser escolhidos pelos alunos, o prazo é na semana final e deve ser defendido da quarta (23:40) à quinta-feira.

|__Exames__|__Percentual__|__#__|
|-|-|-|
|[Exam00]()|-|-|
|[Exam01]()|-|-|
|[Exam02]()|-|-|
|[Exam03]()|-|-|
|[Rush00]()|-|-|
|[Rush01]()|-|-|
|[Rush02]()|-|-|
|[BSQ]()|Erro de Norma|:x:|


#### BONUS
Para você, que chegou até aqui tenho um presente: a realidade. </br>
Passamos recentemente por esse processo inteiro, nos dedicamos corpo e principalmente alma, vimos e tivemos muitas crises de ansiedade, sobrevivemos.
Nos dedicamos ao processo que ahcávamos "verdadeiro", de aprender, de ajudar.

Ficamos até altas horas da madrugada, alguns de nós tinha de trabalhar logo cedo no outro dia, ou trabalhava durante a noite e ia durante o dia.

*Não concordamos com o método aplicado nas avaliações, como que a realidade do programador é lembrar da cabeça todos os códigos e aplicar eles com única folha de papel e uma caneta?*

Vimos gente que copiava as listas e/ou simplesmente usava motores de AI para gerar o código e aprovar o máximo possível, para chegar na prova e simplesmente decorar as questões que poderiam ser cobradas e "se dar bem". Então meu amigo *copie o máximo que puder e estude depois*, deixe para submeter os arquivos durante a madrugada, onde pode-se controlar as avaliações e quem irá avaliar. </br>
Decore a prova e passe nelas, nem que seja com o valor mínimo. Ganhe tempo e vá estudando com calma.