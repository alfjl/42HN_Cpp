NAME = a.out
CC = c++
CFLAGS = -Wall -Wextra -Werror
SRC = main.cpp \
	  Animal.cpp \
	  Dog.cpp \
	  Cat.cpp \
	  WrongAnimal.cpp \
	  WrongCat.cpp
OBJ = $(patsubst %.cpp,%.o,$(SRC))

.PHONY: all debug clean fclean re

all: $(NAME)

%.o: %.cpp
	$(CC) $(CFLAGS) -c $< -o $@

$(NAME): $(OBJ)
	$(CC) $(CFLAGS) $^ -o $@

debug: $(OBJ)
	$(CC) $(CFLAGS) -std=c++98 -pedantic $^ -o $@

clean:
	rm -f *.o *~

fclean: clean
	rm -f $(NAME)
	rm -f debug

re: fclean all
