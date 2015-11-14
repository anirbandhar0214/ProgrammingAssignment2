# R Programming Assessment 2 - Sample Run
## Anirban Dhar

## Testing the code with a sample 2/2 matrix

```r
source ("cachematrix.R")
x = rbind(c(1, -1/2), c(-1/2, 1)) 
m = makeCacheMatrix(x) 
m$get() 
```

```
##      [,1] [,2]
## [1,]  1.0 -0.5
## [2,] -0.5  1.0
```
## First run with no caching

```r
cacheSolve(m)
```

```
##           [,1]      [,2]
## [1,] 1.3333333 0.6666667
## [2,] 0.6666667 1.3333333
```

```r
proc.time() 
```

```
##      user    system   elapsed 
##     89.59     32.33 139523.33
```

## 2nd Run uses caching

```r
cacheSolve(m) 
```

```
## getting cached data.
```

```
##           [,1]      [,2]
## [1,] 1.3333333 0.6666667
## [2,] 0.6666667 1.3333333
```

```r
proc.time()
```

```
##      user    system   elapsed 
##     89.62     32.33 139523.36
```
