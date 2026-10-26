# detekt

## META
- id: detekt
- owner: EduBalderas
- visibility: public
- idioma: en
- estado: WIP
- tipo: fork
- nivel: L4
  - L0=gobernanza/política
  - L1=marca/metodología
  - L2=flujo/arquitectura
  - L3=producto ejecutable
  - L4=herramienta
- familia: desconocido
- origen: upstream:https://github.com/detekt/detekt
- experimento: desconocido
- nacido_de: detekt/detekt
- orquestado_por: N/A
- brief_desde: N/A

## OBJETIVO
Análisis estático de código Kotlin (complejidad, anidamientos y calidad) mediante CLI y plugin de Gradle.

## QUE_CONTIENE
- Código principal en Kotlin, licencia Apache-2.0 (`LICENSE`). Grupo Maven del árbol actual: `dev.detekt`. Versión de desarrollo: `2.0.0-alpha.6` (`build-logic/src/main/kotlin/Versions.kt`).
- Build Gradle (wrapper `9.8.1`). Compilar exige JDK 17 o superior. Ejecutar detekt 2.0 exige Gradle 8.14.3 o superior.
- Módulos del build raíz (`settings.gradle.kts`): `detekt-api`, `detekt-cli`, `detekt-core`, `detekt-generator`, `detekt-kotlin-analysis-api`, `detekt-kotlin-analysis-api-standalone`, `detekt-metrics`, `detekt-parser`, `detekt-psi-utils`, `detekt-tooling`, `detekt-utils`, `detekt-suppressors`, `build-logic` y `code-coverage-report`.
- Plugin de Gradle en composite build: `detekt-gradle-plugin` (id de plugin 2.x documentado: `dev.detekt`).
- Informes: `detekt-report-html`, `detekt-report-markdown`, `detekt-report-sarif`, `detekt-report-checkstyle`, `detekt-report-complexity`, `detekt-report-statistics`.
- Conjuntos de reglas: complexity, coroutines, comments, empty-blocks, potential-bugs, exceptions, ktlint-wrapper, libraries, naming, performance, ruleauthors, standard-library y style.
- Pruebas: `detekt-test`, `detekt-test-assertj`, `detekt-test-junit`, `detekt-test-utils`.
- Sitio Docusaurus en `website/` (paquete `@detekt/website`) y bots Danger en `bots/` (paquete `@detekt/bots`).
- Ejemplo aparte, con su propio `settings.gradle.kts`: `detekt-sample-extensions`.

## CARACTERISTICAS
- Detección de code smells en Kotlin; `AGENTS.md` documenta más de 200 reglas integradas y conjuntos de reglas configurables.
- Baselines para deuda existente y supresión en fuente con `@Suppress`.
- Informes HTML, Markdown, SARIF y XML tipo Checkstyle, más informes de complejidad (líneas de código, complejidad ciclomática y número de code smells).
- Extensible con reglas, procesadores e informes propios.
- Dos interfaces de primera parte: CLI (`detekt-cli`) y plugin de Gradle.
- El README de upstream documenta además la línea estable 1.x (`1.23.8`), grupo Maven `io.gitlab.arturbosch.detekt` y plugin `io.gitlab.arturbosch.detekt`.
- Sitio: https://detekt.dev. Descripción del fork en GitHub: «Analiza la complejidad, anidamientos y problemas de calidad del código Kotlin».

## FUERA_DE_ALCANCE
- Plugin de IntelliJ: repositorio aparte, https://github.com/detekt/detekt-intellij-plugin.
- Plugin de Maven citado en el README de upstream: https://github.com/Ozsie/detekt-maven-plugin (terceros).
- Integraciones de terceros listadas en el README de upstream (SonarQube, Codacy, Codefactor, Bazel rules, GitHub Actions, TCA, Violations Lib, sputnik, gnag): no viven en este repositorio.
- Reglas y reportes de la comunidad: tema `detekt-plugin` y marketplace en https://detekt.dev/marketplace.

## RELACIONES
- Fork público de https://github.com/detekt/detekt (padre GitHub: `detekt/detekt`). Este remoto: https://github.com/EduBalderas/detekt.
- Documentación y marketplace: https://detekt.dev.
- Publicación Maven del árbol 2.x: grupo `dev.detekt` (POM: nombre `detekt`, descripción «Static code analysis for Kotlin», SCM `https://github.com/detekt/detekt`).
- Línea 1.x citada en el README de upstream: grupo `io.gitlab.arturbosch.detekt`; el wrapper de ktlint se publicaba como `detekt-formatting`.
- Wrapper de ktlint en este árbol: módulo `detekt-rules-ktlint-wrapper`.
- Topics de GitHub del fork: ninguno configurado.

## ETIQUETAS
- kotlin
- analisis-estatico
- detekt
- gradle
- cli
- fork
- apache-2.0

## TOPICS_GITHUB
- N/A
