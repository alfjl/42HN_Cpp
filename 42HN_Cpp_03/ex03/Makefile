NAME = a.out
CC = c++
CFLAGS = -Wall -Wextra -Werror
#CFLAGS = -Wall -Wextra -Werror -Wshadow -Wno-shadow
SRC = main.cpp \
	  ClapTrap.cpp \
	  ScavTrap.cpp \
	  FragTrap.cpp \
	  DiamondTrap.cpp
OBJ = $(patsubst %.cpp,%.o,$(SRC))

.PHONY: all debug clean fclean re

all: $(NAME)

%.o: %.cpp
	$(CC) $(CFLAGS) -c $< -o $@

$(NAME): $(OBJ)
	$(CC) $(CFLAGS) $^ -o $@

debug: $(OBJ)
	$(CC) $(CFLAGS) -std=c++98 $^ -o $@

clean:
	rm -f *.o *~
	rm -f *.out

fclean: clean
	rm -f $(NAME)
	rm -f debug

re: fclean all
