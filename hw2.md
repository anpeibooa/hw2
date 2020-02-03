---
title: "Homework 2"
author: '[Group name and member names]'
date: ""
output: 
  html_document:
    keep_md: yes
---



## Task 3


```r
myclass <- function(x){
  stopifnot(length(x) == 4)
  structure(x, class = "myarray")
}
```


```r
mycheck <- function(x){
  #stopifnot(is.integer(x)==TRUE)
  #stopifnot(sum(x)>0)
  if(is.integer(x)==TRUE & sum(x) >0){
    return ("all good")
  }
  else{
    return ("not good")
  }
 
}
```


```r
myhelper <- function(x){
  if(length(x)==4 & mycheck(x) == "all good"){
    myclass(x)
  }
  else{
    newx <- abs(round(x[1:4], 0))
    myclass(newx)
  
  }
}
```


```r
myclass(1:4)
```

```
[1] 1 2 3 4
attr(,"class")
[1] "myarray"
```

```r
mycheck(c(1.1,1.2,1.3,2))
```

```
[1] "not good"
```

```r
myhelper(c(1.1,1.2,1.3,2))
```

```
[1] 1 1 1 2
attr(,"class")
[1] "myarray"
```

```r
myhelper(c(1.1,1.2,1.3,2,2.1,2.2))
```

```
[1] 1 1 1 2
attr(,"class")
[1] "myarray"
```

```r
myhelper(1:4)
```

```
[1] 1 2 3 4
attr(,"class")
[1] "myarray"
```

## Task 4

Please include your write-up here...

