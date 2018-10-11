#Makefile for CS3560 Make quiz
#Alexis Lanier

all: build doczip

build: college.o collegemain.o course.o
	g++ -o build college.cc collegemain.cc course.cc

college.o: college.cc college.h
	g++ -c college.cc college.h

collegemain.o: collegemain.cc course.h node.h college.h
	g++ -c collegemain.cc

course.o: course.cc course.h
	g++ -c course.cc course.h

doc:
	doxygen -g index.html
	doxygen index.html

doczip: college.cc collegemain.cc course.cc course.h node.h tarray.h makefile
	tar cvzf college_project.tar.gz college.cc college.h collegemain.cc course.cc course.h node.h tarray.h makefile

myexe:
	./a.out

clean:
	rm -rf *.o a.out html latex college_project.tar.gz build course.h.gch college.h.gch index.html index.html.bak


