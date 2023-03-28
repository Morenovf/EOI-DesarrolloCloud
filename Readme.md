# Ejercicios de clase Algoritmos

Proceso:

**Paso 1**: Definir el problema

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Paso 3**: Escribir el pseudocódigo.

## 1. **Calcular la letra del DNI Español**

**Paso 1**: Definir el problema:

**¿Cómo se calcula la letra del DNI?**

El número del DNI **debe tener 8 dígitos**. Para calcular la letra del Documento Nacional de Identidad (DNI) español, se utiliza un algoritmo que se basa en el número de identificación. El procedimiento es el siguiente:

1. Dividir el número de identificación entre 23.
2. Tomar el resto de la división anterior.
3. Consultar una tabla que asocia cada resto con una letra. La tabla es la siguiente:
    
    
    | Resto | Letra |
    | --- | --- |
    | 0 | T |
    | 1 | R |
    | 2 | W |
    | 3 | A |
    | 4 | G |
    | 5 | M |
    | 6 | Y |
    | 7 | F |
    | 8 | P |
    | 9 | D |
    | 10 | X |
    | 11 | B |
    | 12 | N |
    | 13 | J |
    | 14 | Z |
    | 15 | S |
    | 16 | Q |
    | 17 | V |
    | 18 | H |
    | 19 | L |
    | 20 | C |
    | 21 | K |
    | 22 | E |

**Paso 2**: Ingresar la entrada, el proceso y la salida.

```markdown
Algoritmo CalculoDNI
	# Entrada
Definir las variables:
1. **DNI**
	- Pedir a usuario español ingresar su número de identificación, sin la letra.
2. **TablaLetrasDNI**
	- Tabla que asocia cada resto con una letra. 
3. r**esultadoResto
	-** Es el resto de la división del número de DNI entre 23.
	# Proceso
1. Verificar que el número de identificación introducido sea igual a 8 dígitos y que no haya caracteres.
	+ Si es erronea, asigne a la variable **resultado** "El número de DNI introducido no es válido"
2. Convertir **DNI** a valor entero.
3. Dividir **DNI** entre 23 y tomar el resto de la división anterior asociandolo a la variable **resultadoResto**.
3. Consultar **TablaLetrasDNI** y asociar **resultadoResto** con la letra que le corresponde.
	# Salida
- Si número de identificación es igual a 8 dígitos:
	- La salida mostrará el DNI junto al caracter
- Si número de identificación no es igual a 8 dígitos, hay caracteres intercalados o no hay números::
	- Imprimir en pantalla: "DNI no válido"	
Fin Algoritmo
```

**Paso 3**: Escribir el pseudocódigo.

Ahora en pseudocódigo:

```markdown
Algoritmo CalculoDNI
	# Entrada
	DNI<-leer
	tablaLetrasDNI<-"TRWAGMYFPDXBNJZSQVHLCKE"
	tablaLetrasDNI[0]<-T
	tablaLetrasDNI[1]<-R
	tablaLetrasDNI[2]<-W
	tablaLetrasDNI[3]<-A
	tablaLetrasDNI[4]<-G
	tablaLetrasDNI[5]<-M
	tablaLetrasDNI[6]<-Y
	tablaLetrasDNI[7]<-F
	tablaLetrasDNI[8]<-P
	tablaLetrasDNI[9]<-D
	tablaLetrasDNI[10]<-X
	tablaLetrasDNI[11]<-B
	tablaLetrasDNI[12]<-N
	tablaLetrasDNI[13]<-J
	tablaLetrasDNI[14]<-Z
	tablaLetrasDNI[15]<-S
	tablaLetrasDNI[16]<-Q
	tablaLetrasDNI[17]<-V
	tablaLetrasDNI[18]<-H
	tablaLetrasDNI[19]<-L
	tablaLetrasDNI[20]<-C
	tablaLetrasDNI[21]<-K
	tablaLetrasDNI[22]<-E
	numeroFila1<-0
	letraFila1z<-T
	resultado<-""
	# Proceso
	si DNI es valido Entonces #
			resultadoResto<-DNI mod 23 #mod es el resto de dividir
			#resultado<-recuperarLetra a partir de tablaLetrasDNI y resultadoResto
			#Para i<-0 Hasta 22 Con Paso 1 Hacer
			#  Si resultadoResto Igual i Entonces
			#    resultado = tablaLetrasDNI[i]
			#    i<-23 #break
			#  Finsi
			#Fin Para
			resultado<-tablaLetrasDNI[resultadoResto]
	Sino
			resultado<-"DNI inválido"
	Fin si
	# Salida
	Escribir resultado
Fin Algoritmo
```

