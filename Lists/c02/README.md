# C02
## ex00
## ex01
## ex02
Aqui está uma possível implementação em C da função ft_str_is_alpha que verifica se uma string contém apenas caracteres alfabéticos usando somente a biblioteca <unistd.h>:

```c
#include <unistd.h>
int ft_str_is_alpha(char *str)
{ // Itera pelos caracteres da string
	while (*str != '\0')
	{ // Verifica se o caractere atual não é uma letra do alfabeto
		if (!((*str >= 'a' && *str <= 'z') || (*str >= 'A' && *str <= 'Z')))
		{
			return (0); // Se não for, retorna 0
		}
		str++; // Move para o próximo caractere
	}
	return (1); // Se todos os caracteres forem letras do alfabeto, retorna 1
}
```

Nessa implementação, em vez de usar a função isalpha da biblioteca ctype.h, a função verifica se um caractere é uma letra do alfabeto usando comparações diretas com os valores ASCII correspondentes. O intervalo de valores ASCII para as letras maiúsculas e minúsculas é de 65 a 90 e de 97 a 122, respectivamente. A função itera pelos caracteres da string, verificando se cada um deles é uma letra do alfabeto. Se encontrar um caractere que não seja uma letra, ela retorna 0 imediatamente, indicando que a string não contém apenas caracteres alfabéticos. Se a função chegar ao final da string sem encontrar nenhum caractere que não seja uma letra, ela retorna 1, indicando que a string contém apenas caracteres alfabéticos. A função utiliza apenas a biblioteca <unistd.h>, que é uma biblioteca padrão em sistemas Unix-like e fornece funções de entrada/saída de baixo nível, como write.

**por que o uso de "!" junto ao if?**

O operador "!" (negação lógica) usado junto ao if inverte a condição do teste. Em outras palavras, se a condição dentro do if for verdadeira, o ! a torna falsa e o bloco dentro do if não é executado. Por outro lado, se a condição dentro do if for falsa, o ! a torna verdadeira e o bloco dentro do if é executado.
No caso da função ft_str_is_alpha, a condição dentro do if é !isalpha(*str), que significa "se o caractere atual não é uma letra do alfabeto". O operador ! inverte essa condição para "se o caractere atual não é uma letra do alfabeto, retorne 0". Isso significa que, se o caractere atual não for uma letra do alfabeto, a função retorna imediatamente 0, indicando que a string não contém apenas caracteres alfabéticos. Se o caractere atual for uma letra do alfabeto, a função continua verificando os próximos caracteres até que chegue ao final da string. Se não encontrar nenhum caractere que não seja uma letra, a função retorna 1, indicando que a string contém apenas caracteres alfabéticos.

## ex03
## ex04
## ex05
## ex06
## ex07
## ex08
## ex09
## ex10
## ex11
## ex12
## ex13