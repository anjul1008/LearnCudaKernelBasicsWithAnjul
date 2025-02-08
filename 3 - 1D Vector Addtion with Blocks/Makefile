NVCCFLAGS = -g -G

all: build

build: matrix_add.out vector_add.out vector_add_simple.out

vector_add.out: vector_add.cu
	nvcc $(NVCCFLAGS) -o vector_add.out vector_add.cu

clean:
	rm -f vector_add.out

run: build
	./vector_add.out