# Contribuindo para o Java_Copiloto

Obrigado por querer melhorar este projeto! Aqui você encontra tudo que precisa para propor alterações com qualidade.

---

## O que é este projeto?

Uma coleção de **prompts estruturados** para um copiloto técnico Java (persona Cortana), prontos para usar em qualquer assistente de IA (GitHub Copilot Chat, ChatGPT, Claude, etc.).

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
├── CONTRIBUTING.md     # Este arquivo
└── README.md
```

---

## Como contribuir

### 1. Fork e branch

```bash
git clone https://github.com/<seu-usuario>/Java_Copiloto.git
cd Java_Copiloto
git checkout -b feat/nome-da-melhoria
```

### 2. Faça suas alterações

Siga as convenções descritas abaixo.

### 3. Abra um Pull Request

- Título claro no formato: `feat: descrição` / `fix: descrição` / `docs: descrição`
- Descreva o que mudou e por que.
- Se for um novo modo, inclua um exemplo de sessão.

---

## Convenções de nomenclatura

| Item | Convenção | Exemplos |
|---|---|---|
| Arquivo de prompt | `kebab-case.md` | `agent-code.md`, `review.md` |
| Arquivo compartilhado | prefixo `_` | `_stack.md` |
| Modo no README | `ALL CAPS` | **REVIEW**, **DEBUG** |
| Versão do prompt | comentário HTML no topo | `<!-- version: 1.0 -->` |

---

## Estrutura obrigatória de um prompt

Todo arquivo de modo (`prompts/*.md`, exceto `_stack.md`) deve seguir esta estrutura:

```markdown
<!-- version: X.Y -->
<!--
╔══════════════════════════════════════════════════════════╗
║  BLOCO DE CONFIGURAÇÃO — edite antes de colar o prompt  ║
╠══════════════════════════════════════════════════════════╣
║  STACK_FILE : prompts/_stack.md  (ou cole sua stack)    ║
║  IDIOMA     : pt-BR  (troque por "en-US" se necessário) ║
║  NIVEL      : intermediário  (iniciante / avançado)      ║
╚══════════════════════════════════════════════════════════╝
-->

# Prompt (Instruções) — Copiloto "NOME_DO_MODO" (Java Edition)

## IDENTIDADE
(Descreve o papel e missão do modo)

---

## 1) STACK (EDITÁVEL)
(Referência ao _stack.md ou stack inline para o modo)

---

## 2) IDIOMA (EDITÁVEL)
(Instrução de idioma)

---

## 3) PERSONALIDADE (EDITÁVEL) — "tipo Cortana"
(Tom e voz da persona)

---

## REGRAS DO MODO NOME (IMPORTANTÍSSIMO)
(Regras específicas do modo)

---

## FORMATO OBRIGATÓRIO DE RESPOSTA
(Template de saída)

---

## EXEMPLO DE SESSÃO
(Diálogo simulado: input do usuário → resposta da Cortana)
```

### Seções obrigatórias

| Seção | Obrigatória | Descrição |
|---|---|---|
| Bloco de configuração (comentário HTML) | ✅ | Versão + parâmetros editáveis |
| `## IDENTIDADE` | ✅ | Missão do modo |
| `## 1) STACK (EDITÁVEL)` | ✅ | Stack do projeto |
| `## 2) IDIOMA (EDITÁVEL)` | ✅ | Instrução de idioma |
| `## 3) PERSONALIDADE (EDITÁVEL)` | ✅ | Persona Cortana |
| `## REGRAS DO MODO` | ✅ | Regras comportamentais |
| `## FORMATO OBRIGATÓRIO DE RESPOSTA` | ✅ | Template de saída |
| `## EXEMPLO DE SESSÃO` | ✅ | Diálogo simulado |

---

## Atualizando a stack

A stack fica centralizada em `prompts/_stack.md`. Ao mudar de projeto ou atualizar versões:

1. Edite `prompts/_stack.md`.
2. Copie/adapte a seção `## 1) STACK (EDITÁVEL)` nos prompts que você usa.
3. Não altere a estrutura das tabelas do `_stack.md` sem atualizar o README.

---

## Propondo um novo modo

1. Crie `prompts/novo-modo.md` seguindo a estrutura obrigatória acima.
2. Adicione o modo à tabela "Modos disponíveis" no `README.md`.
3. Verifique se a persona Cortana está consistente com os demais modos.
4. Inclua um `## EXEMPLO DE SESSÃO` completo e realista.

---

## Atualizando a personalidade (Cortana)

A persona é descrita em cada prompt na seção `## 3) PERSONALIDADE (EDITÁVEL)`. Se quiser alterar o tom globalmente:

- Atualize todos os arquivos de modo **e** documente a mudança neste arquivo.
- Mantenha consistência: `"Certo."`, `"Entendi."`, pronomes ela/dela, sem bajulação.

---

## Versionamento dos prompts

- Use `<!-- version: X.Y -->` no topo de cada arquivo.
- Incremente `Y` para mudanças menores (nova regra, novo exemplo).
- Incremente `X` para mudanças que alteram o comportamento do modo de forma significativa.

---

## Dúvidas?

Abra uma [issue](https://github.com/alancostaoliveira/Java_Copiloto/issues) descrevendo sua dúvida ou sugestão.
