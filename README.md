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

