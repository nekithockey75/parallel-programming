CC = gcc
CC_FLAGS = -g -fopenmp -O0 -std=c99

all: kmeans-serial kmeans-parallel

kmeans-serial: main.c cluster.c kmeans-clustering.c kmeans.h
	${CC} ${CC_FLAGS} main.c cluster.c kmeans-clustering.c -o kmeans-serial -lm

kmeans-parallel: main.c cluster.c kmeans-clustering.c kmeans.h
	${CC} ${CC_FLAGS} -DPARALLEL main.c cluster.c kmeans-clustering.c -o kmeans-parallel -lm

clean:
	rm -f *~ kmeans-serial kmeans-parallel
