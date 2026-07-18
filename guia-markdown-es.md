[Inicio/Home](README.md) · [English version](guide-markdown-en.md)

---

# Guía básica de Markdown <!-- omit from toc -->

# Guía básica de Markdown <!-- omit from toc -->

## Sintaxis, organización y ejemplos <!-- omit from toc -->

**Autor:** Gonzalo Fernández Romero

**Objetivo:** Documentación y escritura técnica

**Fecha de creación:** julio de 2026

**Última actualización:** julio de 2026

---

## Introducción <!-- omit from toc -->

Markdown es un lenguaje ligero empleado para escribir documentos estructurados. Esta guía recoge lo esencial para:

- Tomar apuntes.
- Documentar programas.
- Preparar contenido para GitHub.
- Escribir fórmulas o incluir código.

## Índice <!-- omit from toc -->


- [1. Títulos y secciones](#1-títulos-y-secciones)
- [2. Formato de texto](#2-formato-de-texto)
  - [Negrita](#negrita)
  - [Cursiva](#cursiva)
  - [Negrita y cursiva](#negrita-y-cursiva)
- [3. Párrafos y saltos de línea](#3-párrafos-y-saltos-de-línea)
- [4. Listas](#4-listas)
  - [Lista sin numerar](#lista-sin-numerar)
  - [Lista numerada](#lista-numerada)
  - [Lista con niveles o anidadas](#lista-con-niveles-o-anidadas)
- [5. Enlaces](#5-enlaces)
  - [Enlaces internos](#enlaces-internos)
- [6. Imágenes](#6-imágenes)
- [7. Código](#7-código)
  - [Código dentro de una frase](#código-dentro-de-una-frase)
  - [Bloques de código](#bloques-de-código)
- [8. Citas](#8-citas)
- [9. Tablas](#9-tablas)
- [10. Líneas separadoras](#10-líneas-separadoras)
- [11. Comentarios ocultos](#11-comentarios-ocultos)
- [12. Visual Studio Code](#12-visual-studio-code)
  - [Vista previa](#vista-previa)
  - [Generar índice automático](#generar-índice-automático)
      - [Instalación](#instalación)
      - [Creación del índice](#creación-del-índice)
- [13. Referencias](#13-referencias)
 

## 1. Títulos y secciones

En Markdown se usa el símbolo `#` para crear títulos:

```
# Título principal
## Sección
### Subsección
#### Apartado
##### Nivel inferior
```
Es importante el ***espacio después de `#`***.

---

## 2. Formato de texto

### Negrita

```markdown
**Texto en negrita**
```

### Cursiva

```markdown
*Texto en cursiva*
```

### Negrita y cursiva

```markdown
***Negrita y cursiva***
```


## 3. Párrafos y saltos de línea

Para crear un nuevo párrafo, se deja una línea vacía.

```markdown
Primer párrafo.

Segundo párrafo.
```

Para forzar un salto de línea, se pueden añadir dos espacios al final.

---


## 4. Listas

### Lista sin numerar

```markdown
- Elemento 1
- Elemento 2
- Elemento 3
```
De nuevo, es importante el espacio después de `-`.

### Lista numerada

```markdown
1. Elemento 1
2. Elemento 2
3. Elemento 3
```

### Lista con niveles o anidadas

```markdown
- Elemento principal 1
  - Secundario 1
  - Secundario 2
- Elemento principal 2
```

---

## 5. Enlaces

La estructura de un enlace es:

```markdown
[Texto visible](https://ejemplo.com)
```

También se puede mostrar directamente una dirección:

```markdown
<https://example.com>
```

### Enlaces internos

Se usan para enlazar una sección del propio documento:

```markdown
[Ir a la sección de listas](#4-listas)
```

Normalmente, para convertir un título en identificador, se escribe en minúsculas, se sustituyen los espacios por guiones y se eliminan signos de puntuación.

## 6. Imágenes

De forma local, primero hay que descargar las imágenes. Es recomendable guardarlas en una carpeta independiente. Para poner la imagen:

```markdown
![Descripción de la imagen](imagenes/ejemplo.png)
```

También se puede usar una imagen que se encuentra en internet:

```markdown
![Descripción](https://example.com/imagen.png)
```

## 7. Código

### Código dentro de una frase

Cuando se quiere mencionar una palabra o instrucción como código dentro de un párrafo, se escribe entre acentos graves:

```text
`código que no se ejecuta`
```

Ejemplo:

```markdown
La función `print()` permite mostrar información.
```

El código corto no se ejecuta. Solamente se presenta con un formato visual diferente para distinguirlo del resto del texto.

La barra invertida indica que el siguiente carácter debe mostrarse de forma literal:

```markdown
\# Esto aparece como texto normal
```


### Bloques de código

Cuando el código ocupa varias líneas, se utiliza un bloque de código.

El bloque comienza y termina con tres acentos graves:

````text
```
Primera línea
Segunda línea
Tercera línea
```
````

En la vista previa aparecerá dentro de un recuadro.

## 8. Citas

Las citas permiten destacar un fragmento de texto y separarlo visualmente del contenido principal.

Se crean colocando el símbolo `>` al principio de la línea.

```markdown
> Primera línea de la cita.
> Segunda línea de la cita.
> Tercera línea de la cita.
```

También se puede incluir una cita dentro de otra utilizando varios símbolos `>`:

```markdown
> Cita principal.
>
>> Cita dentro de la cita principal.
```

## 9. Tablas

Una tabla básica se escribe de la siguiente forma:

```markdown
| Columna 1 | Columna 2 | Columna 3 |
|---|---|---|
| Dato 1 | Dato 2 | Dato 3 |
| Dato 4 | Dato 5 | Dato 6 |
```

- `:---` alinea el contenido a la izquierda.
- `:---:` centra el contenido.
- `---:` alinea el contenido a la derecha.

```markdown
| Izquierda | Centro | Derecha |
|:---|:---:|---:|
| Texto | Texto | Texto |
| Texto | Texto | Texto |
```

## 10. Líneas separadoras

Una línea horizontal permite separar visualmente dos partes de un documento. Conviene dejar una línea vacía antes y después.

```markdown
---
```

## 11. Comentarios ocultos

```markdown
<!--
Este es un comentario interno.

Puede ocupar varias líneas.
-->
```

Aunque no aparezcan en la vista previa, sí se ven al abrir el archivo original o el código fuente en GitHub. No deben contener información privada.

## 12. Visual Studio Code

### Vista previa
Para abrir la vista previa:

```text
Ctrl + Shift + V
```

Para abrir el editor y la vista previa al mismo tiempo:

```text
Ctrl + K
```

y después:

```text
V
```

### Generar índice automático


Para insertar un índice que forme parte del propio archivo se puede utilizar la extensión **Markdown All in One**.

##### Instalación

1. Abrir el apartado **Extensions** de Visual Studio Code.
2. Buscar `Markdown All in One`.
3. Comprobar que la extensión está publicada por **Yu Zhang**.
4. Seleccionar **Install**.


##### Creación del índice

1. Colocar el cursor en la posición donde se desea insertar el índice.
2. Se abre la paleta de comandos y se usa el atajo:

```text
Ctrl + Shift + P
```

3. Buscar y ejecutar:

```text
Markdown All in One: Create Table of Contents
```

La extensión analizará los títulos y generará una lista de enlaces internos. Para actualizar el índice, sirve con:

```text
Ctrl + S
```

En ocasiones se desea mostrar un título en el documento sin incluirlo en el índice automático.

Para excluirlo, se añade el comentario `<!-- omit from toc -->` al final del encabezado:

```text
# Título del documento <!-- omit from toc -->
```

## 13. Referencias

Las siguientes fuentes se han consultado para comprobar la sintaxis y las funciones descritas en esta guía:

1. CommonMark. [CommonMark Specification](https://spec.commonmark.org/current/).  
   Especificación de referencia para la sintaxis básica de Markdown.

2. GitHub Docs. [Sintaxis básica de escritura y formato](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).  
   Documentación sobre el uso de Markdown y GitHub Flavored Markdown en GitHub.

3. Microsoft. [Markdown and Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown).  
   Documentación oficial sobre edición, vista previa y navegación de archivos Markdown en Visual Studio Code.

4. Zhang, Yu. [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one).  
   Extensión de Visual Studio Code utilizada para generar y actualizar automáticamente la tabla de contenidos.



<!--
Pendiente:

Hacer un README que abra página que te de opciones de ir a la guía en español e ingles

-->

