# Instalação no Gemini

## Google Antigravity / ambiente compatível com Agent Skills

O Google documenta Agent Skills como diretórios contendo `SKILL.md` e recursos auxiliares. Para escopo de projeto, use:

```text
<project-root>/.agents/skills/juriskill/
```

Copie o repositório Juriskill para esse diretório preservando a estrutura.

Para os produtos Antigravity que usam escopo global documentado pelo Google, consulte a documentação atual do produto antes da instalação, pois os caminhos globais podem variar entre interfaces/CLIs.

## Teste de ativação

Abra uma nova sessão e peça:

```text
Revise esta petição usando Juriskill. Valide toda legislação e jurisprudência em fontes oficiais e execute EXISTÊNCIA → IDENTIDADE → CONTEÚDO → PERTINÊNCIA. Marque qualquer referência que não possa confirmar.
```

## Resultado esperado

O agente deve:

1. localizar as referências jurídicas da peça;
2. não confiar na memória do modelo como fonte;
3. pesquisar fontes oficiais;
4. conferir se cada precedente realmente sustenta a proposição;
5. marcar cada referência como `VERIFICADA`, `PARCIALMENTE VERIFICADA`, `NÃO VERIFICADA` ou `CONTRADITA`;
6. não completar números, datas, relatores ou ementas por inferência.

## Gemini web/app

Uma conversa comum no Gemini web/app não deve ser presumida como equivalente a uma Agent Skill instalada. Se a interface utilizada não carregar `SKILL.md` nativamente, use o conteúdo como instrução persistente do recurso equivalente disponível naquela interface e mantenha os arquivos de referência acessíveis ao modelo.
