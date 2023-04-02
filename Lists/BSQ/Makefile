NAME = bsq

CC = gcc

CFLAGS = -Wall -Wextra -Werror

SRC = main.c solution.c verification.c read_map1.c read_map2.c lib1.c lib2.c

all: $(NAME)

$(NAME):
	$(CC) $(CFLAGS) -o $(NAME) $(SRC)
clean:
	/bin/rm -f *.o

fclean: clean
	/bin/rm -f $(NAME)

re: fclean all
