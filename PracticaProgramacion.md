practica\_programacion
================
diego vilca torres
3/7/2021

## Ejercicio 1

``` r
10000%%3
```

    ## [1] 1

## Ejercicio 2

``` r
4560%%3
```

    ## [1] 0

``` r
#residuo = 0
```

## Ejercicio 3

``` r
vec<- c(2:87)
b<-vec%%7
b[b==0]
```

    ##  [1] 0 0 0 0 0 0 0 0 0 0 0 0

``` r
# 12 numeros son divisibles por 7
```

## Ejercicio 4

``` r
v1 <- c(7:3)
v2 <- c(seq(from=5, to=25, by=5))
A <- ifelse(v1%%2==0, "TRUE", "FALSE")
B <- ifelse(v2>10, "TRUE", "FALSE")
data.frame(A,B)
```

    ##       A     B
    ## 1 FALSE FALSE
    ## 2  TRUE FALSE
    ## 3 FALSE  TRUE
    ## 4  TRUE  TRUE
    ## 5 FALSE  TRUE

``` r
# se cumple A y B simultanamente en la posición 4
```

## Ejercicio 5

``` r
V <- (1:100)
sum(1:100)
```

    ## [1] 5050

``` r
sum_v<- (100*101)/2
# resultado = 5050
```

## Ejercicio 6

``` r
vector5<- c(1, -4, 4, 9, -4)
min(vector5)
```

    ## [1] -4

``` r
nivel<-c(1, -4, 4, 9, -4)
nivel[2]
```

    ## [1] -4

``` r
nivel[5]
```

    ## [1] -4

``` r
ifelse(vector5==min(vector5), "VMIN", "---")
```

    ## [1] "---"  "VMIN" "---"  "---"  "VMIN"

## Ejercicio 7

``` r
prod(1:8)
```

    ## [1] 40320

``` r
#resultado = 40320
```

## Ejercicio 8

``` r
i<- 3:7
sum(exp(i))
```

    ## [1] 1723.159

``` r
#resultado = 1723.159
```

## Ejercicio 9

``` r
i<-1:10
prod(log(sqrt(i)))
```

    ## [1] 0

``` r
#resultado = 0
```

## Ejercicio 10

``` r
a_segmento_circular<-function(R,r,ang){
  A<-((r^2)/2)*((pi*ang/180)-sin(ang))
  return(A)
}
a_segmento_circular (10,5,30)
```

    ## [1] 18.89538

## Ejercicio 11

``` r
a<- 1:10
b<- 10:1
vec_c<- c(21, 30, 22, 17, 18, 16)
rev(vec_c)
```

    ## [1] 16 18 17 22 30 21

## Ejercicio 12

``` r
i<- 10:100
sum(i^3+ 4*i^2)
```

    ## [1] 26852735

``` r
#resultado = 26852735
```

## Ejercicio 13

``` r
i<- 1:25
sum(2^i/i +3^i/i^2)
```

    ## [1] 2129170437

``` r
# resultado = 2129170437
```

## Ejercicio 14

``` r
d.f<-mtcars
#a
d.f[d.f$mpg<18.0,]
```

    ##                      mpg cyl  disp  hp drat    wt  qsec vs am gear carb
    ## Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
    ## Merc 280C           17.8   6 167.6 123 3.92 3.440 18.90  1  0    4    4
    ## Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
    ## Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
    ## Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
    ## Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
    ## Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
    ## Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
    ## Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
    ## AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
    ## Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
    ## Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
    ## Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8

