CUDIR = /usr/local/cuda-7.0
CULIB = ${CUDIR}/lib64 -lcudart
CUINC = ${CUDIR}/include
CUFLAG = -gencode arch=compute_35,code=sm_35 -Xptxas=-v -fmad=false -use_fast_math -maxrregcount=56  
CFLAG = -fopenmp -O3

CC = g++
CU = nvcc

all: a.out

a.out:	rtmlib-modC.o rtmlib-modC-gpu.o
	${CC} ${CFLAG} rtmlib-modC.o rtmlib-modC-gpu.o -L${CULIB} -o a.out  



rtmlib-modC.o:	rtmlib-modC.c
	${CC} -c ${CFLAG} rtmlib-modC.c



rtmlib-modC-gpu.o: rtmlib-modC-gpu.cu
	${CU} -c rtmlib-modC-gpu.o ${CUFLAG} rtmlib-modC-gpu.cu -I${CUINC}

run:	
	./a.out

clean:
	rm -f *.o
	rm *.out
