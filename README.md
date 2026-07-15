# CIEGES — Plugin de Documentos Oficiais SES/TO

Plugin do **Claude Code** que ajuda a redigir, revisar e estruturar **documentos
oficiais da Secretaria de Estado da Saúde do Tocantins (SES/TO)** — atos
normativos (portarias, políticas), documentos administrativos e técnicos,
documentos de contratação (Lei 14.133/2021), e artefatos de governança de TIC e
engenharia de software.

O plugin aplica um padrão de **redação oficial**, exige **fundamentação normativa
citável** (nunca de memória) e, quando o tema envolve dados ou TIC, aplica também
critérios de **segurança da informação e LGPD**.

## O que ele faz

- **Identifica o tipo de documento** a partir da sua intenção e monta a estrutura
  correta (seções, quadros, matriz de riscos, ciclo PDCA quando cabível).
- **Aplica as 40 regras de redação e formatação** da SES/TO ao *como escrever*.
- **Aplica critérios de segurança da informação e proteção de dados** quando o
  documento envolve segurança, cibersegurança, LGPD, prontuário,
  interoperabilidade/RNDS, telessaúde, TIC ou tratamento de dados.
- **Exige base normativa vigente** para cada afirmação e decisão, resolvendo
  conflitos de normas por antinomia (LINDB).

## Estrutura do repositório

```
CIEGES/
├─ README.md
├─ .claude-plugin/
│  └─ plugin.json                     # manifesto do plugin
└─ skills/
   └─ documento-oficial-ses-to/
      ├─ SKILL (1).md                     # fluxo de trabalho + as 40 regras
      └─ references/
         ├─ criterios-seguranca-informacao-protecao-dados.md
         └─ catalogo-tipos-documento.md
```

| Arquivo | Conteúdo |
|---|---|
| `.claude-plugin/plugin.json` | Manifesto que registra o plugin no Claude Code. |
| `skills/documento-oficial-ses-to/SKILL.md` | Skill principal: fluxo de trabalho e as 40 regras de redação/formatação. |
| `references/criterios-seguranca-informacao-protecao-dados.md` | 19 critérios de segurança da informação e LGPD, matriz de riscos, PDCA, governança e checklist. |
| `references/catalogo-tipos-documento.md` | Catálogo dos tipos de documento: finalidade, base normativa, estrutura/seções e matriz de decisão. |

## Como instalar

1. Abra o Claude Code no diretório onde você trabalha com os documentos.
2. Adicione este repositório como marketplace/fonte de plugins e instale o plugin
   `documento-oficial-ses-to`.
3. A skill é acionada automaticamente ao redigir, revisar ou estruturar um
   documento oficial da SES/TO.

> Consulte a documentação do Claude Code para o comando exato de instalação de
> plugins na sua versão.

## Como usar

Basta descrever o documento que você precisa, por exemplo:

- *"Redija uma portaria instituindo o comitê de segurança da informação da SES/TO."*
- *"Monte o Termo de Referência para contratação de solução de prontuário eletrônico."*
- *"Revise este ofício aplicando as regras de redação oficial."*

O plugin identifica o tipo, monta a estrutura, aplica as 40 regras e — quando
pertinente — os critérios de segurança/LGPD, sempre pedindo confirmação da base
normativa vigente.

## Observações

- Onde uma regra depende de padrão interno da SES/TO (papel timbrado, numeração
  SEI, fonte oficial, fluxo de assinatura), o texto traz a marca
  **`[confirmar norma interna SES/TO]`** — substitua pela instrução vigente da casa.
- As 40 regras e as referências foram redigidas a partir dos padrões públicos
  (Manual de Redação da Presidência da República, ABNT, LINDB, Lei 14.133/2021,
  LGPD). Substitua por textos normativos oficiais da SES/TO quando disponíveis.

---

Mantido pela **BHQ Consultoria** para a governança documental da SES/TO (CIEGES).
