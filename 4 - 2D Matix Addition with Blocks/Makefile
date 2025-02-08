NVCCFLAGS = -g -G

all: build

build: matrix_add.out vector_add.out vector_add_simple.out

matrix_add.out: matrix_add.cu
	nvcc $(NVCCFLAGS) -o matrix_add.out matrix_add.cu
	nvcc $(NVCCFLAGS) -o vector_add_simple.out vector_add_simple.cu

clean:
	rm -f matrix_add.out

run: build
	./matrix_add.out