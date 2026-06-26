# 🧪 Test Report — https://punchgamebr.com/

> **Projeto:** Testes Manuais de Interface e Usabilidade  
> **Site testado:** https://punchgamebr.com/
> **Tipo de teste:** Manual + Performance  
> **Status geral:** ⚠️ Falhas Críticas Identificadas

---

## 📋 Sumário Executivo

Este relatório documenta os defeitos encontrados durante a execução de testes manuais no site **punchgamebr.com**. Foram feitos 25 testes cobrindo a página inicial, Navegação e Menu, cadastro de usuário e embaixadores. Todos os casos de teste estão disponiveis na [Planilha de Testes](https://docs.google.com/spreadsheets/d/1Lf0s7QaXpJXEDnToFwi2ALe7-HFXftOH9ahpNZNVESM/edit?usp=sharing). 

| Métrica | Valor |
|---|---|
| Total de casos com falha documentados | 6 |
| Severidade Alta | 3 |
| Severidade Média | 2 |
| Severidade Baixa | 1 |

---

## 🐛 Defeitos Encontrados

### CT-003 — Botão dos patrocinadores oficiais 

| Campo | Detalhe |
|---|---|
| **ID** | CT-003 |
| **Módulo** | Botão / Hiperlink |
| **Severidade** | 🟢 Baixa |
| **Ambiente** | Desktop |

**Descrição:**  
O link vinculado ao patrocinador "Batalha da Norte" é de uma página diferente.

**Resultado Esperado:** .  Clicar no ícone da "Batalha da Norte" te leva ao instagram da Batalha da Norte-SP.
**Resultado Obtido:** Clicar no ícone da "Batalha da Norte" te leva para o instagram da Batalha da Norte-TO.

---

### CT-016 — Cadastro com telefone inválido

| Campo | Detalhe |
|---|---|
| **ID** | CT-016 |
| **Módulo** | Cadastro / Segurança |
| **Severidade** | 🟠 Alta |
| **Ambiente** | Desktop |

**Descrição:**  
Ao inserir um telefone inválido o sistema não acusa erro e permite a criação do usuário.

**Resultado Esperado:** Acesso negado com mensagem informativa de telefone inválido. 
**Resultado Obtido:** Usuário criado com um número de telefone inexistente.

---

### CT-024 — Cadastro com CPF já utilizado: duplicidade permitida

| Campo | Detalhe |
|---|---|
| **ID** | CT-024 |
| **Módulo** | Cadastro / Autenticação |
| **Severidade** | 🔴 Alta |
| **Ambiente** | Desktop |

**Descrição:**  
O sistema permite que o mesmo CPF seja cadastrado em duas contas diferentes, sem emitir qualquer alerta ou impedimento. Isso representa uma falha de integridade de dados e pode viabilizar fraudes ou duplicação de identidade na plataforma.

**Resultado Esperado:** O sistema deve validar o CPF no momento do cadastro e impedir o registro caso ele já esteja vinculado a outra conta.  
**Resultado Obtido:** Cadastro concluído com sucesso utilizando um CPF já associado a outra conta existente.

---

### CT-017 — Validação do campo "Nome" muito fraca

| Campo | Detalhe |
|---|---|
| **ID** | CT-017 |
| **Módulo** | Cadastro / Autenticação |
| **Severidade** | 🔴 Alta |
| **Ambiente** | Desktop |

**Descrição:**  
O sistema não apresenta uma limitação de quantidade de caracteres ou de uso de caracteres especiais para o Nome do usuário, permitindo a criação com nomes extensos e com qualquer tipo de caractere.

**Resultado Esperado:** O sistema deve ter um limite de caracteres e impedir o uso de caracteres especiais no campo "Nome".
**Resultado Obtido:** Cadastro concluído com sucesso utilizando um nome como: L2@!OPSJKAMS216@!!&#)!*#@_KANDASDNASYHDUQ

---

*Relatório gerado para fins de portfólio — Testes executados manualmente, sem automação.*
