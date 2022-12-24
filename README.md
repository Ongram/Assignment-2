# Assignment-2
Programming Assignment week 4 


makeVector <- function(x = numeric()) {
        inver <- NULL
        set <- function(y) {
                x <<- y
                m <<- NULL
        }
        
        get <- function() x
        setInverse <- function(mean) inver <<- inverse
        getInverse <- function() inver
        list(set = set, get = get,
             setInverse = setInverse,
             getInverse = getInverse)
}


cacheInverse <- function(x, ...) {
        inver <- x$getInverse()
        if(!is.null(inver)) {
                message("getting cached data")
                return(inver)
        }
        data <- x$get()
        inver <- solve(data, ...)
        x$setInverse(inver)
        inver
}


# Run exemple:

my_matrix <-matrix(1:4, nrow=2, ncol=2)
my_matrix
