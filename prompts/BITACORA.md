# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Tokens y ventana de contexto
| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. |34 |7 |
| The students program in Java. |29 |6 |
| desafortunadamente |18 |4 |

Paso 4: La IA supo responder porque tenia informacion. 
Paso 5: La IA interpreto que me referia a ella como una aplicacion y su tecnologia 

## Ejercicio 3: Temperatura

Al repetir el mismo prompt en 3 chats nuevos, obtuve los mismos 3 nombres
en los tres intentos. Esto sugiere que la herramienta usa una temperatura
baja por defecto, o que tiene activada una funcion de memoria entre chats.

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|-----------------|----------------------------|
| 0   | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 65.3%  | PrestaLibro, BiblioTec, BiblioTec, BiblioTec, LibroYa |
| 1   | 44.5%  | BiblioTec, PrestaLibro, BiblioTec, BiblioTec, BiblioTec |
| 1.8 | 32.2%  | LectoGo, NubeDeTinta, BiblioTec, BiblioTec, LibroYa |

## Ejercicio 4: Prompt vago vs estructurado

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|----------------------|
| Menciona el objetivo del sistema |SI |NO |
| Menciona a los usuarios principales |SI |SI |
| Tiene exactamente 3 funcionalidades |SI |SI |
| Esta en 3 parrafos |NO |SI |
| Lo usaria en un informe real |NO |SI |

## Ejercicio 5: Anatomia de un prompt

| Componente | Texto de mi prompt |
|------------|---------------------|
| Rol |Actua como desarrollador Java. |
| Instruccion |Crea un programa en Java para gestionar los productos de una tienda, usando una clase Producto con los atributos codigo, nombre, precio y stock. Explica primero la estructura de la clase y luego presenta el codigo Java. |
| Contexto |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.  |
| Ejemplo |(No especificado de forma explícita en el prompt) |
| Formato |Explica primero la estructura de la clase y luego presenta el codigo Java.  |

## Ejercicio 6: Del prompt basico al profesional

```text
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```


