### Función Login
- **Descripción**: Recibe un nombre de usuario y una contraseña, y devuelve un valor lógico: verdadero si se ha introducido el nombre y la contraseña adecuadas. Además, incrementa el número de intentos que recibe como parámetro de entrada/salida.
- **Parámetros de Entrada**: nombre y contraseña.
- **Parámetros de Entrada y Salida**: intentos.
- **Dato Devuelto**: Valor lógico indicando si ha hecho login.

```markdown
Funcion login <- esLogin(nombre, pass, intentos por referencia)
    Definir eslogin Como Logico;
    Si nombre = "usuario1" Y pass = "asdasd" Entonces
        eslogin <- Verdadero;
    SiNo
        eslogin <- Falso;
        intentos <- intentos + 1;
    FinSi
FinFuncion
```

### Descripción del Proceso de Login
- **Objetivo**: Crear una subproceso llamada "Login", que recibe un nombre de usuario y una contraseña y devuelve Verdadero si el nombre de usuario es "usuario1" y la contraseña es "asdasd". Además, recibe el número de intentos que se ha intentado hacer login y, si no se ha podido hacer login, incrementa este valor.
- **Programa Principal**: Se pide un nombre de usuario y una contraseña y se intenta hacer login, teniendo solo tres oportunidades para intentarlo.

```markdown
Proceso EntrarEnElSistema
    Definir usuario, clave Caracter;
    Definir cuantasveces entero;
    Definir entrar Logico;
    cuantasveces <- 0;

    Repetir
        Escribir "Usuario:";
        Leer usuario;
        Escribir "Password:";
        Leer clave;
        entrar <- esLogin(usuario, clave, cuantasveces);
        Si no entrar Entonces
            Escribir "Error. Nombre de usuario o contraseña incorrecta.";
        FinSi
    Hasta Que entrar o cuantasveces = 3;

    Si entrar Entonces
        Escribir "Bienvenidos al sistema";
    SiNo
        Escribir "No has entrado en el sistema";
    FinSi
FinProceso
```
