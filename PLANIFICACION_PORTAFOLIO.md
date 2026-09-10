# Planificación del Portafolio Virtual

*Documento consolidado del desafío "Planificación de portafolio virtual" — Fundamentos de
Ciencia de Datos, Talento Digital. Sirve de base para la construcción del portafolio final.*

**Estudiante:** Eric Ignacio Rodríguez Acuña
**Contacto:** eric.rodriguez.acu@gmail.com · [linkedin.com/in/ericrodrigueza](https://linkedin.com/in/ericrodrigueza)

> **Retroalimentación docente:** no se recibió retroalimentación formal sobre este desafío antes
> de avanzar a la etapa de finalización del portafolio.

---

## 1. Selección del repositorio

**Repositorio elegido: GitHub.**

GitHub es la opción más adecuada para construir mi portafolio virtual por las siguientes
razones, en línea con mi perfil como ingeniero orientado a datos y programación:

- **Control de versiones nativo:** permite documentar la evolución de cada proyecto (commits,
  ramas, historial de cambios), algo que plataformas como YouTube o Stack Overflow no ofrecen.
- **GitHub Pages:** posibilita publicar un sitio web estático gratuito directamente desde el
  repositorio, ideal para mostrar un portafolio navegable sin costo de hosting.
- **Estándar de la industria técnica:** es la plataforma que reclutadores y líderes técnicos de
  tecnología y minería de datos revisan primero para evaluar código real, no solo un CV.
- **Integración directa con herramientas que ya uso:** Jupyter Notebooks, Python y Spark se
  visualizan correctamente en la interfaz de GitHub, sin necesidad de conversores externos.

A diferencia de Stack Overflow (orientado a preguntas y respuestas, no a mostrar proyectos
propios) o YouTube (formato audiovisual, poco adecuado para mostrar código), GitHub combina
documentación técnica, código ejecutable y presentación profesional en un mismo lugar.

## 2. Ejemplo de portafolio existente

**Portafolio de referencia:** [github.com/GeostatsGuy](https://github.com/GeostatsGuy)

Se trata del perfil de GitHub de Michael Pyrcz, profesor de la Universidad de Texas en Austin y
referente en geoestadística, data analytics y machine learning aplicado a subsuelo. Su perfil
incluye un README personal y una serie de repositorios que documentan toda su producción
académica y docente: GeostatsPy (reimplementación en Python de GSLIB, la librería clásica de
geoestadística), PythonNumericalDemos y MachineLearningDemos, entre otros. Lo elegí por sobre
un portafolio genérico de ingeniería de datos porque está exactamente en la intersección que me
interesa: geoestadística clásica y machine learning aplicados a datos espaciales.

**Dos características que me gustan:**

- El perfil no es solo una lista de proyectos: cada repositorio indica claramente su propósito
  docente o de investigación y el número de estrellas/forks, lo que transmite de inmediato el
  impacto y la adopción real de su trabajo por la comunidad.
- Combina divulgación (cursos, demos bien documentadas) con una librería de software seria
  (GeostatsPy), mostrando que puede tanto enseñar conceptos como construir herramientas
  robustas — un balance que quiero reflejar en mi propio portafolio.

**Dos características perfectibles:**

- Con más de 15 repositorios visibles en el perfil, cuesta identificar rápidamente por dónde
  empezar; un README de perfil con una sección "Empieza aquí" o proyectos fijados ("pinned")
  con una frase de contexto ayudaría a un visitante nuevo.
- La descripción de cada repositorio es muy técnica y asume que el visitante ya conoce la jerga
  de geoestadística; una breve traducción a lenguaje de negocio (qué problema resuelve, para
  quién) ampliaría la audiencia del portafolio más allá de pares académicos.

**Mejoras aplicadas a mi propio portafolio** (ver perfil de GitHub, sección "Empieza aquí" y
descripciones de proyectos en lenguaje simple): ordené mis repositorios fijados con una frase
de contexto en lenguaje simple, y agregué una sección introductoria clara que oriente a quien
visite mi perfil por primera vez.

## 3. Prueba seleccionada como ejemplo de habilidades

**Prueba elegida:** Optimización y Despliegue de Modelos Predictivos Supervisados

Elijo este trabajo porque condensa el ciclo completo de optimización responsable de modelos
supervisados: construcción de un Pipeline único (ColumnTransformer + modelo) para evitar fugas
de información, búsqueda de hiperparámetros con GridSearchCV para un RandomForestClassifier y
un RandomForestRegressor, y validación con esquemas de cross-validation anidada
(StratifiedKFold para clasificación, KFold para regresión) separando claramente la búsqueda de
hiperparámetros de la evaluación final.

Lo considero especialmente relevante para mi perfil porque este mismo stack metodológico —Random
Forest, ajuste de hiperparámetros y validación cruzada— es exactamente el que se usa hoy para
estimar recursos minerales (ley de mineral, tonelaje) a partir de datos de sondajes, como
complemento o alternativa a los métodos geoestadísticos clásicos (kriging) con los que ya
trabajo. Es el puente natural entre mi formación en geoestadística y minería, y las herramientas
de machine learning que estoy incorporando en este bootcamp; de hecho, es el área en la que me
gustaría enfocar un proyecto propio más adelante.

Un aspecto que destaco de este trabajo, y que sumé como mejora en la reflexión final, fue
reportar con honestidad un resultado negativo: el modelo de regresión obtuvo un R² promedio
negativo en la validación cruzada externa, resultado esperable dado que el dataset de práctica
tenía solo 10 observaciones. En vez de ocultar o maquillar esa métrica, la interpreté
explícitamente como una limitación del tamaño muestral y no del algoritmo — una práctica que
considero más valiosa para un portafolio técnico que mostrar solo resultados perfectos.

**Vínculo de visualización:**
[optimizacion_modelos_predictivos.ipynb](https://github.com/EricRodAcu/Fundamentos-de-ciencia-de-datos/blob/main/optimizacion_modelos_predictivos.ipynb)

## 4. Perfil en GitHub

**Usuario:** [github.com/EricRodAcu](https://github.com/EricRodAcu)

Bio del perfil, respondiendo las preguntas solicitadas:

- **¿Quién eres?** Eric Rodríguez Acuña, Ingeniero Civil de Minas (Universidad de Concepción) y
  MBA (Universidad Isabel I, España).
- **¿De dónde eres?** Chile, actualmente radicado en Coelemu, Región de Ñuble.
- **¿A qué te dedicas?** Trabajo en la intersección entre ingeniería de minas y análisis de
  datos: planificación minera, control de gestión, estudios técnicos y, cada vez más, ciencia de
  datos aplicada a procesos mineros.
- **¿Cuál es tu formación?** Ingeniería Civil de Minas y MBA, más un bootcamp en curso de
  Fundamentos de Ciencia de Datos (Talento Digital), que incluye Python, Machine Learning, Big
  Data (Spark) e inferencia estadística.
- **¿Cuáles son tus experiencias previas?** Práctica de investigación en JKMRC (Universidad de
  Queensland, Australia) sobre tronadura y fragmentación; Oficina Técnica en
  Salfamantenciones/Minera Centinela; programa Trainee en Timining (planificación y control de
  producción minera); y liderazgo de equipos multiculturales en Clayton Hotel, Irlanda.
- **¿Cómo y a través de qué medios te pueden contactar?** Correo:
  eric.rodriguez.acu@gmail.com · LinkedIn: linkedin.com/in/ericrodrigueza

## 5. Buenas prácticas para el desarrollo del portafolio

- Mantener el README principal actualizado y con una estructura clara (resumen, stack técnico,
  proyectos destacados, contacto), ya que es lo primero que se lee.
- Documentar cada proyecto con su objetivo, tecnologías usadas y resultados concretos, evitando
  dejar código sin contexto.
- Cuidar la consistencia visual y de nomenclatura entre repositorios (nombres de carpetas,
  convenciones de commits) para transmitir profesionalismo.
- Priorizar calidad sobre cantidad: 3 o 4 proyectos bien documentados generan mejor impresión
  que diez proyectos incompletos o sin explicación.
- Actualizar el portafolio periódicamente a medida que se completan nuevos desafíos o proyectos,
  evitando que quede desactualizado respecto al nivel técnico actual.
- Revisar ortografía y redacción tanto en español como en inglés si se apunta a un público
  internacional.
