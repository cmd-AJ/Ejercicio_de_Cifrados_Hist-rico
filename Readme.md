# Proyecto de Cifrados Historicos en 

## Descripción

Este proyecto implementa varios métodos clásicos de criptografía utilizando Python, sin el uso de librerías externas. El objetivo es comprender los fundamentos matemáticos y lógicos detrás de los cifrados tradicionales y las técnicas básicas de criptoanálisis.

El código incluye implementaciones de:

- Cifrado César y su descifrado
- Cifrado ROT13
- Cifrado y descifrado de Vigenère
- Análisis de frecuencias de caracteres

Todos los algoritmos están diseñados con fines educativos.

---

## Contenido del Proyecto

### 1. Cifrado César

El cifrado César es un cifrado por sustitución simple que desplaza cada letra del texto un número fijo de posiciones en el alfabeto.

**Funciones**
- `cifrado_cesar(texto, desplazamiento)`
- `decifrado_cesar(texto, desplazamiento)`

**Características**
- Opera sobre letras alfabéticas
- Mantiene intactos los caracteres que no son letras
- Utiliza aritmética modular para evitar desbordamientos del alfabeto

**Ejemplo**
```python
mensaje = "hola"
mensaje_cifrado = cifrado_cesar(mensaje, 3)
mensaje_descifrado = decifrado_cesar(mensaje_cifrado, 3)
```

---

### 2. Cifrado ROT13

ROT13 es una variante del cifrado César con un desplazamiento fijo de 13 posiciones.

**Funciones**
- `rot13cifrado(texto)`
- `rot13decifrado(texto)`

**Características**
- Utiliza internamente el cifrado César
- El cifrado y descifrado son simétricos
- Se usa comúnmente con fines demostrativos

---

### 3. Cifrado de Vigenère

El cifrado de Vigenère es un cifrado por sustitución polialfabética que utiliza una clave para determinar el desplazamiento de cada letra.

**Funciones**
- `cifrado_devigenere(plaintext, llave)`
- `decifrado_devigenere(mensaje, llave)`

**Características**
- Convierte el texto y la clave a mayúsculas
- Aplica desplazamientos variables según la clave
- Conserva espacios y signos de puntuación
- Emplea aritmética modular

**Ejemplo**
```python
message = "hola"
llave = "sol"

encrypted = cifrado_devigenere(message, llave)
decrypted = decifrado_devigenere(encrypted, llave)
```

---

### 4. Análisis de Frecuencias

El análisis de frecuencias es una técnica de criptoanálisis que permite identificar patrones en textos cifrados por sustitución simple.

**Función**
- `analisis_frecuencias(texto)`

**Funcionamiento**
- Convierte el texto a mayúsculas
- Cuenta la aparición de cada letra de la A a la Z
- Calcula el porcentaje de frecuencia de cada carácter
- Muestra los resultados ordenados de mayor a menor frecuencia

**Ejemplo**
```python
texto_cifrado = "KHOOR ZRUOG"
analisis_frecuencias(texto_cifrado)
```

---

## Requisitos

- Python 3.x
- No se requieren librerías externas

---

## Objetivo Académico

Este proyecto está orientado al aprendizaje de:
- Criptografía clásica
- Aritmética modular
- Manejo de caracteres ASCII
- Implementación manual de algoritmos
- Técnicas básicas de criptoanálisis

---
