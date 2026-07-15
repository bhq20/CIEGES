# Critérios de Segurança da Informação e Proteção de Dados — SES/TO

> **Referência de conteúdo** para documentos oficiais da Secretaria de Estado da Saúde do Tocantins (SES/TO) que envolvam **segurança da informação, cibersegurança, privacidade/LGPD, prontuário, interoperabilidade/RNDS, telessaúde, TIC ou tratamento de dados**.
>
> Esta referência **complementa — não substitui** — as 40 regras de redação e formatação da skill `documento-oficial-ses-to`. Aplique aquelas regras ao *como escrever*; aplique estes critérios ao *o que cobrir* em matéria de segurança e proteção de dados.

---

## Como usar esta referência

- **Cubra os critérios pertinentes** ao tipo de documento. Não force os inaplicáveis; quando omitir um critério relevante, **justifique brevemente** a omissão (instrução processual).
- **Confirme toda norma na Bibliografia**, sempre na **versão vigente**. Consulte as subpastas de legislação federal, as leis estaduais do TO, as normas regulatórias e o `Catalogo_Acervo_ABNT.xlsx`. **Nunca cite de memória.** Em conflito de normas, resolva pela **antinomia** (critérios hierárquico, cronológico e da especialidade — LINDB) e aplique a **mais atual/protetiva**.
- **Proteção reforçada** para **dados pessoais sensíveis de saúde**, **prontuários eletrônicos** e **serviços assistenciais críticos**.
- **Reaproveite os instrumentos já previstos na skill**: a **matriz de riscos**, o ciclo **PDCA** e os **quadros (`tabela`)**. **Ancore cada controle na base legal** — todo controle proposto deve remeter a uma norma confirmada (instrução processual).

---

## Base normativa típica (a confirmar na Bibliografia)

| Norma | Objeto |
|---|---|
| ABNT NBR ISO/IEC 27001:2022 | Sistema de Gestão de Segurança da Informação (SGSI) |
| ABNT NBR ISO/IEC 27002 | Controles de segurança da informação |
| ISO 27799 | Gestão de segurança da informação em saúde (informática em saúde) |
| ISO 31000:2018 | Gestão de riscos |
| LGPD — Lei nº 13.709/2018 | Proteção de dados pessoais (esp. arts. 7º, 11, 41, 46, 48) |
| Decreto Estadual nº 6.547/2022 (TO) | Regulamentação estadual de proteção de dados |
| LAI — Lei nº 12.527/2011 | Acesso à informação |
| Lei nº 14.133/2021 | Licitações e contratos (segurança desde o planejamento) |
| RNDS / Estratégia de Saúde Digital para o Brasil | Interoperabilidade e saúde digital |

> Confirme edição, ano e vigência de **cada** item acima antes de citar. Normas ABNT devem ser conferidas no `Catalogo_Acervo_ABNT.xlsx`.

---

## Critérios

### 1. Atributos e princípios
- **Atributos de segurança:** confidencialidade, integridade, disponibilidade, **autenticidade**, **não repúdio** e **responsabilização (accountability)**.
- **Princípios de proteção de dados:** legalidade, privacidade, **minimização / finalidade / necessidade**, **sigilo profissional em saúde**, transparência e **segurança e privacidade desde a concepção e por padrão** (*security & privacy by design and by default*).

### 2. SGSI e melhoria contínua
- Ciclo **PDCA** (ISO 27001:2022): Planejar → Executar → Verificar → Agir.
- **Objetivos e indicadores** de segurança definidos e medidos.
- **Análise crítica pela alta administração** em intervalos definidos.
- **Declaração de Aplicabilidade (SoA)** revista a cada mudança relevante.

### 3. Gestão de riscos
- Processo conforme **ISO 31000**: estabelecimento de contexto → identificação → análise → avaliação → tratamento → monitoramento → comunicação.
- **Opções de tratamento:** mitigar, transferir, evitar ou reter.
- **Risco residual** registrado e **aceito formalmente** pela autoridade competente.
- **Apresente em matriz/quadro** (reutilizar a matriz de riscos da skill).

**Modelo de matriz de riscos (`tabela`):**

| # | Ativo / Processo | Ameaça / Vulnerabilidade | Prob. | Impacto | Nível | Tratamento | Controle (base legal) | Risco residual | Aceite |
|---|---|---|---|---|---|---|---|---|---|
| R1 | Prontuário eletrônico | Acesso indevido | Média | Alto | Alto | Mitigar | Controle de acesso + MFA (LGPD art. 46) | Baixo | *Autoridade / data* |

