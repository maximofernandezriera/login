### 1. Pseudocódigo para la Conversión de un Número Decimal a Binario
```markdown
#### Método decimalBinari (argumento: entero nombre)
- Mientras nombre sea diferente de 0
  - Imprimir en consola el residuo de nombre dividido por 2
  - Asignar a nombre el valor de nombre dividido por 2
#### Fin del Método
```

### 2. Pseudocódigo para la Conversión de un Número Binario a Decimal
```markdown
#### Método binariDecimal (argumento: largo binari)
- Declarar decimal como decimal y asignarle el valor 0
- Para i = 0 mientras binari sea diferente de 0
  - Declarar digit como entero y asignarle el residuo de binari dividido por 10
  - Incrementar decimal por el producto de digit y 2 elevado a i
  - Asignar a binari el valor de binari dividido por 10
- Fin del bucle
- Imprimir en consola decimal
#### Fin del Método
```

### 3. Pseudocódigo para Verificar si un Número es Par
```markdown
#### Método esParell (argumento: entero n)
- Devolver verdadero si el residuo de n dividido por 2 es igual a 0
- De lo contrario, devolver falso
#### Fin del Método
```

### 4. Pseudocódigo para Calcular los Primeros Números Pares Hasta n
```markdown
#### Método primersNombresParells (argumento: entero n)
- Para i = 0 hasta i menor o igual a n
  - Si esParell(i) es verdadero
    - Imprimir en consola i
  - Fin del Si
- Fin del Para
#### Fin del Método
```

### 5. Pseudocódigo para Calcular el Volumen de un Cilindro
```markdown
#### Método volumCilindre (argumentos: decimal radi, decimal longitud)
- Devolver el valor de pi multiplicado por el cuadrado de radi y luego multiplicado por longitud
#### Fin del Método
```

### 6. Pseudocódigo para Calcular el Volumen de un Prisma Rectangular
```markdown
#### Método volumPrismaRectangular (argumentos: decimal c1, decimal c2, decimal c3)
- Devolver el producto de c1, c2 y c3
#### Fin del Método
```

### 7. Pseudocódigo para el Método Principal con Menú y Cálculos de Volumen
```markdown
#### Método main
- Imprimir en consola "Què hem de transportar? 1. Líquids 2. Sòlids"
- Leer opcio como entero
- Mientras opcio no sea igual a 1 y opcio no sea igual a 2
  - Imprimir en consola "No és una opció vàlida"
  - Imprimir en consola "Què hem de transportar? 1. Líquids 2. Sòlids"
  - Leer opcio nuevamente
- Fin del Mientras

- Declarar volum como decimal y asignarle 0
- Si opcio es igual a 1
  - Imprimir en consola "Què medeix el radi de la cisterna"
  - Leer radi como decimal
  - Imprimir en consola "Què medeix de llarg la cisterna"
  - Leer llarg como decimal
  - Asignar a volum el resultado de volumCilindre(radi, llarg)
- Sino Si opcio es igual a 2
  - Imprimir en consola "Què medeix el costat 1 del camió"
  - Leer c1 como decimal
  - Imprimir en consola "Què medeix el costat 2 del camió"
  - Leer c2 como decimal
  - Imprimir en consola "Què medeix el costat 3 del camió"
  - Leer c3 como decimal
  - Asignar a volum el resultado de volumPrismaRectangular(c1, c2, c3)
- Fin del Si

- Imprimir en consola "Quants metres cúbics hem de transportar?"
- Leer m3_a_transportar como decimal
- Imprimir en consola "El tràiler té " + volum + " centímetres cúbics"
- Asignar a capacitat el valor de volum dividido por 1,000,000
- Imprimir en consola "Hi caben " + capacitat + " metres cúbics"
- Asignar a viatges el valor entero de m3_a_transportar dividido por capacitat, incrementado en 1
- Imprimir en consola "Has de fer " + viatges + " viatges."
#### Fin del Método
```
#### Paquete codigo

- Importar utilidades Arrays y Scanner

#### Clase Main

##### Método main (argumentos: cadena de texto args)
- Crear objeto Scanner sc para leer desde consola
- Imprimir en consola "Longitud de la combinación secreta: "
- Leer longitud como entero
- Declarar combSecreta como tabla de enteros de tamaño longitud
- Declarar combJugador como tabla de enteros de tamaño longitud

- Llamar a generaCombinacion y pasar combSecreta
- Imprimir combSecreta
- Imprimir en consola "Escriba una combinación"
- Llamar a leeTabla y pasar combJugador

- Mientras combSecreta no sea igual a combJugador
  - Llamar a muestraPistas y pasar combSecreta y combJugador
  - Imprimir en consola "Escriba una combinación: "
  - Llamar a leeTabla y pasar combJugador
- Fin del Mientras

- Imprimir en consola "¡La cámara está abierta!"

##### Método generaCombinacion (argumento: tabla de enteros t)
- Declarar constante MAX con valor 5
- Para cada elemento en t
  - Asignar a t[i] un valor entero aleatorio entre 1 y MAX
- Fin del Para

##### Método leeTabla (argumento: tabla de enteros t)
- Crear objeto Scanner sc para leer desde consola
- Para cada elemento en t
  - Leer t[i] como entero
- Fin del Para

##### Método muestraPistas (argumentos: tabla de enteros secret, tabla de enteros jug)
- Imprimir en consola "Pistas:"
- Para cada elemento en jug
  - Imprimir jug[i]
  - Si secret[i] es mayor que jug[i]
    - Imprimir " mayor"
  - Sino Si secret[i] es menor que jug[i]
    - Imprimir " menor"
  - Sino
    - Imprimir " igual"
- Fin del Para

#### Fin de la Clase Main
