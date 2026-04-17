# Java_Copiloto

Copiloto técnico em Java — um conjunto de prompts estruturados para auxiliar nos estudos e no desenvolvimento com a stack Java/Spring Boot.

---

## Modos disponíveis

| Modo | Arquivo | Descrição |
|---|---|---|
| **STUDY** | [`prompts/study.md`](prompts/study.md) | Tutor técnico: conceitos, analogias, exemplos e checkpoints de aprendizado |
| **PLAN** | [`prompts/plan.md`](prompts/plan.md) | Plano de implementação revisável (passos, riscos e validações) antes de qualquer código |
| **ASK** | [`prompts/ask.md`](prompts/ask.md) | Responde dúvidas, explica código e diagnostica erros em modo somente leitura |
| **AGENT CODE** | [`prompts/agent-code.md`](prompts/agent-code.md) | Gera implementações completas seguindo o ciclo Descobrir → Planejar → Implementar → Verificar → Finalizar |

---

## Stack principal

- **Linguagem:** Java 17 / 21 (LTS)
- **Framework:** Spring Boot (ou Jakarta EE)
- **Web:** Spring MVC / WebFlux
- **ORM:** JPA/Hibernate
- **Testes:** JUnit 5 + Mockito / Testcontainers
- **Build:** Maven / Gradle
- **Logging:** SLF4J + Logback

---

## Personalidade (Cortana)

Todos os modos adotam a voz da **Cortana**:

- tom calmo, confiante e levemente espirituoso
- didática, direta, sem enrolar
- sem bajulação, sem excesso de emojis
- pronomes: **ela/dela**

---

## Como usar

1. Abra o arquivo do modo desejado em `prompts/`.
2. Copie o conteúdo do prompt.
3. Cole no seu assistente de IA preferido (ex.: GitHub Copilot Chat, ChatGPT, Claude).
4. Comece a interação descrevendo seu contexto ou dúvida.

---

## Estrutura do repositório

```
Java_Copiloto/
├── prompts/
│   ├── study.md        # Modo STUDY — tutor de conceitos Java
│   ├── plan.md         # Modo PLAN — planejamento de implementação
│   ├── ask.md          # Modo ASK — perguntas e diagnóstico (read-only)
│   └── agent-code.md   # Modo AGENT CODE — geração de código
└── README.md
```
