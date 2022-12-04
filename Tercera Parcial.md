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
|#  | cont | i |  i<4  | j | j<4 |  i==j  | M[j,i]=cont | cont++ | j++ | i++ |
|-- |----- |-- |------ |-- |---- |------- |------------ |------- |---- |---- |
| 1 |  1   | 0 |  0<4  | 0 | 0<4 |0==0 sí |  M[0,0]=1   |   2    |  1  |  -  |
| 2 |  2   | 0 |  0<4  | 1 | 1<4 |0==1 no |      -      |   -    |  2  |  -  |
| 3 |  2   | 0 |  0<4  | 2 | 2<4 |0==2 no |      -      |   -    |  3  |  -  |
| 4 |  2   | 0 |  0<4  | 3 | 3<4 |0==3 no |      -      |   -    |  4  |  -  |
| 5 |  2   | 0 |  0<4  | 4 | 4<4 |    -   |      -      |   -    |  -  |  1  |
| 6 |  2   | 1 |  1<4  | 0 | 0<4 |1==0 no |      -      |   -    |  1  |  -  |
| 7 |  2   | 1 |  1<4  | 1 | 1<4 |1==1 sí |  M[1,1]=2   |   3    |  2  |  -  |
| 8 |  3   | 1 |  1<4  | 2 | 2<4 |1==2 no |      -      |   -    |  3  |  -  |
| 9 |  3   | 1 |  1<4  | 3 | 3<4 |1==3 no |      -      |   -    |  4  |  -  |
|10 |  3   | 1 |  1<4  | 4 | 4<4 |    -   |      -      |   -    |  -  |  2  |
|11 |  3   | 2 |  2<4  | 0 | 0<4 |2==0 no |      -      |   -    |  1  |  -  |
|12 |  3   | 2 |  2<4  | 1 | 1<4 |2==1 no |      -      |   -    |  2  |  -  |
|13 |  3   | 2 |  2<4  | 2 | 2<4 |2==2 sí |  M[2,2]=3   |   4    |  3  |  -  |
|14 |  4   | 2 |  2<4  | 3 | 3<4 |2==3 no |      -      |   -    |  4  |  -  |
|15 |  4   | 2 |  2<4  | 4 | 4<4 |    -   |      -      |   -    |  -  |  3  |
|16 |  4   | 3 |  3<4  | 0 | 0<4 |3==0 no |      -      |   -    |  1  |  -  |
|17 |  4   | 3 |  3<4  | 1 | 1<4 |3==1 no |      -      |   -    |  2  |  -  |
|18 |  4   | 3 |  3<4  | 2 | 2<4 |3==2 no |      -      |   -    |  3  |  -  |
|19 |  4   | 3 |  3<4  | 3 | 3<4 |3==3 sí |  M[3,3]=4   |   5    |  4  |  -  |
|20 |  5   | 3 |  3<4  | 4 | 4<4 |    -   |      -      |   -    |  -  |  4  |
|21 |  5   | 4 |  4<4  | - |  -  |    -   |      -      |   -    |  -  |  -  |