### 4. Gestão de ativos e classificação
- **Inventário de ativos** com responsáveis identificados.
- **Classificação da informação:** *pública, interna, restrita, sigilosa*.
- Regras de **rotulagem, manuseio, transmissão e descarte** por classe.
- **Descarte irrecuperável** de dados sensíveis, **documentado**.

**Classes de informação (`tabela`):**

| Classe | Definição | Manuseio / transmissão | Descarte |
|---|---|---|---|
| Pública | Divulgação livre | Sem restrição | Comum |
| Interna | Uso interno | Canais institucionais | Comum controlado |
| Restrita | Acesso limitado por função | Cifrada; need-to-know | Seguro |
| Sigilosa | Sensível/legalmente protegida | Cifrada + autenticada | **Irrecuperável, documentado** |

### 5. Controle de acesso
- **Menor privilégio** e **need-to-know**.
- **Prontuários e dados sensíveis** restritos a quem presta o cuidado ou é **legalmente autorizado**.
- **Concessão, revisão e revogação formais**; **revogação imediata** em desligamento, afastamento ou mudança de função.
- **Vedação de compartilhamento de credenciais.**
- **MFA** para sistemas com dados sensíveis.
- **Acessos auditados** (ver critério 9).

### 6. Proteção criptográfica
- **Criptografia proporcional à criticidade**, **em repouso e em trânsito**.
- **Gestão segura de chaves** (geração, guarda, rotação, revogação).
- **Canais cifrados e autenticados** em toda comunicação de saúde, **inclusive RNDS e telessaúde**.

### 7. Segurança física e ambiental
- Proteção de **instalações, equipamentos e ambientes** que armazenem/processem dados de saúde.
- **Controle de entrada**, monitoramento e **infraestrutura de apoio** (energia, climatização, prevenção/combate a incêndio).

### 8. Operações e comunicações
- **Rotinas documentadas** de operação.
- **Backup testado**; **logs protegidos**; **gestão de vulnerabilidades/patches**; **antimalware**.
- **Rede** com **segmentação, perímetro, monitoramento e IDS/IPS**.

### 9. Registro de auditoria (trilhas)
Registrar **eventos relevantes**, com reforço em **prontuários e dados sensíveis**.

**Conteúdo mínimo do registro (`tabela`):**

| Campo | Descrição |
|---|---|
| Identificação | Usuário, serviço ou processo |
| Data e hora | Precisas e **sincronizadas** |
| Tipo de ação | Acesso, consulta, inclusão, alteração, exclusão, exportação, **tentativa**, **falha** |
| Recurso / dado | Recurso ou dado afetado |
| Origem | Endereço/origem da ação |
| Resultado | Sucesso ou falha |

Requisitos adicionais:
- **Sincronização de relógio** entre sistemas.
- **Integridade dos logs** contra alteração/exclusão — **inclusive por usuários privilegiados**.
- **Segregação de funções.**
- **Retenção** conforme prazos legais.
- **Correlação/SIEM** retroalimentando a gestão de **incidentes** e **riscos**.
- **Minimização** e **disponibilização apenas no limite legal**.

### 10. Uso aceitável, mobilidade e trabalho remoto
- Recursos institucionais para **fins institucionais**.
- Acesso **remoto/móvel/telessaúde** com **cifragem** e **autenticação reforçada**.
- **Vedação de armazenamento local não autorizado** de dados sensíveis.

### 11. Aquisições, desenvolvimento e fornecedores/operadores
- **Requisitos de segurança desde o planejamento** (Lei nº 14.133/2021).
- **Security/privacy by design.**
- **Contratos com cláusulas de operador:** finalidade, limites, sigilo, segurança, **notificação de incidentes**, auditoria, subcontratação, **eliminação/devolução** dos dados.
- **Avaliação prévia e monitoramento** dos operadores.

### 12. Gestão de incidentes e violação de dados
- Ciclo: **identificação → registro → classificação → contenção → tratamento → resposta → recuperação**, conduzido pela **ETIR** sob **supervisão técnica do CDO**.
- **Dever de reporte imediato.**
- **Notificação à ANPD e aos titulares** (**art. 48 da LGPD**) por meio do **Encarregado (DPO)** quando houver **risco ou dano relevante**.
- **Causa-raiz** e medidas de **não recorrência**.

