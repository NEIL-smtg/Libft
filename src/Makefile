# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: suchua <suchua@student.42kl.edu.my>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/10/05 12:01:03 by suchua            #+#    #+#              #
#    Updated: 2022/10/12 18:03:41 by suchua           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

SRCS    	=    ft_memset.c \
	ft_bzero.c \
	ft_memcpy.c \
	ft_memmove.c \
	ft_memchr.c \
	ft_memcmp.c \
	ft_strlen.c \
	ft_isalpha.c \
	ft_isdigit.c \
	ft_isalnum.c \
	ft_isascii.c \
	ft_isprint.c \
	ft_toupper.c \
	ft_tolower.c \
	ft_strchr.c \
	ft_strrchr.c \
	ft_strncmp.c \
	ft_strlcpy.c \
	ft_strlcat.c \
	ft_strnstr.c \
	ft_atoi.c \
	ft_calloc.c \
	ft_strdup.c \
	ft_substr.c \
	ft_strjoin.c \
	ft_strtrim.c \
	ft_split.c \
	ft_itoa.c \
	ft_strmapi.c \
	ft_putchar_fd.c \
	ft_putstr_fd.c \
	ft_putendl_fd.c \
	ft_putnbr_fd.c \
	ft_striteri.c \

BONUS		= ft_lstnew.c \
	ft_lstadd_front.c \
	ft_lstsize.c \
	ft_lstlast.c \
	ft_lstadd_back.c \
	ft_lstdelone.c \
	ft_lstclear.c \
	ft_lstiter.c \
	ft_lstmap.c

BONUS_OBJS	= 	 $(BONUS:.c=.o);
OBJS    	=    $(SRCS:.c=.o)
HEADER		= 	 libft.h
LIBFT    	=    libft.a
MAN			=	 man.a
B			=	 bonus.a
ARCR    	=    ar -crs
RMRF    	=    rm -rf
CFLAGS  	=    -Wall -Wextra -Werror
GCC     	=    gcc
BLUE		=	 \033[1;34m
NC			=    \033[0m

all: $(LIBFT)

$(LIBFT): m b

m: $(MAN)

$(MAN): $(OBJS)
	$(ARCR)	$(MAN) $(OBJS)
	cp $(MAN) $(LIBFT)

b: $(B)

$(B): $(BONUS_OBJS)
	$(ARCR) $(B) $(BONUS_OBJS)
	cp $(B) $(LIBFT)

clean:
	$(RMRF) $(OBJS) $(BONUS_OBJS)
	clear
	@echo "${BLUE}deleted .o files$(NC)"

fclean:    clean
	$(RMRF) $(LIBFT) $(B) $(MAN)
	clear
	@echo "${BLUE}deleted .o .a files$(NC)"

re:    fclean all
