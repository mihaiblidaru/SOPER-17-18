# Práctica 2
# Sistemas Operativos - 2262
# 
# Pareja 9:
#        Lucia Fuentes
#        Mihai Blidaru
# 

CC = gcc
EXE = ejercicio2 ejercicio4 ejercicio6a ejercicio6b ejercicio9
FLAGS = -Wall -g

$(mkdir doc)

all: $(EXE)

ejercicio2: ejercicio2.c
	$(CC) $(FLAGS) $< -o $@

ejercicio4: ejercicio4.c
	$(CC) $(FLAGS) $< -o $@

ejercicio6a: ejercicio6a.c
	$(CC) $(FLAGS) $< -o $@

ejercicio6b: ejercicio6b.c
	$(CC) $(FLAGS) $< -o $@
	
ejercicio9: ejercicio9.o semaforos.o
	$(CC) $(FLAGS) $^ -o $@

semaforos.o: semaforos.c semaforos.h
	$(CC) -c $(FLAGS) $< -o $@

ejercicio9.o: ejercicio9.c
	$(CC) -c $(FLAGS) $< -o $@
	
PHONY: clean

clean:
	rm -f $(EXE) *.o
	rm -r -f doc/
	rm -f *.txt
	
doxygen:
	rm -f -r doc/
	mkdir doc
	doxygen Doxyfile
