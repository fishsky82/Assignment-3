# Assignment-3
makeCatcheMatrix=function(x=matrix()){
    inv=NULL
    set=function(y){
        x<=y
        inv<=NULL
    }
    get=function()x
    setinverse=function(inverse) inv=inverse
    getinverse=function() inv
    list=(set=set,get=get,inverse=setinverse,getinverse=getinverse)
}

cacheSolve=function(x,...){
    inv=x$getinverse()
    if(!is.null(inv)){
        message("gettng cached data.")
        return(inv)
        }
    data=x$get()
    inv=solve(data)
    x$setinverse(inv)
    inv
    }
