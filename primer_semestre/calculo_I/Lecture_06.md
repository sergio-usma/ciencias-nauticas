# Funciones Reales y Cuadráticas: Análisis Formal, Gráfico y de Dominio en el Plano Cartesiano**

Esta lección establece el marco fundamental para el estudio de funciones reales, con énfasis en la función cuadrática como caso de estudio profundo. Los objetivos centrales son: (1) comprender la definición rigurosa de función real como subconjunto del plano cartesiano R×R con asignación única; (2) dominar el análisis estructural de la función cuadrática (vértice, discriminante, cortes con ejes, simetría); y (3) desarrollar la capacidad de determinar dominio y rango no por defecto, sino mediante el análisis de restricciones impuestas por la regla de correspondencia. Este conocimiento es relevante porque constituye la base conceptual para el cálculo diferencial, la modelación de fenómenos físicos (trayectorias parabólicas), la optimización en ingeniería y economía, y el análisis de señales en ciencias aplicadas.

---

### 1. OUTLINE CONCEPTUAL (El Panorama General)

```
FUNCIONES REALES EN EL PLANO CARTESIANO
│
├── 1. MARCO DE REFERENCIA: R×R (Plano Cartesiano)
│   ├── Conjunto universal de pares ordenados (x, y) con x, y ∈ R
│   ├── Ejes como subconjuntos particulares
│   │   ├── Eje X: puntos (x, 0)
│   │   └── Eje Y: puntos (0, y)
│   └── Representación geométrica de relaciones matemáticas
│
├── 2. RELACIONES VS. FUNCIONES
│   ├── Relación: cualquier subconjunto de R×R
│   └── Función: relación con asignación ÚNICA (cada x → un solo y)
│       ├── Dominio (Df): subconjunto de R donde la regla está definida
│       ├── Codominio: conjunto declarado de llegada (generalmente R)
│       └── Rango/Imagen: subconjunto del codominio efectivamente alcanzado
│
└── 3. FUNCIÓN CUADRÁTICA: ESTUDIO DE CASO PROFUNDO
    ├── Forma general: f(x) = ax² + bx + c, con a ≠ 0
    ├── Componentes estructurales
    │   ├── Coeficiente a: concavidad (a>0: ↑ mín; a<0: ↓ máx)
    │   ├── Coeficiente b: desplazamiento horizontal del vértice
    │   └── Coeficiente c: corte con eje Y (0, c)
    ├── Análisis mediante discriminante (Δ = b² - 4ac)
    │   ├── Δ > 0: dos raíces reales distintas (dos cortes eje X)
    │   ├── Δ = 0: una raíz real doble (tangencia en vértice)
    │   └── Δ < 0: sin raíces reales (sin corte eje X; raíces complejas)
    ├── Vértice (h, k): punto extremo de la parábola
    │   ├── h = -b/(2a) [coordenada x del vértice]
    │   └── k = f(h) [valor mínimo o máximo]
    ├── Eje de simetría: recta vertical x = h
    └── Técnica fundamental: completación de cuadrados
        └── Convierte forma general → forma canónica: a(x - h)² + k
```

---

### 2. DESGLOSE DE CONCEPTOS FUNDAMENTALES (El Núcleo del Conocimiento)

#### **Concepto 1: Función Real**
*   **Definición de Alto Nivel:** Una función real f es una relación que asigna a cada elemento x de un subconjunto D ⊆ R (dominio) un ÚNICO elemento y en el codominio R, mediante una regla de correspondencia específica. Se denota f: D ⊆ R → R.
*   **Explicación Mecanicista (El "Cómo"):** La función actúa como un transformador: ingresa un valor x del dominio, la regla de correspondencia (ej: 2x² + x + 4) procesa ese valor, y produce un único valor de salida y. La variable x es independiente; y es dependiente de x. Para verificar si una relación es función, se aplica la "prueba de la recta vertical": cualquier recta vertical (x = constante) debe intersectar la gráfica en a lo sumo un punto.
*   **Implicaciones y Matices (El "Por Qué" Importa):** No toda expresión algebraica define automáticamente una función de R en R. El dominio debe restringirse explícitamente cuando la regla de correspondencia no está definida para algunos reales (raíces pares de negativos, denominadores cero, logaritmos de no positivos). Es crítico distinguir entre codominio (el conjunto que DECLARAMOS como llegada) y rango (el conjunto que EFECTIVAMENTE se alcanza). Esta distinción es fundamental en análisis matemático posterior y en aplicaciones donde la salida debe cumplir restricciones físicas.

