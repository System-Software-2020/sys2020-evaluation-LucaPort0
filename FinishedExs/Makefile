all: ex1 installEx1 ex2 installEx2

run:
	./ex1

clean:
	rm -f libex2.so ex1

install: installEx1 installEx2

installEx1: 
	cp ex1 $(prefix)/usr/bin/

installEx2: 
	cp libex2.so $(prefix)/usr/lib/

uninstall:
	rm $(prefix)/usr/bin/ex1
	rm $(prefix)/usr/lib/libex2.so

ex1: 
	gcc -Wall -o ex1 ex1.c

ex2: 
	gcc -c -Wall ex2.c
	gcc -shared -o libex2.so ex2.o