### 13. Continuidade de negócio
- **Planos de continuidade e recuperação** com **RTO/RPO** definidos.
- **Testes periódicos**, assegurando resiliência dos **processos críticos e do cuidado**.

### 14. Proteção de dados pessoais e sensíveis de saúde
- **Bases legais e princípios** da LGPD; dados **sensíveis** fundados no **art. 11**.
- **Inventário / ROPA** e **RIPD** para tratamentos de **alto risco**.
- **Ciclo de vida** com **retenção e eliminação segura** (ressalvada a **guarda do prontuário**).
- **Direitos dos titulares** assegurados com apoio do **DPO**.

### 15. Interoperabilidade, RNDS e saúde digital
- Compartilhamento com **segurança, minimização, autenticação, rastreabilidade e cifragem**.
- Observância dos **padrões nacionais de interoperabilidade**.

### 16. Transparência x sigilo
- Conciliar a **LAI** com a **proteção de dados** e o **sigilo em saúde**.
- **Anonimização/pseudonimização** na divulgação.
- **Vedada a exposição de dados sensíveis** fora das hipóteses legais.

### 17. Conscientização e capacitação
- **Programas contínuos por função**, com ênfase em **dados sensíveis** e **resposta a incidentes**.

### 18. Monitoramento, auditoria e conformidade
- **Monitoramento contínuo**, **auditorias internas** e **avaliação de conformidade** do SGSI.
- **Planos de ação** acompanhados até a conclusão.

### 19. Violações e sanções
- Descumprimento sujeito às **sanções do estatuto funcional** e demais medidas cabíveis, além de **responsabilidades contratuais**.
- **Tentativa de burla** tratada como violação.

---

## Governança de referência (SES/TO)

> Confirme cargos, colegiados e atos **vigentes** na Bibliografia **antes de citar**.

| Instância | Papel |
|---|---|
| **CESD/SES-TO** | Colegiado máximo de segurança e dados |
| **Câmara Técnica de Segurança, Privacidade e Inovação em Saúde Digital** | Instância técnica |
| **CDO — Autoridade Técnica em Dados** (Coordenador do CIEGES-TO) | Autoridade técnica em dados |
| **ETIR** | Equipe de tratamento e resposta a incidentes |
| **Encarregado (DPO)** | Vinculado ao DPO central da **CGE/TO** |
| **Superintendentes** | Gestores de dados (*data owners*) |
| **ATI** | Custodiante |

---

## Especificidades por classe de documento

### Ato normativo de segurança (POSIN e anexos)
- **Políticas específicas como anexos** de **igual força normativa** (numeração reiniciada por anexo).
- Hierarquia: **política → normas → procedimentos**.
- **Regra de conflito:** prevalece a disposição **mais protetiva ao titular/à segurança**.
- **Revisão periódica** e cláusula de **vigência**.

### TR / contrato de TIC
- **Segurança desde o planejamento** (Lei nº 14.133/2021) + **cláusulas de operador** quando houver **tratamento por terceiros**.

### Plano de saúde digital
- **Segurança e privacidade *by design/by default*** como **requisito transversal** do **marco lógico**, dos **indicadores** e da **matriz de riscos**.

---

## Checklist final

- [ ] Atributos (CID + autenticidade / não repúdio / accountability) e princípios tratados.
- [ ] SGSI (PDCA), Declaração de Aplicabilidade e gestão de riscos (ISO 31000) presentes.
- [ ] Classificação da informação e descarte seguro definidos.
- [ ] Menor privilégio, MFA para dados sensíveis e revogação imediata previstos.
- [ ] Criptografia em repouso e em trânsito + gestão de chaves.
- [ ] Trilhas de auditoria com conteúdo mínimo, integridade, segregação e sincronização de tempo.
- [ ] Incidentes: ETIR, reporte, notificação ANPD/titulares (art. 48 LGPD), causa-raiz.
- [ ] Continuidade com RTO/RPO e testes.
- [ ] LGPD: bases legais (arts. 7º/11), ROPA, RIPD, direitos dos titulares, ciclo de vida.
- [ ] Interoperabilidade/RNDS com rastreabilidade e cifragem; LAI conciliada com sigilo.
- [ ] Todas as normas confirmadas na Bibliografia (versão vigente); **nada citado de memória**.