## 2. **Calcular el salario de un empleado**

**Paso 1:** Definir el problema.

El salario en España se calcula a partir del salario bruto anual, que incluye todas las percepciones económicas que recibe un trabajador durante el año, incluyendo salario base, pagas extras, complementos y otros conceptos retributivos.

A partir del salario bruto se deducen las cotizaciones a la Seguridad Social y el impuesto sobre la Renta de las Personas Físicas (IRPF), que varían en función del nivel salarial y la situación personal del trabajador.

El salario neto anual se obtiene restando al salario bruto anual las cotizaciones y el IRPF correspondiente. El resultado final es el salario que percibe el trabajador después de impuestos y cotizaciones.

**Paso 2:** Poner la entrada, el proceso y la salida.

Entrada: 

- `salarioBase`,
- `pagasExtras`,
- `complementos`,
- `otrosConceptosRetributivos`,
- `IRPF`,
- `seguridadSocial`.

Proceso:

- Sumar `salarioBase`, `pagasExtras`, `complementos`, `otrosConceptosRetributivos` y lo asigno a `salarioBruto`.
- Sumar `IRPF`, `seguridadSocial` y lo asigno a deducciones.
- `salarioNeto` asigna `salarioBruto` - `deducciones`.

Salida:

- Escribir(`salarioBruto`,`salarioNeto`)

**Paso 3:** Escribir el pseudocódigo

```markdown
Algoritmo CalculoSalario
	# Entrada
		salarioBase <- leer()
		pagasExtras <- leer()
		complementos <- leer()
		otrosConceptosRetributivos <- leer()
		IRPF <- leer()
		Seguridad Social <- leer()
	# Proceso
		salarioBruto <- salarioBase+pagasExtras+complementos+otrosConceptosRetributivos
		deducciones <- IRPF+Seguridad Social
	# Salida
		Escribir salario
Fin Algoritmo
```

## 3. **Determinar la ruta para llegar a una ciudad por avión**

**Paso 1**: Definir el problema

El problema que se describe en el enunciado es el siguiente:

- Se necesita determinar la ruta óptima para llegar a una ciudad por avión.

Para resolver este problema, se pueden seguir los siguientes pasos:

- El usuario debe introducir información necesaria para determinar la ruta óptima, como la ciudad de **origen** y la de **destino**.
- La información sobre las rutas por avión podemos plantear que la podríamos obtener mediante la ******************supuesta función inventada `Obtener_Rutas_Por_Avión()`**, que accederá a bases de datos de agencias de viajes en línea, sitios web de aerolíneas y darnos la información que requerimos. **`OBTENER_CIUDADES_DE_RUTA(rutaOptima)`** se usará para obtener la lista de ciudades que conforman la ruta óptima.
- Finalmente, se devuelve la lista de ciudades como salida.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada**:

Solicitar al usuario:

- Ciudad de origen `**ciudadOrigen**`.
- Ciudad de destino `**ciudadDestino**`.

**Proceso**:

- Usar una función para obtener rutas: **`Obtener_Rutas_Por_Avión()`**  teniendo en cuenta la información introducida por el usuario y recorreremos la lista para encontrar la ruta que encaje con nuestros requisitos.
- Si no se encuentra una ruta óptima mostraremos un mensaje de error. Si no, se utiliza la función **`OBTENER_CIUDADES_DE_RUTA(rutaOptima)`**  para mostrar la lista de ciudades que formarían la ruta óptima definida.

**Salida**:

- No hay ruta óptima → "No existen rutas para llegar de la ciudad de origen a la ciudad destino descritas."
- Sí hay ruta óptima → `ruta` muestra la lista de ciudades que formarían la ruta óptima.

**Paso 3**: Escribir el pseudocódigo.

