# Shell01 Lista
## ex00
1.	logar na intranet no pc do avaliado ou no seu proprio
2.	clicar em iniciar avaliacao
3.	$ git clone git@vogsphere… shell_00
4.	verificar todos os arquivos com $ ls */                                                              ** ou $ norminette
5.	se algum arquivo estiver faltando > marcar “empty work”
6.	o avaliado deve explicar como chegou no resultado de cada avaliacao, pode-se chegar numa solucao, caso seja encontrado algum erro, caso de forma alguma consiga explicar como chegou naquela resposta… marcar “cheat”
7.	lembrar de marcar os Ratings
8.	e concluir com comentarios

o avaliado deve mandar sempre o feedback do avaliador!

## ex01
c1r10s4% cat > testShell00
zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz
c1r10s4% ls -l
total 4
-rw-r--r-- 1 gabrodri 2023_porto 42 Mar  6 18:29 testShell00
c1r10s4% nano testShell00
c1r10s4% ls -l      	 
total 4
-rw-r--r-- 1 gabrodri 2023_porto 40 Mar  6 18:30 testShell00
c1r10s4% touch -t 06012342
touch: missing file operand
Try 'touch --help' for more information.
c1r10s4% touch -t 06012342 testShell00
c1r10s4% ls -l
total 4
-rw-r--r-- 1 gabrodri 2023_porto 40 Jun  1  2023 testShell00
c1r10s4% chmod 455 testShell00
c1r10s4% ls -l
total 4
-r--r-xr-x 1 gabrodri 2023_porto 40 Jun  1  2023 testShell00
c1r10s4% tar -cf testShell00.tar testShell00
c1r10s4% ls -l
total 16
-r--r-xr-x 1 gabrodri 2023_porto	40 Jun  1  2023 testShell00
-rw-r--r-- 1 gabrodri 2023_porto 10240 Mar  6 18:36 testShell00.tar
c1r10s4% ls
testShell00.tar
c1r10s4%

## ex02
c1r10s4% pwd
/nfs/homes/gabrodri/Documents/shell00/ex02
c1r10s4% mkdir test0 test 2
c1r10s4% touch test1 test3 test4
c1r10s4% ln test3 test5
c1r10s4% ln -s test0 test6
c1r10s4% ls -l
total 12
drwxr-xr-x 2 gabrodri 2023_porto 4096 Mar  6 18:56 2
drwxr-xr-x 2 gabrodri 2023_porto 4096 Mar  6 18:56 test
drwxr-xr-x 2 gabrodri 2023_porto 4096 Mar  6 18:56 test0
-rw-r--r-- 1 gabrodri 2023_porto	0 Mar  6 18:57 test1
-rw-r--r-- 2 gabrodri 2023_porto	0 Mar  6 18:57 test3
-rw-r--r-- 1 gabrodri 2023_porto	0 Mar  6 18:57 test4
-rw-r--r-- 2 gabrodri 2023_porto	0 Mar  6 18:57 test5
lrwxrwxrwx 1 gabrodri 2023_porto	5 Mar  6 18:57 test6 -> test0
c1r10s4% ls -l
total 8
drwxr-xr-x 2 gabrodri 2023_porto 4096 Mar  6 18:56 test0
-rw-r--r-- 1 gabrodri 2023_porto	0 Mar  6 18:57 test1
drwxr-xr-x 2 gabrodri 2023_porto 4096 Mar  6 18:56 test2
-rw-r--r-- 2 gabrodri 2023_porto	0 Mar  6 18:57 test3
-rw-r--r-- 1 gabrodri 2023_porto	0 Mar  6 18:57 test4
-rw-r--r-- 2 gabrodri 2023_porto	0 Mar  6 18:57 test5
lrwxrwxrwx 1 gabrodri 2023_porto	5 Mar  6 18:57 test6 -> test0
c1r10s4% truncate -s 4 test1
c1r10s4% truncate -s 1 test3
c1r10s4% truncate -s 2 test4
c1r10s4% truncate -s 1 test5
c1r10s4% ls -l
total 8
drwxr-xr-x 2 gabrodri 2023_porto 4096 Mar  6 18:56 test0
-rw-r--r-- 1 gabrodri 2023_porto	4 Mar  6 18:59 test1
drwxr-xr-x 2 gabrodri 2023_porto 4096 Mar  6 18:56 test2
-rw-r--r-- 2 gabrodri 2023_porto	1 Mar  6 18:59 test3
-rw-r--r-- 1 gabrodri 2023_porto	2 Mar  6 18:59 test4
-rw-r--r-- 2 gabrodri 2023_porto	1 Mar  6 18:59 test5
lrwxrwxrwx 1 gabrodri 2023_porto	5 Mar  6 18:57 test6 -> test0
c1r10s4% touch -t 06012047 test0
c1r10s4% touch -t 06012146 test1
c1r10s4% touch -t 06012245 test2
c1r10s4% touch -t 06012344 test3
c1r10s4% touch -t 06012343 test4
c1r10s4% touch -t 06012344 test5
c1r10s4% touch -ht 06012220 test6
c1r10s4% ls -l
total 8
drwxr-xr-x 2 gabrodri 2023_porto 4096 Jun  1  2023 test0
-rw-r--r-- 1 gabrodri 2023_porto	4 Jun  1  2023 test1
drwxr-xr-x 2 gabrodri 2023_porto 4096 Jun  1  2023 test2
-rw-r--r-- 2 gabrodri 2023_porto	1 Jun  1  2023 test3
-rw-r--r-- 1 gabrodri 2023_porto	2 Jun  1  2023 test4
-rw-r--r-- 2 gabrodri 2023_porto	1 Jun  1  2023 test5
lrwxrwxrwx 1 gabrodri 2023_porto	5 Jun  1  2023 test6 -> test0
c1r10s4% chmod 715 test0
c1r10s4% chmod 714 test1
c1r10s4% chmod 504 test2
c1r10s4% chmod 404 test3
c1r10s4% chmod 641 test4
c1r10s4% chmod 404 test5
c1r10s4% ls -l
total 8
drwx--xr-x 2 gabrodri 2023_porto 4096 Jun  1  2023 test0
-rwx--xr-- 1 gabrodri 2023_porto	4 Jun  1  2023 test1
dr-x---r-- 2 gabrodri 2023_porto 4096 Jun  1  2023 test2
-r-----r-- 2 gabrodri 2023_porto	1 Jun  1  2023 test3
-rw-r----x 1 gabrodri 2023_porto	2 Jun  1  2023 test4
-r-----r-- 2 gabrodri 2023_porto	1 Jun  1  2023 test5
lrwxrwxrwx 1 gabrodri 2023_porto	5 Jun  1  2023 test6 -> test0
c1r10s4% tar -cf exo2.tar *
c1r10s4% ls
exo2.tar  test0  test1    test2  test3  test4  test5  test6
c1r10s4% ls
exo2.tar
c1r10s4%

