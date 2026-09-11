# Juriskill

Juriskill é uma skill portátil para reduzir alucinações jurídicas em tarefas envolvendo Direito brasileiro.

O foco da v0.1 é simples: nenhuma lei, artigo, súmula, tema, precedente ou jurisprudência deve ser apresentada como verificada com base apenas na memória do modelo.

## Objetivo

O Juriskill aplica um gate de validação antes de uma referência jurídica ser usada como fundamento confirmado.

Fluxo principal:

`pedido jurídico → pesquisa → fonte oficial → existência → identidade → conteúdo → pertinência → redação → auditoria final`

Cada referência recebe um status:

- `VERIFICADA`
- `PARCIALMENTE VERIFICADA`
- `NÃO VERIFICADA`
- `CONTRADITA`

## Escopo da v0.1

- Legislação federal brasileira
- STF
- STJ
- CNJ
- Validação de citações jurídicas
- Detecção de precedente verdadeiro usado com tese falsa
- Detecção de referências inventadas
- Checklist final de auditoria

## Fora do escopo inicial

- Parecer jurídico autônomo
- Substituição de revisão profissional
- Cálculo de prazos processuais
- Suporte garantido a todos os tribunais estaduais, federais, trabalhistas e eleitorais
- Automação de peticionamento

## Estrutura

```text
Juriskill/
├── SKILL.md
├── README.md
├── LICENSE
├── references/
│   ├── SOURCE_POLICY.md
│   └── OFFICIAL_SOURCES.md
├── checklists/
│   ├── legislation-verification.md
│   ├── precedent-verification.md
│   └── final-legal-audit.md
└── tests/
    ├── hallucinated-case.md
    ├── real-case-false-holding.md
    ├── hallucinated-statute.md
    └── unverifiable-citation.md
```

## Princípio central

> Conhecimento paramétrico do modelo não constitui verificação de fonte jurídica.

O modelo pode usar conhecimento interno para formular hipóteses, termos de busca e contexto inicial. Ele não pode usar esse conhecimento como prova de que uma referência jurídica existe, está vigente ou sustenta determinada tese.

## Compatibilidade

O núcleo é escrito em Markdown e evita depender de ferramentas exclusivas de um único fornecedor. A meta é manter compatibilidade com ambientes que aceitem skills ou instruções baseadas em `SKILL.md`, incluindo Codex, Claude Code e Gemini CLI, com adaptações pontuais quando necessárias.

## Status

Projeto em desenvolvimento. A v0.1 é experimental e deve ser validada em testes adversariais antes de uso em produção jurídica.
