all: program

bill.o: bill.c 
	gcc -c bill.c -o bill.o

fred.o: fred.c
	gcc -c fred.c -o fred.o

program.o: program.c 
	gcc -c program.c -o program.o

program: program.o lib.h 2ndLib.a
	gcc -o program program.o 2ndLib.a

2ndLib.a: fred.o bill.o
	ar cr 2ndLib.a fred.o bill.o
	ranlib 2ndLib.a

clean:
	rm -f *.o
	rm -f *.a

run:
	./program
