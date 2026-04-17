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
| **REVIEW** | [`prompts/review.md`](prompts/review.md) | Revisão crítica de código: legibilidade, segurança (OWASP), testes, design e performance |
| **DEBUG** | [`prompts/debug.md`](prompts/debug.md) | Diagnóstico sistemático de bugs: stack traces, logs, hipóteses e estratégia de correção |

---

## Stack principal

- **Linguagem:** Java 21 LTS (recomendado) / 17 LTS
- **Framework:** Spring Boot 3.x (ou Jakarta EE)
- **Web:** Spring MVC / WebFlux
- **ORM:** JPA/Hibernate
- **Testes:** JUnit 5 + Mockito / Testcontainers
- **Build:** Maven / Gradle
- **Logging:** SLF4J + Logback
- **Concorrência:** Virtual Threads (Project Loom, Java 21)

> A stack completa e editável está em [`prompts/_stack.md`](prompts/_stack.md). Edite esse arquivo para refletir o seu projeto.

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
2. Edite o **Bloco de Configuração** no topo do arquivo (stack, idioma, nível).
3. Copie o conteúdo do prompt.
4. Cole no seu assistente de IA preferido (ex.: GitHub Copilot Chat, ChatGPT, Claude).
5. Comece a interação descrevendo seu contexto ou dúvida.

---

## Estrutura do repositório

```
Java_Copiloto/
├── prompts/
│   ├── _stack.md       # Fonte de verdade da stack (compartilhada por todos os modos)
│   ├── study.md        # Modo STUDY — tutor de conceitos Java
│   ├── plan.md         # Modo PLAN — planejamento de implementação
│   ├── ask.md          # Modo ASK — perguntas e diagnóstico (read-only)
│   ├── agent-code.md   # Modo AGENT CODE — geração de código
│   ├── review.md       # Modo REVIEW — revisão crítica de código
│   └── debug.md        # Modo DEBUG — diagnóstico e correção de bugs
├── CONTRIBUTING.md
└── README.md
```

---

## Contribuindo

Consulte [CONTRIBUTING.md](CONTRIBUTING.md) para convenções de nomenclatura, estrutura obrigatória dos prompts e como propor novos modos.
