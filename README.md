Trabajo Práctico Integrador (TPI): Gestión de Datos de Países en Python

Alumnos: Lucas Matias Catanzaro y Emiliano Fiscina. Grupo 27.

Docentes: Cinthia Rigoni, Tutor Brian Lara c3 y Tutor Ana Mutti c4

El trabajo se desarrollará en etapas, donde cada una se enfocará en la composición que tendrá nuestro programa.
Etapa 1: Carga y Visualización de Datos
1.	Carga de Datos: Crear una función en Python que lea los datos de los países desde un archivo.CSV
2.	Mostrar Datos: Implementar una función que imprima en la consola una tabla con la información básica de todos los países (nombre, superficie, población, continente).
Etapa 2: Insertar datos
1.	Carga de País: Una función que solicite al usuario el ingreso de País, Población, Superficie y Continente que considere faltante.
Etapa 3: Actualización de datos
1.	Modificar datos: El usuario podrá modificar los datos que fueron cargados inicialmente por el archivo, ingresará País y podrá modificar Población y Superficie.
Etapa 4: Búsqueda:
1.	Búsqueda de información: El usuario podrá realizar la búsqueda de los datos que el desee.
Etapa 5: Filtros de Información
Permitirá al usuario filtrar la lista de países según los siguientes criterios:
1.	Filtrar por Continente: El usuario podrá filtrar como parámetro el nombre de un continente y devuelva una lista con los países que pertenecen a ella.
2.	Filtrar por Población: El usuario podrá filtrar ingresando un número mínimo y máximo que muestre los países que cumplen con lo solicitado.
3.	Filtrar por Superficie: El usuario podrá filtrar ingresar un número mínimo y máximo que muestre los países que cumplen con lo solicitado.
Etapa 6: Ordenamiento de Datos
Permitirá al usuario ordenar la lista de países de acuerdo a diferentes atributos:
1.	Ordenar por Nombre: El usuario podrá ordenar los países alfabéticamente por su nombre de forma ascendente o descendente.
2.	Ordenar por Población: El usuario podrá ordenar los países de mayor a menor población y viceversa.
3.	Ordenar por Superficie: El usuario podrá ordenar los países según su superficie de forma ascendente o descendente.
Etapa 7: Cálculos Estadísticos
Esta etapa le dará al usuario la información necesaria de estadísticas según cálculos sobre el conjunto de datos:
1.	País más y menos poblado: Determinar cuál es el país con la mayor y menor población.
2.	Promedio de Población: Calcular la población promedio de todos los países.
3.	Promedio de Superficie: Sumar la población de todos los países para obtener un total.
4.	Países por Continente: Contar cuántos países hay en cada región y mostrar los resultados.
Conceptos de Programación Aplicados en el Proyecto de Gestión de Países
Para el armado de nuestro código utilizamos los siguientes conceptos.
1. Estructuras de Datos
a. Listas 
Una lista es una colección ordenada y mutable de elementos.
La variable lista_paises es una lista que almacena todos los registros de países.
Almacenar resultados temporales: Se utilizan listas para guardar los resultados de búsquedas (buscar_pais), filtrados (filtrar_paises) u ordenamientos (ordenar_paises).
Iteración: Permite recorrer uno por uno todos los países para realizar cálculos (como en mostrar_estadisticas) o comparaciones.
b. Diccionarios
Un diccionario es una colección desordenada de pares clave-valor. Es la forma más natural de representar un objeto o registro. En el código, cada país individual es un diccionario:
Claves fijas: Cada diccionario de país tiene claves definidas ('nombre', 'poblacion', 'superficie', 'continente').
Acceso rápido: Permite acceder a los atributos del país por su nombre (clave), por ejemplo: pais['poblacion'].
Mutabilidad: Permite actualizar valores específicos de un país, como su población y superficie, en la función actualizar_pais.
2. Principios de Programación
a. Funciones
Las funciones son bloques de código reutilizable diseñados para realizar una tarea específica. Su uso promueve el modularidad y la legibilidad del código.
Modularidad: El código está dividido en funciones pequeñas y enfocadas (ejemplos: agregar_pais, limpiar_pantalla, obtener_nombre).
Función Principal (main): El programa inicia y se controla desde la función main(), que actúa como el bucle central de la aplicación.
Funciones Auxiliares: Las funciones obtener_nombre, obtener_poblacion, y obtener_superficie se utilizan específicamente como funciones clave para el ordenamiento.
b. Condicionales (if/elif/else)
Las condicionales permiten que el programa tome decisiones y ejecute diferentes bloques de código basados en el cumplimiento de ciertas condiciones.
Validación de entrada: Se usan (obtener_entrada_no_vacia, obtener_entrada_numerica) para asegurar que el usuario ingrese datos válidos.
Flujo del programa: La función main() utiliza una cadena de if/elif para ejecutar la acción correspondiente a la opción del menú seleccionada por el usuario.
Validación de datos y existencia: En cargar_datos, se usa if para verificar la existencia del archivo, el número de columnas y el tipo de dato.
c. Archivos CSV (Manejo de Datos)
Un archivo CSV es un formato de texto simple utilizado para almacenar datos tabulares.
Persistencia: La función cargar_datos lee el archivo paises.csv línea por línea para inicializar la lista de países, permitiendo que los datos persistan entre ejecuciones del programa, cada línea del archivo se separa en sus componentes (nombre, población, superficie, continente) usando el método split(',').
Diagrama de flujo
 
Explicación del Diagrama de Flujo

Inicio y Carga: El programa comienza llamando a cargar_datos, que intenta leer y validar la información del archivo CSV. Si tiene éxito, devuelve la lista_paises sino devuelve error de carga de archivo.
Bucle Principal (while True): Si se cargan datos, el programa entra en un ciclo infinito que:
Limpia la consola (limpiar_pantalla).
Muestra las opciones disponibles (mostrar_menu).
Espera la entrada del usuario.
Evaluación: Se utiliza una estructura if/elif para dirigir el flujo a la función correspondiente según la opción seleccionada.
Ejecución de Funciones: según la opción seleccionada llama a la función que será:
1.	Agregar país
2.	Actualizar datos de un país
3.	Buscar país por nombre
4.	Filtrar países
5.	Ordenar países
6.	Mostrar estadísticas
7.	Mostrar todos los países
8.	Salir
9.	O otra opción que elija retornara al menú
se ejecuta, opera sobre lista_paises y muestra un resultado.
Pausa: Después de cada operación (o error de opción), el programa se pausa esperando que el usuario presione Enter, lo que permite ver los resultados antes de que la pantalla se limpie para el siguiente menú.
Fin: El bucle se rompe (break) solo si el usuario elige la opción 8 (Salir).
