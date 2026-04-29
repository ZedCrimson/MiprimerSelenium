1. ¿Qué hace la anotación @BeforeEach?
Es una anotación que indica que un método se debe ejecutar antes de cada prueba.
Se usa para preparar todo lo necesario para que cada test empiece con el mismo estado, como abrir el navegador o inicializar objetos.

2. ¿Para qué sirve assertTrue?
Función: assertTrue es un método de aserción que verifica que una condición booleana sea verdadera.
Uso: En pruebas unitarias o funcionales, se usa para validar que el resultado esperado es verdadero. Si la condición es falsa, la prueba falla.

3. ¿Qué diferencia hay entre findElement() y findElements()?
findElement()

Devuelve el primer elemento que coincide con el criterio de búsqueda.
Si no encuentra ningún elemento, lanza una excepción NoSuchElementException.
Uso cuando se espera un único elemento o solo interesa el primero.
findElements()

Devuelve una lista (List<WebElement>) con todos los elementos que coinciden con el criterio.
Si no encuentra ningún elemento, devuelve una lista vacía (no lanza excepción).
Uso cuando se esperan múltiples elementos o se quiere verificar la cantidad de elementos que cumplen la condición.

4. ¿Por qué utilizamos una clase LoginPage en lugar de escribir todo en el test?
Patrón Page Object Model (POM): La clase LoginPage representa la página de login como un objeto con sus elementos y acciones.
Ventajas:
Separación de responsabilidades: El test se enfoca en la lógica de la prueba, mientras que la clase LoginPage maneja la interacción con la interfaz.
Reutilización: Los métodos de la página (por ejemplo, login(), enterUsername()) pueden reutilizarse en múltiples tests.
Mantenimiento: Si cambia la UI, solo se actualiza la clase LoginPage, no todos los tests.
Legibilidad: Los tests son más claros y fáciles de entender porque usan métodos descriptivos en lugar de código de bajo nivel.
