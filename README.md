# PA2
R programming assignment 2
Matrix inversion is usually a costly computation and there may be some benefit to caching the inverse of a matrix rather than compute it repeatedly.
makeCacheMatrix: This function creates a special "matrix" object that can cache its inverse.
cacheSolve: This function computes the inverse of the special "matrix" returned by makeCacheMatrix above. If the inverse has already been calculated (and the matrix has not changed), then the cachesolve retrieves the inverse from the cache.
> source("Caching_the_Inverse_of_a_Matrix.R")
> test2 <- makeCacheMatrix(matrix(1:4, 2, 2))
> test2$get()
     [,1] [,2]
[1,]    1    3
[2,]    2    4
> test2$getinverse()
NULL
> cacheSolve(test2)
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5
> cacheSolve(test2)
getting cached data
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5
> test2$getinverse()
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5
