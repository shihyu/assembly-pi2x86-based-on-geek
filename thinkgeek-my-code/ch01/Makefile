# Makefile

all: first
 
first: first.o
	gcc -o $@ $+
 
first.o : first.s
	as -o $@ $<
	
run: first
	./first; echo $$? # not sure why 132 i.e CR 2 not just 2 

objdump: first.o
	objdump -d first.o

gdb: first
	# http://web.cecs.pdx.edu/~jrb/cs201/lectures/handouts/gdbcomm.txt
	# start
	# disas
	# info registers r0 r1 r2 r3
	# info all-registers
	# p $ro = 2
	# stepi / si
	# nexti / ni
	# p &myvar1
	# p myvar1
	# break function/line-no/file:line-no
	# watch expression
	# info breakpoint
	# bt
	# frame
	# info local
	# show commands
	# define caommand ... end
	# help running/run/info/info line/show/show coammnds
	gdb --args ./first

clean:
	rm -vf first *.o