### CÓDIGO EN JAVA
![6_DFD_CODE](https://user-images.githubusercontent.com/113320901/200194662-cbb6a1bb-7735-4e1f-86a7-f1d44bc62795.png)

![6_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/200194671-24d7509d-d61e-4b48-ab2c-9271944a6afe.png)



## Ejercicio 7.- Convertir una matriz de nxn a un array (vector).

### ANÁLISIS
Datos de entrada: n\
Variables: A, M, n, c, cont, i, j\
Datos de salida: A
### DFD
![7_DFD](https://user-images.githubusercontent.com/113320901/202078205-e0b81507-0cf6-425d-bb8c-5141ad403bb0.png)

### PRUEBA DE ESCRITORIO
__Llenado de la matriz__
|#  |  n   |cont| n<1 OR n>100   | i | i<n | j | j<n |M[i,j]=cont|cont++| j++ | i++ |
|-- |----- |--- |--------------- |-- |---- |-- |---- |---------- |----- |---- |---- |
| 1 |  2   | 1  | 2<1 OR 2>100 no| 0 | 0<2 | 0 | 0<2 | M[0,0]=1  |  2   |  1  |  -  |
| 2 |  2   | 2  | 2<1 OR 2>100 no| 0 | 0<2 | 1 | 1<2 | M[0,1]=2  |  3   |  2  |  -  |
| 3 |  2   | 3  | 2<1 OR 2>100 no| 0 | 0<2 | 2 | 2<2 |     -     |  -   |  -  |  1  |
| 4 |  2   | 3  | 2<1 OR 2>100 no| 1 | 1<2 | 0 | 0<2 | M[1,0]=3  |  4   |  1  |  -  |
| 5 |  2   | 4  | 2<1 OR 2>100 no| 1 | 1<2 | 1 | 1<2 | M[1,1]=4  |  5   |  2  |  -  |
| 6 |  2   | 5  | 2<1 OR 2>100 no| 1 | 1<2 | 2 | 2<2 |     -     |  -   |  -  |  2  |
| 7 |  2   | 5  | 2<1 OR 2>100 no| 2 | 2<2 | - |  -  |     -     |  -   |  -  |  -  |

__Pase de elementos de la matriz al vector__
|#  |  n   | c | i | i<n | j | j<n |A[c]=M[i,j]|c++| j++ | i++ |
|-- |----- |-- |-- |---- |-- |---- |---------- |-- |---- |---- |
| 1 |  2   | 0 | 0 | 0<2 | 0 | 0<2 |A[0]=M[0,0]| 1 |  1  |  -  |
| 2 |  2   | 1 | 0 | 0<2 | 1 | 1<2 |A[1]=M[0,1]| 2 |  2  |  -  |
| 3 |  2   | 2 | 0 | 0<2 | 2 | 2<2 |     -     | - |  -  |  1  |
| 4 |  2   | 2 | 1 | 1<2 | 0 | 0<2 |A[2]=M[1,0]| 3 |  1  |  -  |
| 5 |  2   | 3 | 1 | 1<2 | 1 | 1<2 |A[3]=M[1,1]| 4 |  2  |  -  |
| 6 |  2   | 4 | 1 | 1<2 | 2 | 2<2 |     -     | - |  -  |  2  |
| 7 |  2   | 4 | 2 | 2<2 | - |  -  |     -     | - |  -  |  -  |

__Mostrar los elementos del vector__
|#  |  n   | i | i<(n*n) | A[i] | i++ |
|-- |----- |-- |------- |----- |---- |
| 1 |  2  | 0 | 0<(2*2) | A[0] |  1  |
| 2 |  2  | 1 | 1<(2*2) | A[1] |  2  |
| 3 |  2  | 2 | 2<(2*2) | A[2] |  3  |
| 4 |  2  | 3 | 3<(2*2) | A[3] |  4  |
| 5 |  2  | 4 | 4<(2*2) |  -   |  -  |

### CÓDIGO EN JAVA
![7_DFD_CODE1](https://user-images.githubusercontent.com/113320901/202329601-0e557483-0812-4f0d-bb8e-7550361d57f3.png)

![7_DFD_CODE2](https://user-images.githubusercontent.com/113320901/202329623-a5715033-4b61-4440-b311-c25a30da2978.png)

![7_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/202329640-a68d2d95-40e9-4efd-a1da-edcdd7313efa.png)



## Ejercicio 9.- Pregunte las dimensiones de una matriz. El rango es [5,5]. Valide que sea cuadrada y obtenga la suma de la diagonal principal y la inversa. Determine cuál es mayor. Pregunte los valores para llenar la matriz.

### ANÁLISIS
Datos de entrada: num\
Variables: M, sum, sum2, num, i, j\
Datos de salida: "Diagonal principal es mayor" o "Diagonal inversa es mayor"
### DFD
![9_DFD](https://user-images.githubusercontent.com/113320901/204063853-1c403620-f037-4721-a45a-1d0194e3dcc4.png)

### PRUEBA DE ESCRITORIO
__Llenado de la matriz__
|#  | i | i<5  | j | j<5  | num | M[i,j]=num| j++ | i++ |
|-- |-- |----- |-- |----- |-----|---------- |---- |---- |
| 1 | 0 |0<5 sí| 0 |0<5 sí|  2  | M[0,0]=2  |  1  |  -  |
| 2 | 0 |0<5 sí| 1 |1<5 sí|  8  | M[0,1]=8  |  2  |  -  |
| 3 | 0 |0<5 sí| 2 |2<5 sí|  9  | M[0,2]=9  |  3  |  -  |
| 4 | 0 |0<5 sí| 3 |3<5 sí|  4  | M[0,3]=4  |  4  |  -  |
| 5 | 0 |0<5 sí| 4 |4<5 sí|  5  | M[0,4]=5  |  5  |  -  |
| 6 | 0 |0<5 sí| 5 |5<5 no|  -  |      -    |  -  |  1  |
| 7 | 1 |1<5 sí| 0 |0<5 sí|  5  | M[1,0]=5  |  1  |  -  |
| 8 | 1 |1<5 sí| 1 |1<5 sí|  2  | M[1,1]=2  |  2  |  -  |
| 9 | 1 |1<5 sí| 2 |2<5 sí|  6  | M[1,2]=6  |  3  |  -  |
|10 | 1 |1<5 sí| 3 |3<5 sí|  7  | M[1,3]=7  |  4  |  -  |
|11 | 1 |1<5 sí| 4 |4<5 sí|  6  | M[1,4]=6  |  5  |  -  |
|12 | 1 |1<5 sí| 5 |5<5 no|  -  |      -    |  -  |  2  |

__Suma de los elementos de la diagonal principal de la matriz__
|#  | sum  |sum2| num | i | i<5  | j | j<5  |  i==j  |sum=sum+num| j++ | i++ |
|-- |----- |--- |---- |-- |----- |-- |----- |------- |---------- |---- |---- |
| 1 |  0   |  0 |  2  | 0 |0<5 sí| 0 |0<5 sí| 0==0 sí|  sum=0+2  |  1  |  -  |
| 2 |  2   |  0 |  8  | 0 |0<5 sí| 1 |1<5 sí| 0==1 no|     -     |  2  |  -  |
| 3 |  2   |  0 |  9  | 0 |0<5 sí| 2 |2<5 sí| 0==2 no|     -     |  3  |  -  |
| 4 |  2   |  0 |  4  | 0 |0<5 sí| 3 |3<5 sí| 0==3 no|     -     |  4  |  -  |
| 5 |  2   |  0 |  5  | 0 |0<5 sí| 4 |4<5 sí| 0==4 no|     -     |  5  |  -  |
| 6 |  2   |  0 |  -  | 0 |0<5 sí| 5 |5<5 no|    -   |     -     |  -  |  1  |
| 7 |  2   |  0 |  5  | 1 |1<5 sí| 0 |0<5 sí| 1==0 no|     -     |  1  |  -  |
| 8 |  2   |  0 |  2  | 1 |1<5 sí| 1 |1<5 sí| 1==1 sí|  sum=2+2  |  2  |  -  |
| 9 |  4   |  0 |  6  | 1 |1<5 sí| 2 |2<5 sí| 1==2 no|     -     |  3  |  -  |
|10 |  4   |  0 |  7  | 1 |1<5 sí| 3 |3<5 sí| 1==3 no|     -     |  4  |  -  |
|11 |  4   |  0 |  6  | 1 |1<5 sí| 4 |4<5 sí| 1==4 no|     -     |  5  |  -  |
|12 |  4   |  0 |  7  | 1 |1<5 sí| 5 |5<5 no|    -   |     -     |  -  |  2  |

__Suma de los elementos de la diagonal inversa de la matriz__
|#  | sum  |sum2| num | i | i<5  | j | j<5  |  i+j==4  |sum2=sum2+num| j++ | i++ |
|-- |----- |--- |---- |-- |----- |-- |----- |--------- |------------ |---- |---- |
| 1 |  0   |  0 |  2  | 0 |0<5 sí| 0 |0<5 sí| 0+0==4 no|      -      |  1  |  -  |
| 2 |  0   |  0 |  8  | 0 |0<5 sí| 1 |1<5 sí| 0+1==4 no|      -      |  2  |  -  |
| 3 |  0   |  0 |  9  | 0 |0<5 sí| 2 |2<5 sí| 0+2==4 no|      -      |  3  |  -  |
| 4 |  0   |  0 |  4  | 0 |0<5 sí| 3 |3<5 sí| 0+3==4 no|      -      |  4  |  -  |
| 5 |  0   |  0 |  5  | 0 |0<5 sí| 4 |4<5 sí| 0+4==4 sí|   sum2=0+5  |  5  |  -  |
| 6 |  0   |  5 |  -  | 0 |0<5 sí| 5 |5<5 no|     -    |      -      |  -  |  1  |
| 7 |  0   |  5 |  5  | 1 |1<5 sí| 0 |0<5 sí| 1+0==4 no|      -      |  1  |  -  |
| 8 |  0   |  5 |  2  | 1 |1<5 sí| 1 |1<5 sí| 1+1==4 no|      -      |  2  |  -  |
| 9 |  0   |  5 |  6  | 1 |1<5 sí| 2 |2<5 sí| 1+2==4 no|      -      |  3  |  -  |
|10 |  0   |  5 |  7  | 1 |1<5 sí| 3 |3<5 sí| 1+3==4 sí|   sum2=5+7  |  4  |  -  |
|11 |  0   | 12 |  6  | 1 |1<5 sí| 4 |4<5 sí| 1+4==4 no|      -      |  5  |  -  |
|12 |  0   | 12 |  -  | 1 |1<5 sí| 5 |5<5 no|     -    |      -      |  -  |  2  |

### CÓDIGO EN JAVA
![9_DFD_CODE1](https://user-images.githubusercontent.com/113320901/204065410-0d23bfbd-8919-488b-a800-2b241296bdea.png)

![9_DFD_CODE2](https://user-images.githubusercontent.com/113320901/204065415-5084dd0c-7ca4-482c-b518-d8a1d57bf554.png)

![9_DFD_CODE_RUN1](https://user-images.githubusercontent.com/113320901/204065417-8ac278cb-b794-4648-adfc-64720216ecd5.png)

![9_DFD_CODE_RUN2](https://user-images.githubusercontent.com/113320901/204065418-e8e71902-049d-4a16-887f-f3f00e02ab63.png)



## Ejercicio 10.- Almacenar en un array la sumatoria de los números desde uno hasta _**n**_ en cada posición del array (vector). Ejemplo: si _**n**_=3, el array deberá ser 1, 3, 6.

### ANÁLISIS
Datos de entrada: num\
Variables: A, num, a, b, c, i\
Datos de salida: A
### DFD
![10_DFD](https://user-images.githubusercontent.com/113320901/204193332-e477d14a-2815-46f3-af55-ff814e380d90.png)

### PRUEBA DE ESCRITORIO
|#  |  a   |  b  |    num    | A[num+1] |  i  |i<=num |A[i]=a | c=a+b  | a=c | b++ | i++ | c |
|-- |----- |---- |---------- |--------- |---- |------ |------ |------- |---- |---- |---- |-- |
| 1 |  1   |  2  |     4     |  A[4+1]  |  0  |0<=4 sí|A[0]=1 | c=1+2  | a=3 |  3  |  1  | 3 |
| 2 |  3   |  3  |     4     |  A[4+1]  |  1  |1<=4 sí|A[1]=3 | c=3+3  | a=6 |  4  |  2  | 6 |
| 3 |  6   |  4  |     4     |  A[4+1]  |  2  |2<=4 sí|A[2]=6 | c=6+4  | a=10|  5  |  3  |10 |
| 4 | 10   |  5  |     4     |  A[4+1]  |  3  |3<=4 sí|A[3]=10| c=10+5 | a=15|  6  |  4  |15 |
| 5 | 15   |  6  |     4     |  A[4+1]  |  4  |4<=4 sí|A[4]=15| c=15+6 | a=21|  7  |  5  |21 |
| 6 | 21   |  7  |     4     |  A[4+1]  |  5  |5<=4 no|   -   |    -   |  -  |  -  |  -  | - |

### CÓDIGO EN JAVA
![10_DFD_CODE](https://user-images.githubusercontent.com/113320901/204191038-7426ba12-e3a9-400c-af9c-9e5d55eb1a39.png)

![10_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/204191053-0eedd417-ecc7-4701-880d-eea572ef750f.png)



## Ejercicio 11.- Dada una matriz de _**nxm**_, almacenar en un vector los números mayores de cada renglón de la matriz.

### ANÁLISIS
Datos de entrada: n, m, num\
Variables: A, M, i, j, n, m, num, mayor\
Datos de salida: M, A
### DFD
![11_DFD](https://user-images.githubusercontent.com/113320901/205471291-3aeeb61d-9721-42a6-bcb1-1a3023540066.png)

### PRUEBA DE ESCRITORIO
|#  |  n  |  m  |   M[n,m]  | i | i<n | j | j<m | num | M[i,j]=num | j++ | i++ |
|-- |---- |---- |---------- |-- |---- |-- |---- |---- |----------- |---- |---- |
| 1 |  2  |  3  |   M[2,3]  | 0 | 0<2 | 0 | 0<3 |  1  |  M[0,0]=1  |  1  |  -  |
| 2 |  2  |  3  |   M[2,3]  | 0 | 0<2 | 1 | 1<3 |  2  |  M[0,1]=2  |  2  |  -  |
| 3 |  2  |  3  |   M[2,3]  | 0 | 0<2 | 2 | 2<3 |  3  |  M[0,2]=3  |  3  |  -  |
| 4 |  2  |  3  |   M[2,3]  | 0 | 0<2 | 3 | 3<3 |  -  |      -     |  -  |  1  |
| 5 |  2  |  3  |   M[2,3]  | 1 | 1<2 | 0 | 0<3 |  9  |  M[1,0]=9  |  1  |  -  |
| 6 |  2  |  3  |   M[2,3]  | 1 | 1<2 | 1 | 1<3 |  7  |  M[1,1]=7  |  2  |  -  |

### CÓDIGO EN JAVA
![11_DFD_CODE1](https://user-images.githubusercontent.com/113320901/205471795-b83c59c2-d05b-42e6-bc5e-8e1826c2b097.png)

![11_DFD_CODE2](https://user-images.githubusercontent.com/113320901/205471801-583d4785-bd5f-40ce-9bf2-bfcd8e1af418.png)

![11_DFD_CODE3](https://user-images.githubusercontent.com/113320901/205471808-a96da889-40ea-4ec5-8375-3afe260c122b.png)

![11_DFD_CODE_RUN](https://user-images.githubusercontent.com/113320901/205471825-c4038cad-bec9-4cb7-a574-e5c996173374.png)