#### **Concepto 2: Discriminante (Δ)**
*   **Definición de Alto Nivel:** El discriminante de una ecuación cuadrática ax² + bx + c = 0 es la expresión Δ = b² - 4ac, que determina la naturaleza y existencia de las raíces reales (cortes con el eje X) sin necesidad de resolver completamente la ecuación.
*   **Explicación Mecanicista (El "Cómo"):** El discriminante aparece dentro de la raíz cuadrada en la fórmula general: x = [-b ± √(b² - 4ac)]/(2a). Al evaluar su signo, se puede clasificar:
    *   Δ > 0 → √Δ es real positivo → dos valores reales distintos → dos cortes.
    *   Δ = 0 → √Δ = 0 → un único valor (raíz doble) → tangencia en el vértice.
    *   Δ < 0 → √Δ es imaginario → no hay soluciones reales → sin cortes.
*   **Implicaciones y Matices (El "Por Qué" Importa):** El discriminante "discrimina" los casos posibles. En el ejemplo de clase (2x² + x + 4), Δ = -31 < 0, lo que inmediatamente revela que la parábola NO corta el eje X, información crucial antes de graficar. En cálculo, el discriminante se relaciona con la naturaleza de los puntos críticos. En física, determina si un proyectil alcanza cierta altura. En álgebra lineal, análogos del discriminante aparecen en formas cuadráticas y matrices.

