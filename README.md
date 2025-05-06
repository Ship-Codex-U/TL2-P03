# Practica 03

Objetivo: Desarrollar un analizador semántico que valide la corrección de las estructuras sintácticas procesadas en la fase anterior, asegurando la correcta gestión de tipos de datos, ámbito de variables y evaluación de expresiones aritméticas.

Requerimientos:
1. Entrada:
- Se debe proporcionar una secuencia de tokens generada por el analizador léxico y validada por el analizador sintáctico.
- El programa deberá recorrer el árbol sintáctico y verificar posibles errores semánticos.

2. Validaciones a realizar:
- Declaración y uso de variables: Verificar que todas las variables utilizadas hayan sido declaradas previamente.
- Compatibilidad de tipos: Comprobar que las operaciones aritméticas, lógicas y de asignación sean compatibles con los tipos de datos definidos.
- Ámbito de variables: Identificar si se intenta acceder a una variable fuera de su alcance.
- Control de flujo: Validar las estructuras condicionales y de iteración (if, while, for) para evitar expresiones inválidas.
- Retorno de funciones: Asegurar que las funciones devuelvan un valor acorde a su tipo de retorno.

3. Evaluación de expresiones aritméticas:
-Generar un árbol sintáctico a partir de una expresión matemática proporcionada por el usuario.
-Expresiones permitidas:
-Suma (+), resta (-), multiplicación (*), división (/).
-Uso de paréntesis para definir prioridad.
-Operaciones con números enteros y flotantes.

- Ejemplo de expresión válida:
(5 + 3) * (2 - 4)  

-Implementar un recorrido del árbol (postorden o inorden) para evaluar la expresión.
- Cada nodo del árbol representará un operador o un operando.
- Prioridades de operadores:
Multiplicación y división tienen mayor prioridad que la suma y la resta.
Se respetará el uso de paréntesis para modificar la prioridad.
- Manejo de tipos:
Verificar que los operandos sean numéricos (enteros o flotantes).
Realizar conversión de tipos cuando sea necesario en operaciones mixtas.


4. Manejo de errores:
-División por cero: Generar una excepción o mensaje de error si ocurre.
-Operandos no numéricos: Si una expresión intenta operar con un tipo inválido, se debe notificar el error.
Errores de alcance o uso incorrecto de variables.

5. Salida:
- Si el código es semánticamente correcto, mostrar un mensaje de validación exitosa.
- Si se detectan errores, desplegar mensajes indicando el tipo de error y su ubicación.
- Mostrar el resultado de la evaluación de expresiones.
- Generar y mostrar una tabla de símbolos con información sobre las variables declaradas y su tipo.

Implementación:
Puede implementarse en cualquier lenguaje, siempre que cumpla los requerimientos.
Se recomienda utilizar estructuras como tablas de símbolos y árboles de sintaxis abstracta (AST).
Se pueden emplear herramientas como PLY (Python Lex-Yacc), ANTLR, Bison o Yacc para facilitar la implementación.

Entrega:
- Código fuente con comentarios explicativos.
- Reporte detallando el proceso de desarrollo, incluyendo:
Algoritmos utilizados.
Explicación de la tabla de símbolos.
Estructura del árbol sintáctico.
Casos de prueba con análisis de errores.
- Video corto mostrando el funcionamiento del analizador.

Recomendaciones y Recursos de Apoyo

Recomendaciones:
Construcción de la tabla de símbolos:
Implementar un diccionario o estructura hash para almacenar identificadores y sus atributos.
Incluir información como tipo de dato, valor asignado, ámbito y línea de declaración.


Implementación del Árbol Sintáctico:
Definir una estructura de nodos con operadores y operandos.
Implementar métodos de recorrido (postorden o inorden) para evaluar la expresión.

Manejo de errores semánticos:
Implementar un sistema de detección temprana para minimizar propagación de errores.
Mostrar mensajes claros con línea de error y posible causa.

Uso de herramientas:
PLY (Python Lex-Yacc): Biblioteca en Python basada en Yacc/Lex.
ANTLR: Framework para generar analizadores de lenguaje.
Bison/Yacc: Herramientas clásicas para generar analizadores en C/C++.


## Descarga he instalación/configuración del proyecto

Clonar  repositorio

```bash
git clone
```

## Settear ambiente local
(Version de python: 3.12.1)

1. Crear un entorno virtual con **venv** dentro de la nueva carpeta que se creo al clonar el proyecto.

```bash
python -m venv nombre-entorno-virtual
```

2. Activar el entorno virtual creado.
```bash
nombre-entorno-virtual\Scripts\activate
```

3. Instalar los paquetes necesarios que requiere el proyecto para funcionan que vienen indicados en el archivo **requirements.txt**.
```bash
pip install -r requirements.txt
```

Nota: la aplicación para realizar y editar la interfaz del proyecto (Qt Design - design.exe) lo podras encontrar dentro de tu entorno virtual en la siguiente ruta
```bash
entorno-virtual-creado/Lib/Pyside6/
```

## Antes de realizar tu primer push.......
Asegurate que en tu archivo **.gitignore** aparezca por lo menos el siguiente renglon:

nombre-entorno-virtual-creado/  <------------ para que al momento de subir tus cambios no subas paquetes y librerias innecesarios a la repo que hagan que pese de mas.