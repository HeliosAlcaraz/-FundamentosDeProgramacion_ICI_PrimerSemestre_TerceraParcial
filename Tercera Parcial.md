# Problemas resueltos en clase con Diagramas de Flujo de Datos
## Ejercicio 1.- Utilizando dos vectores capture la edad y el semestre de _**n**_ estudiantes.
### ANÁLISIS
Datos de entrada: n, edad, sem\
Variables: A, B, n, edad, sem, i\
Datos de salida: A, B
### DFD
![1_DFD](https://user-images.githubusercontent.com/113320901/200151734-3e6f3e39-b306-41e9-87f7-08aeaf5c1b63.png)

### PRUEBA DE ESCRITORIO
| # | n |    n<=0 OR n>100    | i |  i<n  | edad | edad<=0 OR edad>130 |A[i]=edad|sem |sem<=0 OR sem>12|B[i]=sem |i++|
|---|-- |-------------------- |-- |------ |----- |-------------------- |-------- |--- |--------------- |-------- |-- |
| 1 |-1 | -1<=0 OR -1>100 sí  | - |  -    |  -   |          -          |    -    |  - |       -        |    -    | - |
| 2 | 0 |  0<=0 OR  0>100 sí  | - |  -    |  -   |          -          |    -    |  - |       -        |    -    | - |
| 3 | 3 |  3<=0 OR  3>100 no  | 0 | 0<3 sí|  17  | 17<=0 OR 17>130  no | A[0]=17 |  1 |1<=0 OR 1>12  no|  B[0]=1 | 1 |
| 4 | 3 |  3<=0 OR  3>100 no  | 1 | 1<3 sí|  22  | 22<=0 OR 22>130  no | A[1]=22 |  7 |7<=0 OR 7>12  no|  B[1]=7 | 2 |
| 5 | 3 |  3<=0 OR  3>100 no  | 2 | 2<3 sí|  18  | 18<=0 OR 18>130  no | A[2]=18 |  1 |1<=0 OR 1>12  no|  B[2]=1 | 3 |
| 6 | 3 |  3<=0 OR  3>100 no  | 3 | 3<3 no|  -   |          -          |    -    |  - |       -        |    -    | - |
| 7 |101|101<=0 OR 101>100 sí | - |  -    |  -   |          -          |    -    |  - |       -        |    -    | - |

### CÓDIGO EN JAVA
![1_DFD_CODE1](https://user-images.githubusercontent.com/113320901/200198880-9f8ef64e-50b0-4757-9a21-4929487f34ac.png)

![1_DFD_CODE2](https://user-images.githubusercontent.com/113320901/200198891-c322739a-4a32-443f-afd5-e0d9bb743120.png)

![1_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/200198901-4bb459d8-1a23-4d37-910b-79ed9db8f117.png)



## Ejercicio 2.- Utilizando una matriz, capturar la edad y semestre de _**n**_ estudiantes.
### ANÁLISIS
Datos de entrada: n, edad, sem\
Variables: M, n, edad, sem, i\
Datos de salida: M
### DFD
![2_DFD](https://user-images.githubusercontent.com/113320901/200193284-77be313b-08f1-4c3a-a83f-bc45dd23ea33.png)

### PRUEBA DE ESCRITORIO
|#  | n |  n<=0 OR n>100     | i | i<n   | edad |edad<0 OR edad>130   |M[i,0]=edad | sem |sem<1 OR sem>12   |M[i,1]=sem | i++ |
|-- |-- |------------------- |-- |------ |----- |-------------------- |----------- |---- |----------------- |---------- |---- |
| 1 | 0 |  0<=0 OR 0>100 sí  | - |   -   |   -  |         -           |      -     |  -  |         -        |      -    |  -  |
| 2 |101|101<=0 OR 101>100 sí| - |   -   |   -  |         -           |      -     |  -  |         -        |      -    |  -  |
| 3 | 2 |2<=0 OR 2>100 no    | 0 |0<2 si | 131  | 131<0 OR 131>130 sí |      -     |  -  |         -        |      -    |  -  |
| 4 | 2 |2<=0 OR 2>100 no    | 0 |0<2 si |  -1  |  -1<0 OR -1>130 sí  |      -     |  -  |         -        |      -    |  -  |
| 5 | 2 |2<=0 OR 2>100 no    | 0 |0<2 si |  17  |  17<0 OR 17>130 no  |  M[0,0]=17 |  1  |  1<1 OR 1>12  no |  M[0,1]=1 |  1  |
| 6 | 2 |2<=0 OR 2>100 no    | 1 |1<2 si |  22  |  22<0 OR 22>130 no  |  M[1,0]=22 |  7  |  7<1 OR 7>12  no |  M[1,1]=7 |  2  |
| 7 | 2 |2<=0 OR 2>100 no    | 2 |2<2 no |   -  |         -           |      -     |  -  |         -        |      -    |  -  |
| 8 | 3 |3<=0 OR 3>100 no    | 0 |0<3 si |  18  |  18<0 OR 18>130 no  |  M[0,0]=18 |  1  |  1<1 OR 1>12  no |  M[0,1]=1 |  1  |
| 9 | 3 |3<=0 OR 3>100 no    | 1 |1<3 si |  19  |  19<0 OR 19>130 no  |  M[1,0]=19 |  3  |  3<1 OR 3>12  no |  M[1,1]=3 |  2  |
| 10| 3 |3<=0 OR 3>100 no    | 2 |2<3 si |  23  |  23<0 OR 23>130 no  |  M[2,0]=23 |  9  |  9<1 OR 9>12  no |  M[2,1]=9 |  3  |
| 11| 3 |3<=0 OR 3>100 no    | 3 |3<3 no |   -  |         -           |      -     |  -  |         -        |      -    |  -  |

### CÓDIGO EN JAVA
![2_DFD_CODE1](https://user-images.githubusercontent.com/113320901/200193318-8ed7f6b4-b0eb-4c7a-8492-d34c1bae3f88.png)

![2_DFD_CODE2](https://user-images.githubusercontent.com/113320901/200193328-2ee48f5e-d216-40e7-bd78-134c31a87944.png)

![2_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/200193336-0a53f81c-2941-46bc-a440-7138d487ce6f.png)



## Ejercicio 3.- Rellenar una matriz cuadrada de _**nxn**_ con un número leído del teclado.
### ANÁLISIS
Datos de entrada: n, num\
Variables: M, n, num, i, j\
Datos de salida: M
### DFD
![3_DFD](https://user-images.githubusercontent.com/113320901/200193444-2c52390e-998a-4505-be88-00843cb1d95e.png)

### PRUEBA DE ESCRITORIO
|#  | n |  n<=0 OR n>100     | num | i | i<n | j | j<n | M[i,j]=num | i++ | j++ |
|-- |-- |------------------- |---- |-- |---- |-- |---- |----------- |---- |---- |
| 1 | 0 |  0<=0 OR 0>100 sí  |  -  | - |  -  | - |  -  |      -     |  -  |  -  |
| 2 |103|103<=0 OR 103>100 sí|  -  | - |  -  | - |  -  |      -     |  -  |  -  |
| 3 | 5 |  5<=0 OR 5>100 no  |  35 | 0 | 0<5 | 0 | 0<5 | M[0,0]=35  |  -  |  1  |
| 4 | 5 |  5<=0 OR 5>100 no  |  35 | 0 | 0<5 | 1 | 1<5 | M[0,1]=35  |  -  |  2  |
| 5 | 5 |  5<=0 OR 5>100 no  |  35 | 0 | 0<5 | 2 | 2<5 | M[0,2]=35  |  -  |  3  |
| 6 | 5 |  5<=0 OR 5>100 no  |  35 | 0 | 0<5 | 3 | 3<5 | M[0,3]=35  |  -  |  4  |
| 7 | 5 |  5<=0 OR 5>100 no  |  35 | 0 | 0<5 | 4 | 4<5 | M[0,4]=35  |  -  |  5  |
| 8 | 5 |  5<=0 OR 5>100 no  |  35 | 0 | 0<5 | 5 | 5<5 |      -     |  1  |  -  |
| 9 | 5 |  5<=0 OR 5>100 no  |  35 | 1 | 1<5 | 0 | 0<5 | M[1,0]=35  |  -  |  1  |
|10 | 5 |  5<=0 OR 5>100 no  |  35 | 1 | 1<5 | 1 | 1<5 | M[1,1]=35  |  -  |  2  |
|11 | 5 |  5<=0 OR 5>100 no  |  35 | 1 | 1<5 | 2 | 2<5 | M[1,2]=35  |  -  |  3  |
|12 | 5 |  5<=0 OR 5>100 no  |  35 | 1 | 1<5 | 3 | 3<5 | M[1,3]=35  |  -  |  4  |
|13 | 5 |  5<=0 OR 5>100 no  |  35 | 1 | 1<5 | 4 | 4<5 | M[1,4]=35  |  -  |  5  |
|14 | 5 |  5<=0 OR 5>100 no  |  35 | 1 | 1<5 | 5 | 5<5 |      -     |  2  |  -  |
|15 | 5 |  5<=0 OR 5>100 no  |  35 | 2 | 2<5 | 0 | 0<5 | M[2,0]=35  |  -  |  1  |
|16 | 5 |  5<=0 OR 5>100 no  |  35 | 2 | 2<5 | 1 | 1<5 | M[2,1]=35  |  -  |  2  |
|17 | 5 |  5<=0 OR 5>100 no  |  35 | 2 | 2<5 | 2 | 2<5 | M[2,2]=35  |  -  |  3  |
|18 | 5 |  5<=0 OR 5>100 no  |  35 | 2 | 2<5 | 3 | 3<5 | M[2,3]=35  |  -  |  4  |
|19 | 5 |  5<=0 OR 5>100 no  |  35 | 2 | 2<5 | 4 | 4<5 | M[2,4]=35  |  -  |  5  |
|20 | 5 |  5<=0 OR 5>100 no  |  35 | 2 | 2<5 | 5 | 5<5 |      -     |  3  |  -  |
|21 | 5 |  5<=0 OR 5>100 no  |  35 | 3 | 3<5 | 0 | 0<5 | M[3,0]=35  |  -  |  1  |
|22 | 5 |  5<=0 OR 5>100 no  |  35 | 3 | 3<5 | 1 | 1<5 | M[3,1]=35  |  -  |  2  |
|23 | 5 |  5<=0 OR 5>100 no  |  35 | 3 | 3<5 | 2 | 2<5 | M[3,2]=35  |  -  |  3  |
|24 | 5 |  5<=0 OR 5>100 no  |  35 | 3 | 3<5 | 3 | 3<5 | M[3,3]=35  |  -  |  4  |
|25 | 5 |  5<=0 OR 5>100 no  |  35 | 3 | 3<5 | 4 | 4<5 | M[3,4]=35  |  -  |  5  |
|26 | 5 |  5<=0 OR 5>100 no  |  35 | 3 | 3<5 | 5 | 5<5 |      -     |  4  |  -  |
|27 | 5 |  5<=0 OR 5>100 no  |  35 | 4 | 4<5 | 0 | 0<5 | M[4,0]=35  |  -  |  1  |
|28 | 5 |  5<=0 OR 5>100 no  |  35 | 4 | 4<5 | 1 | 1<5 | M[4,1]=35  |  -  |  2  |
|29 | 5 |  5<=0 OR 5>100 no  |  35 | 4 | 4<5 | 2 | 2<5 | M[4,2]=35  |  -  |  3  |
|30 | 5 |  5<=0 OR 5>100 no  |  35 | 4 | 4<5 | 3 | 3<5 | M[4,3]=35  |  -  |  4  |
|31 | 5 |  5<=0 OR 5>100 no  |  35 | 4 | 4<5 | 4 | 4<5 | M[4,4]=35  |  -  |  5  |
|32 | 5 |  5<=0 OR 5>100 no  |  35 | 4 | 4<5 | 5 | 5<5 |      -     |  5  |  -  |
|33 | 5 |  5<=0 OR 5>100 no  |  35 | 5 | 5<5 | - |  -  |      -     |  -  |  -  |

### CÓDIGO EN JAVA
![3_DFD_CODE1](https://user-images.githubusercontent.com/113320901/200193475-b5164fe6-9dff-4ffd-8bc2-062ac515d172.png)

![3_DFD_CODE2](https://user-images.githubusercontent.com/113320901/200193484-8dfc00d3-fbb4-41bb-9eb3-5339a0834ab5.png)

![3_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/200193498-fa902546-8100-49d2-95b2-17ac9ec0c487.png)



## Ejercicio 4.- Rellenar una matriz con números consecutivos hasta _**nxn**_.
### ANÁLISIS
Datos de entrada: n\
Variables: M, n, c, i, j\
Datos de salida: M
### DFD
![4_DFD](https://user-images.githubusercontent.com/113320901/200193757-28ee8f85-cb74-4c91-bb1d-31b5de156986.png)

### PRUEBA DE ESCRITORIO
|#  | c | n |  n<2 OR n>100  | i | i<n | j | j<n |M[i,j]=c | c++ | i++ | j++ |
|-- |-- |-- |--------------- |-- |---- |-- |---- |-------- |---- |---- |---- |
| 1 | 1 | 3 | 3<2 OR 3>100 no| 0 | 0<3 | 0 | 0<3 |M[0,0]=1 |  2  |  -  |  1  |
| 2 | 2 | 3 | 3<2 OR 3>100 no| 0 | 0<3 | 1 | 1<3 |M[0,1]=2 |  3  |  -  |  2  |
| 3 | 3 | 3 | 3<2 OR 3>100 no| 0 | 0<3 | 2 | 2<3 |M[0,2]=3 |  4  |  -  |  3  |
| 4 | 4 | 3 | 3<2 OR 3>100 no| 0 | 0<3 | 3 | 3<3 |    -    |  -  |  1  |  -  |
| 5 | 4 | 3 | 3<2 OR 3>100 no| 1 | 1<3 | 0 | 0<3 |M[1,0]=4 |  5  |  -  |  1  |
| 6 | 5 | 3 | 3<2 OR 3>100 no| 1 | 1<3 | 1 | 1<3 |M[1,1]=5 |  6  |  -  |  2  |
| 7 | 6 | 3 | 3<2 OR 3>100 no| 1 | 1<3 | 2 | 2<3 |M[1,2]=6 |  7  |  -  |  3  |
| 8 | 7 | 3 | 3<2 OR 3>100 no| 1 | 1<3 | 3 | 3<3 |    -    |  -  |  2  |  -  |
| 9 | 7 | 3 | 3<2 OR 3>100 no| 2 | 2<3 | 0 | 0<3 |M[2,0]=7 |  8  |  -  |  1  |
|10 | 8 | 3 | 3<2 OR 3>100 no| 2 | 2<3 | 1 | 1<3 |M[2,1]=8 |  9  |  -  |  2  |
|11 | 9 | 3 | 3<2 OR 3>100 no| 2 | 2<3 | 2 | 2<3 |M[2,2]=9 | 10  |  -  |  3  |
|12 |10 | 3 | 3<2 OR 3>100 no| 2 | 2<3 | 3 | 3<3 |    -    |  -  |  3  |  -  |
|13 |10 | 3 | 3<2 OR 3>100 no| 3 | 3<3 | - |  -  |    -    |  -  |  -  |  -  |

### CÓDIGO EN JAVA
![4_DFD_CODE1](https://user-images.githubusercontent.com/113320901/200193787-a62258e7-4751-4a46-a8f8-968d9f04097e.png)

![4_DFD_CODE2](https://user-images.githubusercontent.com/113320901/200193795-09a76f9b-4d62-493f-8ff3-b29a62f3b95c.png)

![4_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/200193807-6effbdbc-c319-4c40-9085-27e9ceac9beb.png)



## Ejercicio 5.- Rellenar una matriz de la siguiente manera:
![Ejercicio 5](https://user-images.githubusercontent.com/113320901/200193955-529bf597-328f-4e5a-8bd6-0af6feb20cff.png)

### ANÁLISIS
Datos de entrada: num\
Variables: M, num, i, j\
Datos de salida: M
### DFD
![5_DFD](https://user-images.githubusercontent.com/113320901/200194079-ce0f8df6-436f-414d-8599-576706832ea0.png)

### PRUEBA DE ESCRITORIO
|#  | num | i |  i<4  | j | j<4 |M[j,i]=num| num++ | j++ | num=num-4| i++ |
|-- |---- |-- |------ |-- |---- |--------- |------ |---- |--------- |---- |
| 1 |  1  | 0 |  0<4  | 0 | 0<4 | M[0,0]=1 |   2   |  1  |    -     |  -  |
| 2 |  2  | 0 |  0<4  | 1 | 1<4 | M[1,0]=2 |   3   |  2  |    -     |  -  |
| 3 |  3  | 0 |  0<4  | 2 | 2<4 | M[2,0]=3 |   4   |  3  |    -     |  -  |
| 4 |  4  | 0 |  0<4  | 3 | 3<4 | M[3,0]=4 |   5   |  4  |    -     |  -  |
| 5 |  5  | 0 |  0<4  | 4 | 4<4 |     -    |   -   |  -  | num=5-4  |  1  |
| 6 |  1  | 1 |  1<4  | 0 | 0<4 | M[0,1]=1 |   2   |  1  |    -     |  -  |
| 7 |  2  | 1 |  1<4  | 1 | 1<4 | M[1,1]=2 |   3   |  2  |    -     |  -  |
| 8 |  3  | 1 |  1<4  | 2 | 2<4 | M[2,1]=3 |   4   |  3  |    -     |  -  |
| 9 |  4  | 1 |  1<4  | 3 | 3<4 | M[3,1]=4 |   5   |  4  |    -     |  -  |
|10 |  5  | 1 |  1<4  | 4 | 4<4 |     -    |   -   |  -  | num=5-4  |  2  |
|11 |  1  | 2 |  2<4  | 0 | 0<4 | M[0,2]=1 |   2   |  1  |    -     |  -  |
|12 |  2  | 2 |  2<4  | 1 | 1<4 | M[1,2]=2 |   3   |  2  |    -     |  -  |
|13 |  3  | 2 |  2<4  | 2 | 2<4 | M[2,2]=3 |   4   |  3  |    -     |  -  |
|14 |  4  | 2 |  2<4  | 3 | 3<4 | M[3,2]=4 |   5   |  4  |    -     |  -  |
|15 |  5  | 2 |  2<4  | 4 | 4<4 |     -    |   -   |  -  | num=5-4  |  3  |
|16 |  1  | 3 |  3<4  | 0 | 0<4 | M[0,3]=1 |   2   |  1  |    -     |  -  |
|17 |  2  | 3 |  3<4  | 1 | 1<4 | M[1,3]=2 |   3   |  2  |    -     |  -  |
|18 |  3  | 3 |  3<4  | 2 | 2<4 | M[2,3]=3 |   4   |  3  |    -     |  -  |
|19 |  4  | 3 |  3<4  | 3 | 3<4 | M[3,3]=4 |   5   |  4  |    -     |  -  |
|20 |  5  | 3 |  3<4  | 4 | 4<4 |     -    |   -   |  -  | num=5-4  |  4  |
|21 |  1  | 4 |  4<4  | - |  -  |     -    |   -   |  -  |    -     |  -  |

### CÓDIGO EN JAVA
![5_DFD_CODE](https://user-images.githubusercontent.com/113320901/200194130-30698e1f-4809-4a91-a701-fb3cee4cee88.png)

![5_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/200194152-e8f170f8-3ac1-4ad1-a25b-0255eb410d42.png)



## Ejercicio 6.- Generar una matriz que quede de la siguiente manera:
![Ejercicio 6](https://user-images.githubusercontent.com/113320901/200194875-a9c29d3b-251c-4218-8eb1-2e73d5be8d9a.png)

### ANÁLISIS
Datos de entrada: ninguno\
Variables: M, cont, i, j\
Datos de salida: M
### DFD
![6_DFD](https://user-images.githubusercontent.com/113320901/200194603-988d5cdc-935c-4acb-a07f-2dadf84f1d44.png)

### PRUEBA DE ESCRITORIO
|#  |  |  |  |  |  |
| ----------- |----------- |----------- |----------- |----------- |----------- |
| 1 |  |  |  |  |  |
| 2 |  |  |  |  |  |
| 3 |  |  |  |  |  |
| 4 |  |  |  | |  |
| 5 |  |  | | |  |
| 6 |  |  | | |  |
| 7 |  |  | | |  |
| 8 |  |  | | |  |
| 9 |  |  | | |  |
| 10 |  |  | | |  |

### CÓDIGO EN JAVA
![6_DFD_CODE](https://user-images.githubusercontent.com/113320901/200194662-cbb6a1bb-7735-4e1f-86a7-f1d44bc62795.png)

![6_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/200194671-24d7509d-d61e-4b48-ab2c-9271944a6afe.png)
