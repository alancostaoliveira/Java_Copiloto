# Stack de Referência — Java_Copiloto

> Este arquivo é a **fonte de verdade** da stack usada por todos os prompts.  
> Ao mudar de projeto, edite aqui e replique (ou substitua a seção correspondente em cada prompt).

---

## Stack principal

| Componente        | Padrão                        | Alternativas comuns                        |
|-------------------|-------------------------------|--------------------------------------------|
| **JDK**           | Java 21 LTS                   | 17 LTS, 11, 8                              |
| **Build**         | Maven                         | Gradle                                     |
| **Framework**     | Spring Boot 3.x               | Quarkus, Micronaut, Jakarta EE, Java puro  |
| **Web**           | Spring MVC (servlet)          | WebFlux (reativo), JAX-RS                  |
| **ORM / Banco**   | JPA / Hibernate + PostgreSQL  | JDBC, jOOQ, MySQL, MongoDB                 |
| **Testes unit.**  | JUnit 5 + Mockito             | —                                          |
| **Testes integ.** | Testcontainers                | H2 (somente dev/test)                      |
| **Logging**       | SLF4J + Logback               | Log4j2                                     |
| **Lint / Format** | Checkstyle + Spotless         | PMD, ErrorProne                            |
| **Empacotamento** | JAR executável                | WAR, Native Image (GraalVM)                |
| **Concorrência**  | Virtual Threads (Java 21)     | ExecutorService, WebFlux                   |

---

## Recursos Java 21 em uso

- **Virtual Threads** (Project Loom) — habilitar via `spring.threads.virtual.enabled=true` no Spring Boot 3.2+
- **Structured Concurrency** (preview/incubator) — para coordenação de tarefas paralelas com escopo definido
- **Records** — DTOs e value objects imutáveis
- **Switch Expressions / Pattern Matching** — substituição de `instanceof` + cast e `switch` verboso
- **Text Blocks** — SQL, JSON e templates inline
- **Sequenced Collections** — `SequencedList`, `SequencedSet`, `SequencedMap`
