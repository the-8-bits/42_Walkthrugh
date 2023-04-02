# Shell01 Lista
## ex00
## ex01
#!/bin/bash
id -Gn $FT_USER | tr ' ' ','| tr -d '\n'

https://linuxcommand.org/lc3_man_pages/id1.html

https://superuser.com/questions/1294703/displays-the-list-of-groups-for-a-login-using-command-line-in-imac

https://www.geeksforgeeks.org/tr-command-in-unix-linux-with-examples/

## ex02
#!/bin/bash
find . -type f -name '*.sh' -printf "%f\n" | sed 's/\.sh$//'

o `-name` busca o formato do nome
o `-printf` define o que ele vai listar de acordo com a avaliacao booleana
o `sed` NÃO FAÇO PUTA IDEIA

c1r11s3% mkdir ex02
c1r11s3% cd ex02
c1r11s3% pwd
/nfs/homes/gabrodri/Documents/shell01/ex02
c1r11s3% cat > find_sh.sh
#!/bin/bash
find . type f -name "*sh" -print"%f\n" | sed "s/\.sh$//"
c1r11s3% ls
find_sh.sh

## ex03
https://stackoverflow.com/questions/9157138/recursively-counting-files-in-a-linux-directory


find . | wc -l

wc -l  → conta as pastas e arquivos, incluindo a atual

## ex04
ifconfig | grep ether | awk '{print $2}'

grep ether → Filtra a informacao contida no ether (ip)
awk '{print $2}' → mostra na tela apenas a segunda coluna, ontem tem a informacao do ip

sem a informacao do awk o resultado sai assim:
ether 00:be:43:89:f6:c5  txqueuelen 1000  (Ethernet)
ether 52:54:00:24:34:40  txqueuelen 1000  (Ethernet)

## ex05
cat > \"\\\?\$\*\'MaRViN\'\*\$\?\\\" 42   	


basicamente é só usar os escapes para transformar o carácter especial em str

## ex06
#!/bin/bash
ls -l | awk "NR % 2 == 1"

mostra todas as linhas impares

## ex07
cat /etc/passwd | grep -v '\#' | sed '1!n;d' | cut -d':' -f1 | rev | sort -r | awk 'NR>= ENVIRON["FT_LINE1"] && NR<= ENVIRON["FT_LINE2"]' | paste -s -d"," - | sed 's/,/, /g' | sed 's/$/./' | tr -d '\n'


cat /etc/passwd | grep -v '\#' | sed '1!n;d' | cut -d':' -f1 | rev | sort -r | awk 'NR>= ENVIRON["FT_LINE1"] && NR<= ENVIRON["FT_LINE2"]' | paste -s -d"," - | sed 's/,/, /g' | sed 's/$/./' | tr -d '\n'

resposta correta
#!/bin/bash
cat /etc/passwd | grep -v "#" | sed -n 'n;p' | cut -f 1 -d : | rev | sort -r | sed -n "$FT_LINE1,$FT_LINE2 p" | tr '\n' ',' | sed 's:,:, :g' | sed 's:, $:.:' | tr -d '\n' 
(ERRO: sed: -e expression #1, char 1: unknown command: `,')

cat /etc/passwd |  cat
grep -v "#" |  retira os comentarios
sed -n 'n;p' |  exclui a primeira linha
cut -f 1 -d : |  retira ultima coluna
rev |  inverte
sort -r | ordena
sed -n "$FT_LINE1,$FT_LINE2 p" | 
tr '\n' ',' |  translate, substitui quebra de linha por virgula
sed 's:,:, :g' | 
sed 's:, $:.:' | 
tr -d '\n'

## ex08
cat > add_chelou.sh
echo $FT_NBR1 + $FT_NBR2 | sed 's/\\/1/g' | sed 's/?/3/g' | sed 's/!/4/g' | sed "s/\'/0/g" | sed "s/\"/2/g" | tr "mrdoc" "01234" | xargs echo "ibase=5; obase=23;" | bc | tr "0123456789ABC" "gtaio luSnemf"