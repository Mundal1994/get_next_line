NAME = t1.out
NAME += t2.out
NAME += t3.out
NAME += t4.out
NAME += t5.out
NAME += t6.out
NAME += b.out

DEL = *.o
DEL += ./*.o
DEL += $(SL)*.o

SL = ../
CL = clang
CC = -g -Wall -Wextra -Werror
LIB = -I $(SL)libft/includes
LIBFT = -I $(SL)libft/includes -L $(SL)libft/ -lft
MAKELIB = make -C $(SL)libft/ fclean && make -C $(SL)libft/

COMP = $(CL) $(CC) $(LIB) -o $(SL)get_next_line.o -c $(SL)get_next_line.c

lib:
	$(MAKELIB)

t1:
	$(COMP)
	$(CL) $(CC) $(LIB) -o test1.o -c -x c test1.test
	$(CL) -o t1.out test1.o $(SL)get_next_line.o $(LIBFT)

t2:
	$(COMP)
	$(CL) $(CC) $(LIB) -o test2.o -c -x c test2.test
	$(CL) -o t2.out test2.o $(SL)get_next_line.o $(LIBFT)

t3:
	$(COMP)
	$(CL) $(CC) $(LIB) -o test3.o -c -x c test3.test
	$(CL) -o t3.out test3.o $(SL)get_next_line.o $(LIBFT)

t4:
	$(COMP)
	$(CL) $(CC) $(LIB) -o test4.o -c -x c test4.test
	$(CL) -o t4.out test4.o $(SL)get_next_line.o $(LIBFT)

t5:
	$(COMP)
	$(CL) $(CC) $(LIB) -o test5.o -c -x c test5.test
	$(CL) -o t5.out test5.o $(SL)get_next_line.o $(LIBFT)

t6:
	$(COMP)
	$(CL) $(CC) $(LIB) -o test6.o -c -x c test6.test
	$(CL) -o t6.out test6.o $(SL)get_next_line.o $(LIBFT)

b:
	$(COMP)
	$(CL) $(CC) $(LIB) -o bonus.o -c -x c bonus.test
	$(CL) -o b.out bonus.o $(SL)get_next_line.o $(LIBFT)

clean:
	/bin/rm -f $(DEL)

fclean: clean
	/bin/rm -f $(NAME)

al: t1 t2 t3 t4 t5 t6 b clean

all: lib t1 t2 t3 t4 t5 t6 b clean

run3:
	./t3.out txt/txt1.txt
	./t3.out txt/txt2.txt
	./t3.out txt/txt3.txt
	./t3.out txt/txt4.txt
	./t3.out txt/txt5.txt
	./t3.out txt/txt6.txt
	./t3.out txt/txt7.txt
	./t3.out txt/txt8.txt
	./t3.out txt/txt9.txt
	./t3.out txt/txt10.txt
	./t3.out txt/txt11.txt
	./t3.out txt/txt12.txt
	./t3.out txt/txt13.txt
	./t3.out txt/txt14.txt

runall:
	./t1.out
	./t2.out
	make run3
	./t5.out
	./t6.out

re: fclean all
