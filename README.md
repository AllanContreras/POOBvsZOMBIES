# POOBvsZOMBIES
es un videojuego de defensa en el que un jugador debe proteger la casa de Dave de una invasión de zombies, utilizando diversas plantas . Cada planta tiene características únicas, el jugador debe emplear estratégicamente para evitar que los zombies crucen el campo de juego.

# Informe de Análisis Dinámico basado en el Test Coverage
Se presenta la cobertura de pruebas (Test Coverage) de las clases en el paquete dominio del proyecto. Las métricas analizadas incluyen:

Class Coverage: Cobertura de clases probadas.
Method Coverage: Cobertura de métodos probados.
Line Coverage: Cobertura de líneas ejecutadas en las pruebas.
Branch Coverage: Cobertura de ramas (condicionales) evaluadas.

![image](https://github.com/user-attachments/assets/06965a20-4e44-4922-9cfa-3d89a07828ba)


# Observaciones y Análisis
- Clases con Cobertura Adecuada:

- PruebasJuego: Tiene 97% en métodos y 83% en líneas, siendo una de las clases mejor probadas. Se alcanzan niveles altos en todas las métricas.
- Zombie y GestorZombies: Ambas tienen buena cobertura de líneas (70%) y ramas moderadas (31%-45%).
Clases con Cobertura Baja:

- Planta:
Method Coverage: 31% (solo 9 de 29 métodos probados).
Line Coverage: 24% (45 de 185 líneas ejecutadas).
Branch Coverage: Solo 7%, indicando falta de pruebas en los caminos condicionales.
- GestorPlantas:
Solo 28% en métodos y 16% en líneas, con 6% en branches. Esta clase parece ser una prioridad de mejora para aumentar su cobertura.
Oportunidades de Mejora:

- Ramas (Branch Coverage): En general, la cobertura de ramas en la mayoría de las clases está por debajo del 50%. Esto indica que no todos los escenarios condicionales están siendo evaluados.
- Métodos Clave: Clases como PoobvsZombies y GestorPlantas presentan métodos que no están siendo cubiertos en su totalidad.
Líneas No Ejecutadas: En Planta y GestorPlantas, gran parte del código no se ejecuta en las pruebas actuales.



# Análisis Estático basado en el Reporte de PMD

![image](https://github.com/user-attachments/assets/3d289568-56e0-485b-9fa2-2d9ce5d9e069)

- Análisis por Categoría
  
  - Best Practices (17 violaciones)

Estas violaciones generalmente indican problemas con el uso adecuado de estándares y prácticas recomendadas en el código.
Ejemplo crítico:
Uso de System.out/err en lugar de un logger, lo cual afecta la calidad del código y dificulta la gestión de logs en producción.
Recomendación: Implementar un sistema de logging (como Logger de SLF4J o Log4j) en lugar de usar System.out/err.
  - Code Style (62 violaciones)

La mayoría de las violaciones aquí corresponden a 56 errores de prioridad media.
Estas violaciones suelen involucrar:
Formato de código inconsistente (nombres de variables, espaciado, indentación).
Declaraciones innecesarias o repetitivas.
Recomendación: Aplicar reglas de formateo con herramientas como Checkstyle o el formateador de código de IntelliJ. Configurar reglas claras para nombres y estructuras.
   - Design (7 violaciones)

Violaciones de diseño con prioridad alta que indican problemas en la arquitectura o estructura del código.
Posibles causas:
Clases con alta complejidad ciclomática.
Acoplamiento fuerte entre clases.
Recomendación: Refactorizar el código aplicando principios SOLID y reduciendo la complejidad de métodos/clases.
  - Documentation (12 violaciones)

Se identifican problemas en la documentación, como:
Falta de comentarios Javadoc en métodos o clases.
Documentación incompleta o desactualizada.
Recomendación:
Añadir documentación clara y consistente a todas las clases y métodos públicos.
Usar herramientas como Javadoc para verificar y generar documentación automáticamente.
  - Error Prone (10 violaciones)

Incluye errores potenciales que podrían causar fallos en ejecución:
Mal manejo de excepciones.
Código que puede producir NullPointerException o división por cero.
Recomendación:
Agregar controles y validaciones para evitar excepciones.
Implementar pruebas unitarias adicionales para detectar estos errores temprano.
   - Performance (10 violaciones)

Todas las violaciones son de alta prioridad, indicando problemas críticos de rendimiento:
Uso ineficiente de bucles.
Creación innecesaria de objetos o colecciones.
# Mejoras a Realizar :
Optimizar las estructuras de datos y el manejo de bucles.
Evitar el uso de objetos temporales innecesarios que afecten la memoria y el rendimiento.
-  Priorización de Acciones
Corregir violaciones de alta prioridad:

Implementar logging en lugar de System.out/err.
Resolver problemas de performance y errores críticos de diseño.
Mejorar el estilo del código:

Adoptar una herramienta de formateo automático como Checkstyle.
Documentación:

Añadir Javadoc para cumplir con los estándares de documentación.
Refactorización de diseño:

Aplicar principios de diseño limpio para reducir la complejidad del código.
 - Conclusión
El análisis estático revela problemas principalmente en Code Style y Best Practices, así como errores de diseño y rendimiento que deben priorizarse. Implementando las recomendaciones anteriores, se mejorará la calidad, mantenibilidad y rendimiento del código.