``` r
#b
d.f[d.f$cyl==4,]
```

    ##                 mpg cyl  disp  hp drat    wt  qsec vs am gear carb
    ## Datsun 710     22.8   4 108.0  93 3.85 2.320 18.61  1  1    4    1
    ## Merc 240D      24.4   4 146.7  62 3.69 3.190 20.00  1  0    4    2
    ## Merc 230       22.8   4 140.8  95 3.92 3.150 22.90  1  0    4    2
    ## Fiat 128       32.4   4  78.7  66 4.08 2.200 19.47  1  1    4    1
    ## Honda Civic    30.4   4  75.7  52 4.93 1.615 18.52  1  1    4    2
    ## Toyota Corolla 33.9   4  71.1  65 4.22 1.835 19.90  1  1    4    1
    ## Toyota Corona  21.5   4 120.1  97 3.70 2.465 20.01  1  0    3    1
    ## Fiat X1-9      27.3   4  79.0  66 4.08 1.935 18.90  1  1    4    1
    ## Porsche 914-2  26.0   4 120.3  91 4.43 2.140 16.70  0  1    5    2
    ## Lotus Europa   30.4   4  95.1 113 3.77 1.513 16.90  1  1    5    2
    ## Volvo 142E     21.4   4 121.0 109 4.11 2.780 18.60  1  1    4    2

``` r
#c
d.f[d.f$wt>2.500&d.f$am==1,]
```

    ##                 mpg cyl disp  hp drat    wt  qsec vs am gear carb
    ## Mazda RX4      21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
    ## Mazda RX4 Wag  21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
    ## Ford Pantera L 15.8   8  351 264 4.22 3.170 14.50  0  1    5    4
    ## Ferrari Dino   19.7   6  145 175 3.62 2.770 15.50  0  1    5    6
    ## Maserati Bora  15.0   8  301 335 3.54 3.570 14.60  0  1    5    8
    ## Volvo 142E     21.4   4  121 109 4.11 2.780 18.60  1  1    4    2

## Ejercicio 15

``` r
d.f<-mtcars
#a
d.f[d.f$mpg<18.0,]
```

    ##                      mpg cyl  disp  hp drat    wt  qsec vs am gear carb
    ## Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
    ## Merc 280C           17.8   6 167.6 123 3.92 3.440 18.90  1  0    4    4
    ## Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
    ## Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
    ## Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
    ## Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
    ## Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
    ## Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
    ## Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
    ## AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
    ## Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
    ## Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
    ## Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8

``` r
#b
d.f[d.f$cyl==4,]
```

    ##                 mpg cyl  disp  hp drat    wt  qsec vs am gear carb
    ## Datsun 710     22.8   4 108.0  93 3.85 2.320 18.61  1  1    4    1
    ## Merc 240D      24.4   4 146.7  62 3.69 3.190 20.00  1  0    4    2
    ## Merc 230       22.8   4 140.8  95 3.92 3.150 22.90  1  0    4    2
    ## Fiat 128       32.4   4  78.7  66 4.08 2.200 19.47  1  1    4    1
    ## Honda Civic    30.4   4  75.7  52 4.93 1.615 18.52  1  1    4    2
    ## Toyota Corolla 33.9   4  71.1  65 4.22 1.835 19.90  1  1    4    1
    ## Toyota Corona  21.5   4 120.1  97 3.70 2.465 20.01  1  0    3    1
    ## Fiat X1-9      27.3   4  79.0  66 4.08 1.935 18.90  1  1    4    1
    ## Porsche 914-2  26.0   4 120.3  91 4.43 2.140 16.70  0  1    5    2
    ## Lotus Europa   30.4   4  95.1 113 3.77 1.513 16.90  1  1    5    2
    ## Volvo 142E     21.4   4 121.0 109 4.11 2.780 18.60  1  1    4    2

``` r
#c
d.f[d.f$wt>2.500&d.f$am==1,]
```

    ##                 mpg cyl disp  hp drat    wt  qsec vs am gear carb
    ## Mazda RX4      21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
    ## Mazda RX4 Wag  21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
    ## Ford Pantera L 15.8   8  351 264 4.22 3.170 14.50  0  1    5    4
    ## Ferrari Dino   19.7   6  145 175 3.62 2.770 15.50  0  1    5    6
    ## Maserati Bora  15.0   8  301 335 3.54 3.570 14.60  0  1    5    8
    ## Volvo 142E     21.4   4  121 109 4.11 2.780 18.60  1  1    4    2