```python
ALGORITMO determinarRutaPorAvion
	# ENTRADA: 
		ciudadOrigen<-leer() #Usuario introduce cadena de texto que indica la ciudad de origen.
    ciudadDestino<-leer() #(...) que indica la ciudad de destino.
		rutaOptima<-"" #Inicializar la variable "rutaOptima".
		ruta<-"" #Lo mismo que la anterior
	# PROCESO:
    rutas = Obtener_Rutas_Por_Avión() #Nos inventamos una función que obtenga todas las rutas disponibles por avión.
    
    Para i Desde 0 Hasta Longitud(rutas) Hacer #Recorremos la lista de rutas por avión.
        Si rutas[i].origen = ciudadOrigen Y rutas[i].destino = ciudadDestino Entonces #Buscamos que se cumplan las dos condiciones.
            rutaOptima = rutas[i] #La ruta actual es la ruta óptima.
            Salir #Salir de la iteración. Ya encontramos la ruta óptima.
        Fin Si
    Fin Para

    Si rutaOptima = "" Entonces #Si no se encontró rutaOptima y se conserva el valor inicial...
        Escribir "No existen rutas para llegar de la ciudad de origen a la ciudad destino descritas." 
    Sino
        ruta = Obtener_Ciudades_De_Ruta(rutaOptima) #Nos inventamos una función que obtenga las ciudades que conforman la ruta óptima.
	# SALIDA: 
		Escribir ruta #Escribir la lista de ciudades que conforman la ruta para llegar a la ciudad destino.
```

## 4. **Calcula el área y perímetro de un círculo dado su radio.**

**Paso 1**: Definir el problema

Para resolver el problema de calcular el área y perímetro de un círculo dado su radio, se pueden utilizar las siguientes fórmulas matemáticas:

- El perímetro o circunferencia del círculo se calcula como: P = 2 * pi * r, donde "pi" es una constante que representa la relación entre la circunferencia y el diámetro de cualquier círculo (aproximadamente igual a 3.14159), y "r" es el radio del círculo.
- El área del círculo se calcula como: A = pi * r^2, donde "r" es el radio del círculo.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada**

Solicitar al usuario:

- Valor del radio del círculo `radioCírculo` [mm,cm.dm,m]

Definir constante PI con valor “3.14159265” y asignarla a la variable `constantePi`

**Proceso**

- Calcular el perímetro del círculo como 2 * PI * radio y asignarlo a `perímetroCírculo`
- Calcular el área del círculo como PI * radio * radio `áreaCírculo`

**Salida**

- Mostrar el valor del perímetro del círculo
- Mostrar el valor del área del círculo

**Paso 3**: Escribir el pseudocódigo.

```markdown
Algoritmo cálculoÁreayPerímetroCírculo

# ENTRADA:
	radioCírculo <- leer()
	constantePi <- "3.14159265"
# PROCESO:
	perímetroCírculo <- 2*constantePi*radioCírculo
	áreaCírculo <- constantePi*radioCírculo*radioCírculo
# SALIDA:
	Escribir perímetroCírculo
	Escribir áreaCírculo
```

## 5. **Dada una lista de números enteros, determina cuál es el mayor y cuál es el menor.**

**Paso 1**: Definir el problema

El problema consiste en encontrar el número más grande y el número más pequeño de una lista de números enteros. La solución debe ser un algoritmo que recorra la lista de números y compare cada uno de ellos con las variables "mayor" y "menor" para determinar cuál es el número más grande y cuál es el número más pequeño.

> La lista deberá obligar al usuario a insertar números enteros, si no no podrá continuar con el algoritmo.
> 

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada**

Solicitar al usuario:

- Lista de números enteros `listaNumeros`

Inicializar variables "mayor" y "menor" con el primer número de la lista.

- `numMayor`
- `numMenor`

**Proceso**

Recorreremos la lista de números enteros para determinar cual es el mayor y el menor comparándolo con el primer número de la lista.

1. Para cada número "n" en la lista, hacer lo siguiente:
a. Si "n" es mayor que "mayor", actualizar "mayor" con el valor de "n".
b. Si "n" es menor que "menor", actualizar "menor" con el valor de "n".

**Salida**

- Devolver el valor de "mayor" y "menor".

**Paso 3**: Escribir el pseudocódigo.

