output: main.o function.o
	gcc main.o function.o -o output

main.o: main.c
	gcc -c main.c

function.o: function.c function.h
	gcc -c function.c

clean:
	del *.o output
