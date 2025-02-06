NVCCFLAGS = -g -G

all: build

build: matrix_add.out vector_add.out vector_add_simple.out

vector_add_simple.out: vector_add_simple.cu
	nvcc $(NVCCFLAGS) -o vector_add_simple.out vector_add_simple.cu

clean:
	rm -f vector_add_simple.out

run: build
	./vector_add_simple.out