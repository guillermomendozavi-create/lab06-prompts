# Tarea: Mi prompt profesional

## Funcionalidad elegida

CRUD (crear, listar, editar y eliminar) de productos para una tienda pequeña, ejecutado por consola en Java.

## Version 1: prompt basico

```text
Hazme un CRUD de productos en Java.
```

**Que cambie:** nada todavia, es el punto de partida.

**Por que:** es el primer prompt que se me ocurrio, sin pensar en el proceso.

**Que mejoro:** nada aun, sirve como linea base. La respuesta fue generica: la IA no sabia si el CRUD debia tener interfaz grafica o consola, que atributos debia tener el producto, ni donde guardar los datos. Invento sus propios supuestos.

## Version 2

```text
Actua como desarrollador Java. Crea un CRUD de productos para una tienda pequena, usando una clase Producto con los atributos codigo, nombre, precio y stock, y guardando los datos en una lista en memoria (ArrayList).
```

**Que cambie:** agregue el ROL (desarrollador Java) y el CONTEXTO (tienda pequena, los 4 atributos exactos de Producto, y que el almacenamiento sea una lista en memoria).

**Por que:** en la version 1 la IA invento atributos distintos a los que yo necesitaba y en un intento incluso propuso conectarse a una base de datos, algo que no pedi.

**Que mejoro:** la respuesta ya usa la clase Producto con exactamente los 4 atributos que necesito y guarda los datos en un ArrayList, sin agregar dependencias externas.

## Version 3: prompt final

```text
Actua como desarrollador Java. Crea un CRUD de productos para una tienda pequena, usando una clase Producto con los atributos codigo, nombre, precio y stock, y guardando los datos en una lista en memoria (ArrayList). El programa debe ejecutarse por consola con un menu de texto que permita: agregar, listar, editar y eliminar productos por su codigo. Usa este estilo para los metodos: agregarProducto(Producto p), eliminarProducto(String codigo). No uses librerias externas, todo debe funcionar con las clases estandar de Java. Explica primero la estructura de las clases y luego presenta el codigo Java completo organizado por clases.
```

**Que cambie:** agregue la INSTRUCCION especifica del menu (agregar, listar, editar, eliminar), un EJEMPLO del estilo de los metodos, una RESTRICCION (no usar librerias externas) y el FORMATO de la respuesta (explicacion antes del codigo, organizado por clases).

**Por que:** sin el menu especifico la IA decidia por su cuenta que operaciones incluir; sin el ejemplo de estilo, los nombres de los metodos salian distintos cada vez; sin la restriccion, en un intento anterior la IA sugirio usar una libreria de terceros para el menu.

**Que mejoro:** la respuesta final incluye las 4 operaciones pedidas, nombra los metodos con el estilo indicado, no usa ninguna libreria fuera del JDK, y presenta primero la explicacion de las clases y despues el codigo completo.

## Componentes del prompt final

| Componente | Texto de mi prompt |
|---|---|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea un CRUD de productos ... El programa debe ejecutarse por consola con un menu de texto que permita: agregar, listar, editar y eliminar productos por su codigo. |
| Contexto | para una tienda pequena, usando una clase Producto con los atributos codigo, nombre, precio y stock, y guardando los datos en una lista en memoria (ArrayList) |
| Ejemplo | Usa este estilo para los metodos: agregarProducto(Producto p), eliminarProducto(String codigo). |
| Formato | Explica primero la estructura de las clases y luego presenta el codigo Java completo organizado por clases. (Restriccion incluida: No uses librerias externas, todo debe funcionar con las clases estandar de Java.) |

## Evaluacion del resultado

| Criterio | Cumple (Si/No) |
|---|---|
| ¿Usa una clase Producto con los 4 atributos pedidos (codigo, nombre, precio, stock)? | Si |
| ¿El menu permite agregar, listar, editar y eliminar productos? | Si |
| ¿Usa unicamente clases estandar de Java, sin librerias externas? | Si |
| ¿Explica la estructura de las clases antes de mostrar el codigo? | Si |
| ¿Los metodos siguen el estilo de nombres dado en el ejemplo? | Si |

## Errores que evite

**Ser demasiado general:** en la version 1 no especifique atributos ni forma de almacenamiento, y la IA tuvo que adivinar. Lo evite en las versiones 2 y 3 dando el contexto exacto: los 4 atributos de Producto y el tipo de almacenamiento (ArrayList en memoria).

**No indicar el formato:** si no hubiera pedido explicitamente "explica primero la estructura y luego el codigo", la IA habria mezclado explicaciones con fragmentos de codigo sin un orden claro. Al indicar el formato en la version 3, la respuesta quedo organizada y facil de seguir.