#### **Concepto 3: Vértice de una Parábola (h, k)**
*   **Definición de Alto Nivel:** El vértice es el punto (h, k) donde la parábola alcanza su valor extremo: mínimo si a > 0, máximo si a < 0. Es el único punto por donde pasa el eje de simetría.
*   **Explicación Mecanicista (El "Cómo"):** Se obtiene mediante:
    *   h = -b/(2a) (derivado de completar cuadrados o de la derivada f'(x) = 2ax + b = 0)
    *   k = f(h) = a·h² + b·h + c
    En forma canónica f(x) = a(x - h)² + k, el vértice es directamente legible.
*   **Implicaciones y Matices (El "Por Qué" Importa):** El vértice es el ancla estructural de la gráfica. Conocer (h, k) permite:
    *   Determinar el rango: [k, ∞) si a>0; (-∞, k] si a<0.
    *   Establecer el eje de simetría (x = h) para encontrar puntos simétricos sin tablas.
    *   En problemas de optimización, el vértice da directamente el valor óptimo (costo mínimo, ganancia máxima, altura máxima).
    *   En el ejemplo, el vértice en (-0.25, 3.875) indica que el punto más bajo está por encima del eje X, confirmando Δ < 0.

#### **Concepto 4: Restricción del Dominio por la Regla de Correspondencia**
*   **Definición de Alto Nivel:** El dominio de una función no es un supuesto, sino una consecuencia directa de las operaciones matemáticas presentes en la regla de correspondencia: debe ser el conjunto de todos los números reales para los cuales la regla produce un número real.
*   **Explicación Mecanicista (El "Cómo"):** Para determinar el dominio, se identifican las operaciones "problemáticas":
    *   Raíces de índice par: √(g(x)) → exige g(x) ≥ 0.
    *   Denominadores: 1/g(x) → exige g(x) ≠ 0.
    *   Logaritmos: ln(g(x)) → exige g(x) > 0.
    Se resuelven las desigualdades/ecuaciones resultantes y se expresa el dominio en notación de intervalos.
*   **Implicaciones y Matices (El "Por Qué" Importa):** Error común es asumir dominio = R. En el ejemplo de clase con f(x) = √(x - 4), si se declarara f: R → R, NO sería función porque para x < 4 la regla no produce reales. La función correcta es f: [4, ∞) → R. Esta precisión es crucial en análisis matemático, en la definición de funciones compuestas y en aplicaciones donde las variables tienen significado físico (tiempos no negativos, concentraciones no negativas, etc.).

---

### 3. ANÁLISIS DE CASOS PRÁCTICOS Y APLICACIONES (El Laboratorio)

#### **Caso 1: Análisis Completo de f(x) = 2x² + x + 4**

*   **El Escenario:** Se propone en clase analizar la función cuadrática y = 2x² + x + 4, construyendo su gráfica y determinando dominio y rango, con la condición de NO usar tablas de valores.
*   **Metodología de Análisis:**
    1.  **Identificar coeficientes:** a = 2, b = 1, c = 4.
    2.  **Corte con eje Y:** x = 0 → y = 4 → punto (0, 4).
    3.  **Corte con eje X:** Resolver 2x² + x + 4 = 0. Calcular Δ = b² - 4ac = 1 - 32 = -31.
    4.  **Interpretar Δ:** Δ < 0 → No hay raíces reales → La gráfica NO corta el eje X.
    5.  **Hallar vértice:** h = -b/(2a) = -1/(4) = -0.25; k = f(-0.25) = 2(0.0625) + (-0.25) + 4 = 0.125 - 0.25 + 4 = 3.875 = 31/8.
    6.  **Determinar apertura:** a = 2 > 0 → Parábola abre hacia arriba (vértice es mínimo).
    7.  **Eje de simetría:** x = -0.25.
    8.  **Puntos simétricos:** Usando (0,4) y eje x = -0.25, el punto simétrico es x = -0.5 → f(-0.5) = 2(0.25) -0.5 + 4 = 0.5 -0.5 + 4 = 4 → punto (-0.5, 4).
    9.  **Verificación adicional:** Calcular f(1) = 2+1+4 = 7 → punto (1,7); su simétrico: x = -1.5 → f(-1.5) = 2(2.25) -1.5 +4 = 4.5 -1.5 +4 = 7 → punto (-1.5, 7). Confirma simetría.
*   **Solución o Conclusión:**
    *   **Gráfica:** Parábola con vértice en (-0.25, 3.875), abre hacia arriba, corta eje Y en (0,4), no corta eje X, simétrica respecto a x = -0.25.
    *   **Dominio:** R (todos los reales), pues es un polinomio.
    *   **Rango:** [31/8, ∞) o [3.875, ∞).
*   **Lección Clave para el Estudiante:** La estructura de la función (coeficientes) y el discriminante proveen toda la información necesaria para graficar con precisión. Las tablas de valores son ineficientes y pueden ocultar la visión global. El vértice y los cortes con ejes son los puntos estratégicos.

#### **Caso 2: Análisis de f(x) = √(x - 4)**

*   **El Escenario:** El instructor modifica la regla de correspondencia a y = √(x - 4) para ilustrar restricciones de dominio y la necesidad de definición precisa.
*   **Metodología de Análisis:**
    1.  **Identificar operación restrictiva:** Raíz cuadrada (índice par).
    2.  **Imponer condición de existencia real:** El radicando debe ser ≥ 0 → x - 4 ≥ 0.
    3.  **Resolver:** x ≥ 4.
    4.  **Determinar dominio:** [4, ∞).
    5.  **Corte con eje X:** y = 0 → √(x-4) = 0 → x - 4 = 0 → x = 4 → punto (4, 0).
    6.  **Corte con eje Y:** x = 0 → 0 no pertenece al dominio → No hay corte con eje Y.
    7.  **Análisis gráfico:** La función arranca en (4,0) y crece lentamente (sublineal) hacia la derecha. Para x=5, y=1; x=8, y=2; etc.
    8.  **Rango:** [0, ∞).
*   **Solución o Conclusión:**
    *   La función NO puede definirse de R en R porque para x<4 no produce valores reales.
    *   La definición correcta es: f: [4, ∞) → R, f(x) = √(x-4).
    *   El punto de inicio es (4,0), que es tanto el extremo izquierdo del dominio como el corte con el eje X.
*   **Lección Clave para el Estudiante:** El dominio NO es negociable ni asumible. La regla de correspondencia IMPONE el dominio. Una función está bien definida solo cuando se especifica explícitamente su dominio (o es claro por contexto, como en polinomios donde se sobreentiende R). La gráfica refleja fielmente el dominio: no existe para x<4.

---

### 4. CUADRO DE REFERENCIA RÁPIDA (El "Kit de Herramientas")

| Categoría | Elemento Clave | Definición / Fórmula / Descripción | Contexto de Uso / Importancia |
| :--- | :--- | :--- | :--- |
| **Terminología Esencial** | **Plano Cartesiano R×R** | Conjunto de todos los pares ordenados (x, y) con x, y ∈ R | Marco universal para representar relaciones y funciones reales. |
| | **Función** | Relación que asigna a cada x del dominio un ÚNICO y | Modelo matemático de dependencia unívoca. |
| | **Dominio** | Conjunto de valores x para los que la función está definida | Define el campo de existencia de la función. |
| | **Rango/Imagen** | Conjunto de valores y efectivamente alcanzados por la función | Describe la salida posible del modelo. |
| **Fórmula/Teorema** | **Discriminante Δ** | Δ = b² - 4ac (para ax² + bx + c = 0) | Determina número y tipo de raíces reales. |
| | **Fórmula General** | x = [-b ± √(b² - 4ac)]/(2a) | Solución de ecuaciones cuadráticas. |
| | **Vértice (h, k)** | h = -b/(2a); k = f(h) | Punto extremo de la parábola; define el rango. |
| | **Forma Canónica** | f(x) = a(x - h)² + k | Permite lectura directa de vértice y traslaciones. |
| **Concepto Clave** | **Simetría en Parábola** | Eje de simetría vertical x = h; f(h + d) = f(h - d) | Permite generar puntos sin cálculos adicionales. |
| | **Función Par** | f(-x) = f(x) para todo x en el dominio | Simetría respecto al eje Y. En cuadráticas ocurre solo si b = 0. |
| | **Restricción de Dominio** | Condición impuesta por raíces pares (≥0), denominadores (≠0), logaritmos (>0) | Define el dominio real de la función. |

---

### 5. PREGUNTAS DE AUTOEVALUACIÓN DE ALTO NIVEL (El Examen Oral)

1.  **Pregunta 1 (Síntesis):** Un compañero afirma que para graficar cualquier función cuadrática basta con calcular tres puntos usando una tabla de valores. Usando los conceptos de discriminante, vértice y eje de simetría, explique por qué esta estrategia es ineficiente y potencialmente incorrecta. ¿Qué información crítica podría perderse al usar solo una tabla arbitraria?
2.  **Pregunta 2 (Análisis de Caso):** Considere la función definida por f(x) = √(x² - 5x + 6). Determine su dominio natural (el mayor subconjunto de R para el cual la función produce valores reales). Luego, sin graficar, determine si esta función corta el eje Y. Justifique cada paso.
3.  **Pregunta 3 (Comparación y Contraste):** Compare y contraste los conceptos de "discriminante" en ecuaciones cuadráticas y "prueba de la recta vertical" para funciones. ¿Qué papel juega cada uno en el análisis de funciones? ¿En qué se diferencian fundamentalmente?
4.  **Pregunta 4 (Implicación):** Un proyectil se lanza y su altura (en metros) está dada por h(t) = -5t² + 20t + 2, donde t es el tiempo en segundos. ¿Qué información sobre el movimiento del proyectil se obtiene directamente del vértice? ¿Qué información se obtiene del discriminante? ¿Cómo interpretaría físicamente un discriminante negativo en este contexto?
5.  **Pregunta 5 (La "Trampa"):** Se le presenta la siguiente definición: "Sea f: R → R, definida por f(x) = 1/(x-2)". Inmediatamente, usted detecta un error grave. ¿Cuál es? Reescriba la definición de forma correcta y explique por qué la definición original es inválida. Si un estudiante usara esta definición errónea para calcular f(2), ¿qué ocurriría y por qué?

---

### 6. VOCABULARIO ESENCIAL (El Glosario)

1.  **Plano Cartesiano:** Sistema de coordenadas formado por dos rectas numéricas perpendiculares (ejes X e Y) que se intersectan en el origen, permitiendo representar puntos mediante pares ordenados (x, y).
2.  **Producto Cartesiano:** Operación entre conjuntos (especialmente R×R) que produce el conjunto de todos los pares ordenados posibles, donde el primer elemento pertenece al primer conjunto y el segundo al segundo.
3.  **Relación:** Cualquier subconjunto del producto cartesiano R×R; una correspondencia entre elementos de dos conjuntos.
4.  **Función:** Relación donde a cada elemento del dominio le corresponde exactamente un elemento del codominio.
5.  **Dominio (de una función):** Conjunto de todos los valores de entrada (x) para los cuales la función está definida y produce un valor real.
6.  **Codominio:** Conjunto que se declara como el de llegada de la función; en este curso, típicamente R.
7.  **Rango (o Imagen):** Subconjunto del codominio que contiene todos los valores de salida (y) que la función realmente produce.
8.  **Función Cuadrática:** Función polinómica de grado dos, de la forma f(x) = ax² + bx + c, con a ≠ 0. Su gráfica es una parábola.
9.  **Parábola:** Curva cónica, lugar geométrico de los puntos que equidistan de un foco y una directriz; gráfica de una función cuadrática.
10. **Vértice:** Punto donde la parábola alcanza su valor máximo o mínimo; punto de inflexión de la curva.
11. **Discriminante (Δ):** En una ecuación cuadrática, la expresión Δ = b² - 4ac que determina la naturaleza de las raíces.
12. **Raíz (o Cero) de una Función:** Valor de x para el cual f(x) = 0; corresponde a los cortes de la gráfica con el eje X.
13. **Eje de Simetría:** Recta vertical que pasa por el vértice de la parábola, dividiéndola en dos mitades especulares.
14. **Completación de Cuadrados:** Técnica algebraica para transformar un trinomio cuadrático en la forma a(x - h)² + k, revelando el vértice.
15. **Forma Canónica (o de Vértice):** Representación de una función cuadrática como f(x) = a(x - h)² + k, donde (h, k) es el vértice.

---

### 7. TAREAS DE INVESTIGACIÓN POST-CLASE (La Bitácora del Explorador)

1.  **Profundización (El origen de la fórmula general):** Investigue el método de **completación de cuadrados** para deducir la fórmula general de la ecuación de segundo grado. Prepare una demostración paso a paso, explicando por qué se suma y resta (b/2a)². ¿Qué relación tiene este método con la determinación del vértice? (Pista: el instructor mencionó que esta es la tarea: "¿De dónde sale la fórmula general?").
2.  **Ampliación (Números complejos):** El instructor mencionó los números imaginarios ante la pregunta de Sergio. Investigue el **campo de los números complejos (C)**. ¿Cómo se define la unidad imaginaria i? ¿Cómo se expresan y operan los números complejos? ¿Qué son las raíces complejas conjugadas y por qué aparecen cuando Δ < 0 en una ecuación cuadrática con coeficientes reales? Prepare un breve informe (1-2 páginas) con ejemplos.
3.  **Aplicación (Proyecto de modelado):** El instructor anunció un proyecto basado en el aprendizaje por proyectos. Investigue una aplicación real de las funciones cuadráticas en su área de estudio (ingeniería, economía, física, biología, etc.). Por ejemplo, en ingeniería civil: el trazado de arcos parabólicos en puentes; en economía: funciones de costo-ingreso-beneficio; en física: lanzamiento de proyectiles. Identifique cómo se usarían los conceptos de vértice (valor óptimo), discriminante (alcance de ciertos valores) y dominio restringido (variables no negativas, tiempos, etc.). Tráigalo a la siguiente clase como propuesta inicial para su proyecto.

---

### 8. CONEXIONES INTERDISCIPLINARIAS Y VISIÓN DE FUTURO (El "Mundo Real")

*   **Conexión con Cálculo Diferencial:** La determinación del vértice mediante h = -b/(2a) es un caso particular de encontrar puntos críticos mediante la derivada f'(x) = 2ax + b = 0. La segunda derivada f''(x) = 2a confirma si es mínimo (a>0) o máximo (a<0). Este será el procedimiento estándar para funciones más complejas.
*   **Conexión con Álgebra Lineal:** La completación de cuadrados es análoga a la diagonalización de formas cuadráticas mediante matrices simétricas. El discriminante generaliza a conceptos como el determinante y los valores propios en el análisis de la naturaleza de puntos críticos en funciones de varias variables (matriz Hessiana).
*   **Conexión con Física:** Las trayectorias de proyectiles en campos gravitatorios uniformes (sin resistencia) son parábolas. El vértice representa la altura máxima y el momento en que se alcanza; el discriminante determina si el proyectil alcanza cierta altura objetivo o la distancia horizontal de impacto. El dominio (tiempo) está naturalmente restringido a valores no negativos hasta el impacto.
*   **Conexión con Ingeniería y Economía:** En problemas de optimización (maximizar ganancias, minimizar costos, diseñar estructuras eficientes), las funciones cuadráticas modelan relaciones donde existe un punto óptimo. El análisis de dominio incluye restricciones físicas o económicas (producción no negativa, límites de recursos).
*   **Visión de Futuro:** El estudio de funciones reales es la puerta de entrada al análisis matemático. Próximos temas incluirán funciones polinómicas de mayor grado, funciones racionales, trigonométricas, exponenciales y logarítmicas. El dominio, rango y análisis gráfico serán herramientas recurrentes. En cursos superiores, estos conceptos se extienden a funciones vectoriales, campos escalares y análisis funcional, manteniendo siempre la misma base conceptual: la relación entre una entrada (dominio) y una salida (rango) bajo reglas específicas.