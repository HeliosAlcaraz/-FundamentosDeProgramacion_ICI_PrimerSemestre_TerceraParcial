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