```markdown
Algoritmo encontrarNumeroMayoryMenor

# ENTRADA:
	listaNumeros <- leer[]
	numMayor = lista[0]
	numMenor = lista[0]
# PROCESO:
	Si n = Numero Entero 
		Para n en lista :
			Si n > numMayor Entonces
				numMayor = n
			Si n < numMenor Entonces
				numMenor = n
	Si no 
		Escribir "Por favor, escribe  una lista donde únicamente haya numeros enteros."
# SALIDA:
	Escribir numMayor, numMenor
```

## 6. **Crea un algoritmo que convierta grados Celsius a Fahrenheit.**

**Paso 1**: Definir el problema

Nos piden desarrollar un algoritmo que permita convertir una temperatura en grados Celsius a su equivalente en grados Fahrenheit.  Se resuelve utilizando una fórmula de conversión `ºF=(ºC*1.8) + 32`.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada**

- Leer la temperatura en grados Celsius (ºC) `temperaturaCelsius`

**Proceso**

- Convertir la temperatura de Celsius a Fahrenheit usando la fórmula adecuada.

**Salida**

- Mostrar el resultado de la conversión en grados Fahrenheit (ºF) `gradosFahrenheit`

**Paso 3**: Escribir el pseudocódigo.

```markdown
Algoritmo convertirGradosCelsius-Fahrenheit

# ENTRADA:
	temperaturaCelsius <- leer()
# PROCESO:
	Si temperaturaCelsius = Numero Entero 
		gradosFahrenheit = (temperaturaCelsius*1.8) + 32
	Si no 
		Escribir "Por favor, escribe un valor numérico."
# SALIDA:
	Escribir gradosFahrenheit
```

## 7. **Dado un número entero, crea un algoritmo que determine si es par o impar.**

**Paso 1**: Definir el problema

Para determinar si un número es par o impar debemos calcular su módulo 2 (el resto de la división del número entre 2). Si el resto es igual a cero, el número es par. Si no, es impar.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada**

- Leer`numeroEntero`

**Proceso**

- Calcular módulo de 2 de `numeroEntero`
- Determinar si es impar o par.

**Salida**

- Escribir si el número es par o impar.
- Si el número no es un valor numérico aceptado, mostrar mensaje de error.

**Paso 3**: Escribir el pseudocódigo.

```markdown
Algoritmo ImparoPar

# ENTRADA:
	numeroEntero<- leer()
	paroImpar <- ""
# PROCESO:
	Si numeroEntero % (MOD) 2 = 0 Entonces
		paroImpar <- "El numero es par"
	Sino
		paroImpar <- "El numero es impar"
# SALIDA:
	Escribir paroImpar
```

## 8. **Crea un algoritmo que determine si un año es bisiesto o no.**

**Paso 1**: Definir el problema

Un año bisiesto es aquel año que tiene **366 días** en lugar de 365, en el que febrero tiene 29 días en lugar de 28. Se repite **cada cuatro años**, excepto cuando el año acaba en dos ceros.

Condiciones para determinar cuando un año es bisiesto:

- **Debe** se divisible entre 4
- **No debe** ser divisible entre 100.
    
    Si lo es, el año es bisiesto si:
    
    - **Es divisible** entre 400. Si no lo es, ****************************no es bisiesto****************************.

Ejemplo: 

1. El año 2000 es divisible entre 4 y da resto 0, pero también da resto cero si lo dividimos entre 100, con lo cual ****************************no es bisiesto****************************.
2. Por el contrario, el año 2012 es divisible entre 4 y da resto 0 pero **************no da resto cero************** cuando lo dividimos entre 100 lo cual ****************************es bisiesto****************************.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada**

- Leer `año`
- Inicializar variable texto `resultado`

**Proceso**

Pueden ocurrir dos sucesos:

1. Que el año sea divisible entre 4 y **no lo sea** entre 100: **AÑO BISIESTO**

