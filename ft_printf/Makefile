# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: vvoronts <vvoronts@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2024/09/13 19:28:02 by vvoronts          #+#    #+#              #
#    Updated: 2024/09/29 11:38:54 by vvoronts         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libftprintf.a

SRCS := ft_printf.c ft_print_alfa.c ft_print_numeric.c main.c
OBJS := $(SRCS:.c=.o)
DEPS := ft_printf.h
LBFT := libft/libft.a
LOBJ := libft/*.o

CC := cc
RM := rm -f
AR := ar -rcs
# CFLAGS := -Wall -Wextra -Werror

$(NAME): $(LBFT) $(OBJS) 
	$(AR) $(NAME) $(OBJS) $(LOBJ)

$(OBJS): $(SRCS) $(DEPS)
	$(CC) -c $(SRCS)

$(LBFT):
	$(MAKE) -C ./libft

all: $(NAME)

clean:
	$(MAKE) clean -C ./libft
	$(RM) $(OBJS)

fclean: clean
	$(MAKE) fclean -C ./libft
	$(RM) $(NAME)

re: fclean all

.PHONY: all clean fclean re