## ex03
c1r10s4% pwd
/nfs/homes/gabrodri/Documents/shell00
c1r10s4% mkdir ex03
c1r10s4% cd ex03
c1r10s4% pwd
/nfs/homes/gabrodri/Documents/shell00/ex03
c1r10s4% cd
c1r10s4% pwd
/nfs/homes/gabrodri
c1r10s4% cd ~/.ssh
c1r10s4% pwd
/nfs/homes/gabrodri/.ssh
c1r10s4% ls
id_rsa    id_rsa.pub  known_hosts
c1r10s4% cp id_rsa.pub /nfs/homes/gabrodri/Documents/shell00/ex03
c1r10s4%

===

c1r10s4% wpd
zsh: command not found: wpd
c1r10s4% pwd
/nfs/homes/gabrodri/Documents/shell00/ex03
c1r10s4% ls
id_rsa_pub

## ex04
https://man7.org/linux/man-pages/man1/ls.1.html

c1r10s14% pwd
/nfs/homes/gabrodri/Documents/shell00/ex04
c1r10s14% echo "ls -npt" > midLS
c1r10s14% ls
midLS
c1r10s14%
c1r10s14%

## ex05
git status
git add <file>
git commit -m”mesage”
git log
git log --format='%H' -n5

## ex06
## ex07
c1r11s4% pwd
/nfs/homes/gabrodri/Documents/shell00/ex07
c1r11s4% ls
a  sw.diff
c1r11s4% cp a b
c1r11s4% patch b < sw.diff
patching file b
c1r11s4% cat -e a
STARWARS$
Episode IV, A NEW HOPE It is a period of civil war.$
$
Rebel spaceships, striking from a hidden base, have won their first victory against the evil Galactic Empire.$
During the battle, Rebel spies managed to steal secret plans to the Empire's ultimate weapon, the DEATH STAR,$
an armored space station with enough power to destroy an entire planet.$
$
Pursued by the Empire's sinister agents, Princess Leia races home aboard her starship, custodian of the stolen plans that can save her people and restore freedom to the galaxy...$
$
c1r11s4% diff a b > sw.diff
c1r11s4% ls  
a  b  sw.diff
c1r11s4% cat -e b
Episode V, A NEW H0PE It is a period of civil war$
Rebel spaceships, striking from a hidden base, have won their first victory against the evil Galactic Empire. $
During the battle, Rebel spies managed to steal secret plans to the Empire's ultimate weapon, the STAR DEATH, an armored space station with enough power to destroy an entire planet.$
$
$
Pursued by the Empire's sinister agents,$
Princess Mehdi races home aboard her starship, custodian of the stolen plans that can save her people and restore the dictatorship to the galaxie..$
$
$
$
$
c1r11s4%

## ex08

c1r11s4% pwd
/nfs/homes/gabrodri/Documents/shell00/ex08
c1r11s4% ls
c1r11s4% cat > clean
find . -type f \( -name "#*#" -o -name "*~" \) -print -delete

c1r11s4% cat -e clean
find . -type f \( -name "#*#" -o -name "*~" \) -print -delete$

c1r11s4% touch test~ #test#
c1r11s4% ls -a
 .   ..   clean  '#test#'   test~
c1r11s4% bash clean
./test~
./#test#
c1r11s4% ls -a
.  ..  clean
c1r11s4%

## ex09
c1r11s4% 

41 string 42 42 file

—
 
pra testar arquivo
cat > teste
0000000000000000000000000000000000000000042
c1r14s2% vim ft_magic
c1r14s2% ls
teste
c1r14s2% ls -;
ls: cannot access '-': No such file or directory
c1r14s2% ls -l
total 4
-rw-r--r-- 1 amgoncal 2023_porto 44 Mar  8 15:07 teste
c1r14s2% ls -a
.  ..  .ft_magic.swp  teste
c1r14s2% vim ft_magic
c1r14s2% vim ft_magic
c1r14s2% vim ft_magic
c1r14s2% file -C -m ft_magic > ft_magic.mgc
c1r14s2% file -m ft_magic teste
teste: 42 file
c1r14s2%

