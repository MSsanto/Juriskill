# Instalação no Claude

## Claude Code

O Juriskill usa o formato `SKILL.md`. Instale o diretório completo da skill no local de Agent Skills reconhecido pelo seu ambiente Claude Code, preservando `SKILL.md`, `references/`, `checklists/` e `tests/`.

Não copie somente o texto principal: os arquivos auxiliares fazem parte do protocolo de validação.

## Teste de ativação

Depois de instalar, abra uma nova sessão e peça:

```text
Revise esta petição com o Juriskill. Identifique toda legislação e jurisprudência citada e execute o gate EXISTÊNCIA → IDENTIDADE → CONTEÚDO → PERTINÊNCIA. Não corrija silenciosamente referências que não puder verificar.
```

A resposta deve classificar referências como `VERIFICADA`, `PARCIALMENTE VERIFICADA`, `NÃO VERIFICADA` ou `CONTRADITA`.

## Teste adversarial

Use os casos em `tests/` para verificar se o agente recusa referências inventadas e detecta processo verdadeiro usado para uma tese que o julgado não sustenta.

## Claude.ai

Uma conversa comum no Claude.ai não deve ser presumida como equivalente à instalação de uma Agent Skill no Claude Code. Quando o produto não oferecer carregamento nativo da skill, forneça o `SKILL.md` e os arquivos necessários como instruções/contexto do projeto e peça explicitamente que o protocolo seja aplicado à tarefa.
