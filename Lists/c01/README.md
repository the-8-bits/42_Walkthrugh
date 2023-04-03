# C01
## ex00
Este código em C é um exemplo de como utilizar [ponteiros](../../Docs/Pointers.md) e uma função para modificar o valor de uma variável.

A função `ft_ft` recebe um ponteiro para um inteiro como argumento e atribui o valor `42` ao inteiro apontado por este ponteiro. Isso é feito na linha 3, onde o conteúdo do endereço de memória apontado por nbr é modificado para o valor `42`.

Na função `main` (implementação da Fake Moilinette), são declaradas duas variáveis: `n`, que é um inteiro, e `nbr`, que é um ponteiro para um inteiro.

![c01_ex00_1](https://drive.google.com/uc?export=view&id=1_mPWMVFpLBLVcbl5YfMcvShxjZLU_H0b)

Na linha 11, o ponteiro `nbr` é inicializado com o endereço de memória da variável `n`. Isso é feito utilizando o operador `&`, que retorna o endereço de memória de uma variável.

![c01_ex00_2](https://drive.google.com/uc?export=view&id=12rzkuTErauXMZ2tprLXBv9CmFr2plKOw)

Na linha 12, a função `ft_ft` é chamada passando o ponteiro `nbr` como argumento. Isso faz com que o valor da variável n seja modificado para `42`.

![c01_ex00_3](https://drive.google.com/uc?export=view&id=1AyMTXkDt4jzvZ8KOGRcjZiC6y9eZfSVH)

Finalmente, na linha 13, a função printf é utilizada para imprimir o valor das variáveis n e `*nbr`, bem como o endereço de memória de n. O valor de n e `*nbr` será `42`, já que ambos estão apontando para o mesmo endereço de memória e foram modificados pela função `ft_ft`.

![c01_ex00_4](https://drive.google.com/uc?export=view&id=1xLw--rcbfpLejImmxT6uz5aVfx5_d79D)

Portanto, o resultado final da execução deste programa será a impressão da seguinte linha: n: `42, *nbr: 42, n_address: <endereço de memória>` (sendo `<endereço de memória>` o endereço de memória da variável `n`).

## ex01
## ex02
## ex03
## ex04
## ex05
## ex06
## ex07
## ex08

```c
```