![Untitled](imagenes//Untitled%207.png)

1. Que el año sea divisible entre 4, ******************************también lo sea entre 100****************************** **********************y entre 400: AÑO BISIESTO**
    
    ![Untitled](imagenes//Untitled%208.png)
    

Con lo cual habrá que establecer esas 3 condiciones en el algoritmo, una dentro de otra.

**Salida**

- Escribir `resultado` tras comprobar en el proceso si el año es bisiesto o no según las condiciones establecidas.

**Paso 3**: Escribir el pseudocódigo.

```markdown
Algoritmo añoBisiesto

# ENTRADA:
	año <- leer()
	resultado <- ""
# PROCESO:
	#Comprobar si el año es divisible entre 4 y NO es divisible entre 100:
	Si año % (MOD) 4 = 0 Entonces
		Si año % (MOD) 100 = 0 Entonces
			Si año % (MOD) 400 = 0 Entonces
				resultado <- "El año es bisiesto"
			Sino 
				resultado <- "El año no es bisiesto"
		Sino
			resultado <- "El año es bisiesto"
	Sino
		resultado "El año no es bisiesto"		
# SALIDA:
	Escribir resultado
```

## 9. **Crea un algoritmo que determine si una cadena de texto es un palíndromo o no.**

**Paso 1**: Definir el problema

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada:** Pedir cadena texto al usuario

**Proceso:**

- El algoritmo primero pide al usuario que ingrese una cadena de texto y luego inicializa las variables necesarias.
- Luego utiliza un ciclo "Para" para verificar si la cadena es un palíndromo o no. Dentro del ciclo, se compara cada letra de la cadena con su correspondiente al final de la cadena, para determinar si la cadena es un palíndromo.
- Si se encuentra una letra diferente, la variable "palindromo" se establece en Falso y se sale del ciclo.

**Salida:** Mostrar el resultado al usuario indicando si la cadena es o no un palíndromo.

**Paso 3**: Escribir el pseudocódigo.

```python
Algoritmo Palindromo
	# ENTRADA:
  cadena<-leer()
  longitud <- Longitud(cadena)
  palindromo <- Verdadero
	# PROCESO:
	  Escribir("Ingrese cadena de texto:")
	  Para i <- 1 Hasta Longitud/2 Hacer #cadena es palindromo?
	    Si Subcadena(cadena, i, 1) <> Subcadena(cadena, longitud - i + 1, 1) Entonces
	      palindromo <- Falso
	      Salir
	    Fin Si
	  Fin Para
	  Si palindromo Entonces
	    Escribir("La cadena es un palíndromo.")
	  Sino
	    Escribir("La cadena no es un palíndromo.")
	  Fin Si
	# SALIDA:
```

## 10. **Dada una lista de nombres, crea un algoritmo que ordene la lista alfabéticamente.**

**Paso 1**: Definir el problema:

Lista de nombres separados por comas. Hay que ordenar alfabeticamente los nombres

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada**  Definición usuario lista variable**`nombres`**

**Proceso** 

- Dos ciclos anidados “Para” u ordenamiento de burbuja.
    - El primero se encarga de recorrer la lista ed nombres (primer indice comienza en indice 1)
    - El segundo recorre el resto de la lista a partir de la posición actual del primer ciclo  (segundo indice comienza en indice 2)
        
        ![Untitled](imagenes/Untitled%209.png)
        

**Salida:**  Lista ordenada alfabeticamente

**Paso 3**: Escribir el pseudocódigo.

```python
Algoritmo OrdenarNombres
	# ENTRADA:
  nombres <-leer[]
	# PROCESO:
  Para i <- 1 Hasta Longitud(nombres)- 1 Hacer #desde el primer indice de la lista (1) hasta el penultio indice de la lista (Longitud(nombres)-1).
    Para j <- i + 1 Hasta Longitud(nombres) Hacer #comprobamos si el nombre en el índice "i" de la lista es mayor que el nombre en el índice "j" de la lista.
      Si nombres[i] > nombres[j] Entonces
        temporal <- nombres[i] #si no estan en orden alfabetico se intercambian
        nombres[i] <- nombres[j]
        nombres[j] <- temporal
      Fin Si
    Fin Para
  Fin Para
  Escribir("La lista de nombres ordenada alfabéticamente es:")
  Para i <- 1 Hasta Longitud(nombres) Hacer
    Escribir(nombres[i])
  Fin Para
	# SALIDA:
```

## 14. Dada una lista de números enteros, crea un algoritmo que calcule la suma de todos los números
pares de la lista.

**Paso 1**: Definir el problema

El problema consiste en tomar una lista de números enteros y sumar únicamente los números pares en ella, es decir, cualquier número que sea **divisible entre 2 (resto al dividir entre 2 sea 0).**

Para resolver el problema se necesitaría **iterar sobre la lista y comprobar si cada número es par o no**. En el caso de que lo sea, este número debe ser **añadido a la suma total**. Al final de la iteración se deberá devolver la suma total de los números pares en la lista.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada:** Lista de los números enteros y almacenarla en la variable **`listaNumerosEnteros`.**

**Proceso:** 

- Inicializar variable `suma` en cero.
- Por cada número en la lista:
    - Si el número es par (resto dividido entre 2 es 0):
        - Sumar el número a la variable `suma`.

**Salida:** Devolver la suma total de todos los números pares en la lista almacenando este dato en la variable `resultadoSumaPares`.

**Paso 3**: Escribir el pseudocódigo.

```markdown
Algoritmo sumaNumerosPares
	# ENTRADA:
		listaNumerosEnteros<-leer[] #por ejemplo [1,2,3,4,5,6,7,8,9]
		suma<-0 #Inicializar la variable "suma" en cero.
	# PROCESO:
		Para i Desde 0 Hasta Longitud(listaNumerosEnteros) Hacer #recorremos la lista de numeros.
			Si (listaNumerosEnteros[i] % (MOD) 2 = 0) Entonces #Si número es par...
				suma = suma + listaNumerosEnteros[i] #Sumar el número par a la variable suma.
			Fin Si
		Fin Para
	# SALIDA:
		Escribir "La suma de los números pares es" + suma
```

## 15. Crea un algoritmo que determine si un número es positivo, negativo o cero.

**Paso 1**: Definir el problema

El problema consiste en distinguir cuando un número es mayor, menor o igual que cero.

Para resolver el problema se necesita comprobar si `n es <, > o igual a 0`.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada:** Número introducido por el usuario asignado a variable`numero`

**Proceso:**

Respecto al número introducido:

1. Si el número introducido es un valor numérico:
    - En el caso que sea **menor** (<) la salida determinará que es **negativo**.
    - Si es **mayor** (>) la salida mostrará que es **positivo**.
    - Si el número es **igual** a 0, la salida mostrará que es **igual a cero**.
2. Si el número introducido no es un valor numérico:
    - Devolver salida “Error. Introduzca únicamente valores numéricos.”

**Salida:** Devolver qué condición cumple el número introducido.

**Paso 3**: Escribir el pseudocódigo.

```python
Algoritmo determinarSignoNumero
	# ENTRADA:
		numero<-leer()
	# PROCESO:
		Si no Es_Numerico(numero) Entonces:
			signo = “Error. Introduzca únicamente valores numéricos."
		Sino Si numero > 0 Entonces
			signo = "El número es positivo."
		Sino Si numero < 0 Entonces
			signo = "El número es negativo."
		Sino
			signo = "El número es igual a cero."
		Fin Si
	# SALIDA:
		Escribir signo
```

## 16. Dada una lista de números enteros, crea un algoritmo que calcule la media de la lista.

**Paso 1**: Definir el problema

El problema consiste en, dada una lista de números enteros, calcular la media de los números de la misma.

Para resolver el problema se necesita realizar la **suma de todos los números y dividir el resultado entre la cantidad de valores que tengamos en la lista**.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada:** Lista de los números enteros y almacenarla en la variable **`listaNumeros`.**

**Proceso:**

- Inicializar variable `suma` en cero.
- Por cada número en la lista:
    - Sumar cada número en la lista a la variable `suma`.
- Calcular la media de los números dividiendo la variable `suma` entre la longitud de `listaNumeros`.

**Salida:** Devolver la media numerica de los valores de `listaNumeros`.

**Paso 3**: Escribir el pseudocódigo.

```python
Algoritmo calcularMediaLista
	# ENTRADA: 
		listaNumeros<-leer[]
		suma<-0
	# PROCESO:
		Para i desde 0 hasta Longitud(listaNumeros) Hacer #recorrer cada valor de la lista
			suma = suma + listaNumeros #Sumar cada numero en la lista a la variable "suma".
		Fin Para
		media = suma / Longitud(listaNumeros) #Para hallar media dividimos la suma de valores entre la cantidad de numeros en lista.
	# SALIDA:
		Escribir "La media de los números de la lista es " + media
```

## 17. Crea un algoritmo que genere un número aleatorio entre 1 y 100, y le pida al usuario adivinarlo. El algoritmo deberá indicar si el número introducido es mayor o menor que el número aleatorio, hasta que el usuario adivine el número correcto.

**Paso 1**: Definir el problema

El problema consiste en, dado un rango de números enteros entre 1 y 100, crear un algoritmo que genere un número aleatorio y le pida al usuario adivinarlo. El algoritmo debe indicar si el número introducido por el usuario es mayor o menor que el número aleatorio, hasta que el usuario adivine el número correcto.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada: `respuesta`** del usuario

**Proceso:**

- Generar numero aleatorio entre 1 y 100.
- Bucle *While*: Mientras la respuesta del usuario no sea igual al número aleatorio, indicarle si el valor es mayor o menor al numero aleatorio, sino felicitarle por adivinar el número.

**Salida:**

- El número introducido es:
    - mayor que el numero aleatorio
    - menor que el numero aleatorio
    - Igual que el numero aleatorio. ¡Muy bien!

**Paso 3**: Escribir el pseudocódigo.

```python
Algoritmo adivinarNumeroAleatorio
	# ENTRADA:
		respuesta<-0 #inicializar variable "respuesta"
	# PROCESO:
		numeroAleatorio <- GenerarNumeroAleatorio(1,100) #Generar número aleatorio entre 1 y 100.
		Mientras respuesta != (no igual a) numeroAleatorio Hacer
			Escribir "Introduce un número entre 1 y 100:" #Pedir al usuario que introduzca un número
			numeroUsuario<-leer() #tiene que ser un numero entero.
			Si numeroUsuario > numeroAleatorio Entonces
				Escribir "El número introducido es mayor que el número aleatorio."
			Si No Si numeroUsuario < numeroAleatorio Entonces
				Escribir "El número introducido es menor que el número aleatorio."
			Si No
				Escribir "¡Muy bien! Adivinaste el número aleatorio."
			Fin Si		
		Fin Mientras
	# SALIDA:
```

## 18. Crea un algoritmo que determine si una cadena de texto es un anagrama de otra cadena de texto.

**Paso 1**: Definir el problema

PROBLEMA: Determinar si una cadena de texto es un anagrama de otra cadena de texto.

Anagrama: Procedimiento que consiste en crear una palabra a partir de la reordenación de las letras de otra palabra.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada:** Leer**`cadena1`, `cadena2` .**

**Proceso:`caracteres1`, `caracteres2`**

**Salida:**

- Son anagramas.
- No lo son.

**Paso 3**: Escribir el pseudocódigo.

```python
Algoritmo anagramaCadenasTexto

	# ENTRADA:
		cadena1<-leer()
		cadena2<-leer()
	# PROCESO:
		Si Longitud(cadena1) != (es distinto a) Longitud(cadena2) Entonces
		  Escribir "Las cadenas de texto no son anagramas"
		Sino
	    caracteres1<-Vector(27,0) #abecedario español son 27 palabras
			caracteres2<-Vector(27,0) #inicializado con ceros para indicar que inicialmente no se encuentra letra en cadenas de texto.
			
			Para i<-1 Hasta Longitud(cadena1) Hace
        letra<-Subcadena(cadena1, i, 1)
        posición <-PosiciónEnAlfabeto(letra)
        caracteres1[posición]<-caracteres1[posición] + 1
	    Fin Para

	    Para i<- 1 Hasta Longitud(cadena2) Hacer
        letra ← Subcadena(cadena2, i, 1) #obtener un substring de la cadena de texto "cadena2".
        posición ← PosiciónEnAlfabeto(letra) #función hipotética para obtener la posición de una letra en el alfabeto español.
        caracteres2[posición] ← caracteres2[posición] + 1
	    Fin Para
	    Si caracteres1 = caracteres2 Entonces
        Imprimir "Son anagramas"
	    Sino
        Imprimir "No son anagramas"
	    Fin Si
		Fin Si
	# SALIDA:

```

## 19. Dada una lista de números enteros, crea un algoritmo que elimine los números duplicados de la
lista.

**Paso 1**: Definir el problema

El problema consiste en escribir un programa que a partir de una lista de números enteros como entrada por el usuario y que elimine todos los elementos de la lista que aparezcan más de una vez. Cada número entero aparecerá de esta forma únicamente una vez en la lista de salida a partir de la variable `**listaNumeros**`. 

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada:** Lista de números enteros definida por el usuario almacenada en la variable **`listaNumeros`.**

**Proceso:**

- Tras leer la lista de número enteros `**listaNumeros`** introducida por el usuario, se calcula la longitud de la lista y se almacena en la variable`**longitudLista`** para ****poder recorrerla en un **bucle anidado** (aquel que está dentro de otro).
- Se inicia un bucle “para” anidado que recorra cada número en la lista (bucle exterior) y lo compara con los números que le siguen (bucle interior).
    - Si el número actual `**listaNumeros[x]`** es igual a alguno de los siguientes números en la lista **************************`listaNumeros[y]`** significa que hay un número duplicado.
    - Si hay un número duplicado se elimina el número de la lista ************`listaNumeros[y]`** usando la función “Eliminar” se reduce la longitud de la lista (`longitudLista = longitudLista - 1`), decrementando la variable del bucle interno (`y = y - 1`) para no omitir ningún número.
    
    <aside>
    👉🏻 Esto es necesario porque, después de eliminar un elemento de la lista, el siguiente elemento de la lista se mueve a una posición anterior. SI NO se decrementa el índice del bucle interno se podría omitir la comparación de este elemento.
    
    </aside>
    
    - Se itera por la la lista hasta que se revisen todos los números de la lista.

**Salida:** Se muestra la lista sin números duplicados **`listaNumeros`**.

**Paso 3**: Escribir el pseudocódigo.

```python
Algoritmo eliminarNumerosDuplicadosLista

	# ENTRADA:
		listaNumeros<-leer[]
	# PROCESO:
		longitudLista = Longitud(listaNumeros) 
		#Bucle anidado para comparar cada numero en lista con los numeros que siguen.
		Para x Desde 1 Hasta longitudLista Hacer #Recorre cada numero en la lista.
	    Para y Desde x+1 Hasta longitudLista Hacer #Comparar con siguientes numeros.
        Si listaNumeros[x] = listaNumeros[y] Entonces # Hay duplicado?
	        Eliminar listaNumeros[y] #Se elimina el numero duplicado.
          longitudLista = longitudLista - 1 
          y = y - 1
        Fin Si
	    Fin Para
		Fin Para
	# SALIDA:
		Escribir listaNumeros

```

## 20. Crea un algoritmo que determine si un número es capicúa o no.

**Paso 1**: Definir el problema

El problema consiste en determinar una forma de saber si un numero introducido por el usuario **es igual leído de izquierda a derecha que de derecha a izquierda**.

**Paso 2**: Ingresar la entrada, el proceso y la salida.

**Entrada: `numero`, `numeroInvertido`, `numeroACadenaTexto`, `resultado`.**

**Proceso:** 

- Convertir numero a string.
- Invertir cadena de texto
- Convertir nuevamente a valor numerico
- Comprobar que el numero inicial coincide con el número invertido

**Salida:**

- El número es capicua
- El número no es capicua

**Paso 3**: Escribir el pseudocódigo.

```python
Algoritmo numeroEsCapicuaONo
	# ENTRADA: 
		numero<-Leer() #Tiene que ser numero entero
		numeroInvertido<-"" 
		numeroACadenaTexto<-""
		resultado<-""
	# PROCESO:
	Escribir "Por favor, introduce un número entero:"
	numeroACadenaTexto <- ConvertirACadenaTexto(numero) #convertir a cadena de texto	
	Para x Desde Longitud(numeroACadenaTexto) Hasta 1 Hacer
		numeroInvertido<-numeroInvertido + Subcadena(numeroACadenaTextostring,x,1)
	Fin Para
	numeroInvertido<-ConvertirANumeroInteger(numeroInvertido) #Convertir el número invertido en entero
	Si numero = numeroInvertido Entonces 	~~#Comparar número original con el número invertido..~~
		resultado<-Escribir "El número es capicúa."
	SiNo
		rsultado<-Escribir "El número no es capicúa."
	Fin Si
	# SALIDA:
		Escribir resultado
```