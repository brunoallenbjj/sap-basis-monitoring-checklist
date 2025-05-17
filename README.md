# 📊 SAP Environment Monitoring - Checklist  

![SAP](https://img.shields.io/badge/SAP-0FAAFF?style=for-the-badge&logo=sap&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

> **Documentação interativa** para monitoramento de ambientes SAP (DEV, QAS, PRD).  

---

## 📌 Objetivo  
Garantir a estabilidade, segurança e desempenho de sistemas SAP através de monitoramento proativo.  

✅ **Estabilidade do Sistema**  
✅ **Segurança e Compliance**  
✅ **Otimização de Recursos**  
✅ **Gestão de Erros e Alertas**  

---

## 🔍 Transações de Monitoramento  

Clique em cada seção para expandir:  

<details>
<summary><b>ST22 - DUMP Analysis</b></summary>

### 📋 Visão Geral  
Exibe dumps de erro (ABAP runtime errors).  

### 🎯 Valores de Referência  
- **Dumps críticos**: ≤ 5 por dia (por ambiente)  
- *Ambiente DEV*: ≤ 10 (durante desenvolvimento)  

### 🛠 Monitoramento Recomendado  
- Verificar **diariamente** dumps críticos.  
- Configurar alertas via **CCMS (RZ20)**.  
- Ações: Corrigir programas com falhas recorrentes.  

### ⚠️ Riscos  
- Dumps não tratados podem causar instabilidade.  

</details>

<details>
<summary><b>SM37 - Job Monitor</b></summary>

### 📋 Visão Geral  
Monitora jobs em execução/histórico.  

### 🎯 Valores de Referência  
- **Jobs críticos**: 0% de falha  
- **Jobs não-críticos**: ≤ 5% de falha  

### 🛠 Monitoramento Recomendado  
- Filtrar jobs **cancelados/erros**.  
- Verificar **long-running jobs** (> 2 horas).  
- Ações: Reagendar jobs falhos.  

### ⚠️ Riscos  
- Jobs críticos parados impactam processos.  

</details>

<details>
<summary><b>SM58 - Transactional RFC</b></summary>

### 📋 Visão Geral  
Monitora erros de comunicação entre sistemas SAP (RFCs).  

### 🎯 Valores de Referência  
- **RFCs com erro**: 0  
- **RFCs "In Process"**: ≤ 1 hora de duração  

### 🛠 Monitoramento Recomendado  
- Verificar filas com status **"Error"**.  
- Ações: Reprocessar RFCs pendentes ou reiniciar conexões.  

### ⚠️ Riscos  
- RFCs travados podem paralisar integrações.  

</details>

<details>
<summary><b>SM12 - Table Locks</b></summary>

### 📋 Visão Geral  
Lista bloqueios de tabela no sistema.  

### 🎯 Valores de Referência  
- **Locks prolongados**: 0 (> 15 minutos)  

### 🛠 Monitoramento Recomendado  
- Identificar bloqueios com mais de **15 minutos**.  
- Ações: Contatar usuário ou encerrar bloqueios manualmente.  

### ⚠️ Riscos  
- Deadlocks podem afetar desempenho.  

</details>

<details>
<summary><b>SM13 - Update Records</b></summary>

### 📋 Visão Geral  
Monitora registros de atualização (V1/V2).  

### 🎯 Valores de Referência  
- **Updates falhos**: 0%  

### 🛠 Monitoramento Recomendado  
- Verificar updates com status **"Failed"**.  
- Ações: Reprocessar manualmente ou analisar logs.  

### ⚠️ Riscos  
- Updates não processados corrompem dados.  

</details>

<details>
<summary><b>SMLG - Load Balancing</b></summary>

### 📋 Visão Geral  
Gerencia distribuição de carga entre servidores.  

### 🎯 Valores de Referência  
- **Desequilíbrio de carga**: < 10% entre servidores  

### 🛠 Monitoramento Recomendado  
- Verificar **overload** em servidores específicos.  
- Ações: Ajustar parâmetros de balanceamento.  

### ⚠️ Riscos  
- Desbalanceamento causa lentidão.  

</details>

<details>
<summary><b>SMGW - Gateway Monitor</b></summary>

### 📋 Visão Geral  
Monitora conexões do SAP Gateway.  

### 🎯 Valores de Referência  
- **Threads ocupadas**: < 90% de utilização  

### 🛠 Monitoramento Recomendado  
- Verificar **threads ocupadas**.  
- Ações: Reiniciar serviço se necessário.  

### ⚠️ Riscos  
- Gateway inativo impede comunicações externas.  

</details>

<details>
<summary><b>DB02 - Database Monitor</b></summary>

### 📋 Visão Geral  
Monitora saúde do banco de dados SAP.  

### 🎯 Valores de Referência  
- **Espaço em disco**: ≥ 20% livre  
- *Alerta crítico*: < 10% livre  

### 🛠 Monitoramento Recomendado  
- Checar alertas de **espaço em disco**.  
- Verificar status de **backups**.  

### ⚠️ Riscos  
- Falha no banco paralisa o sistema.  

</details>

<details>
<summary><b>SCC4 - Client Control</b></summary>

### 📋 Visão Geral  
Controla acessos a clientes SAP.  

### 🎯 Valores de Referência  
- **Mudanças não autorizadas**: 0  

### 🛠 Monitoramento Recomendado  
- Auditar **mudanças não autorizadas**.  
- Ações: Bloquear clientes em manutenção.  

### ⚠️ Riscos  
- Acessos indevidos violam compliance.  

</details>

<details>
<summary><b>SM20 - Security Audit Log</b></summary>

### 📋 Visão Geral  
Registra atividades de segurança.  

### 🎯 Valores de Referência  
- **Tentativas de login inválidas**: ≤ 5 por hora (por usuário)  
- *Alerta de ataque*: > 10 tentativas  

### 🛠 Monitoramento Recomendado  
- Buscar por **tentativas de login suspeitas**.  
- Ações: Reportar a equipe de segurança.  

### ⚠️ Riscos  
- Brechas de segurança não detectadas.  

</details>

<details>
<summary><b>SUIM - User Analysis</b></summary>

### 📋 Visão Geral  
Audita usuários e permissões.  

### 🎯 Valores de Referência  
- **Usuários inativos (>45 dias)**: 0 em PRD  
- **Usuários com SAP_ALL**: ≤ 5 (apenas administradores)  

### 🛠 Monitoramento Recomendado  
- Identificar usuários **inativos >45 dias**.  
- Checar atribuição de **SAP_ALL**.  

### ⚠️ Riscos  
- Privilégios excessivos aumentam riscos.  

</details>

<details>
<summary><b>STRUST - SSL Certificates</b></summary>

### 📋 Visão Geral  
Gerencia certificados digitais.  

### 🎯 Valores de Referência  
- **Certificados expirados**: 0  

### 🛠 Monitoramento Recomendado  
- Verificar **validade de certificados**.  
- Ações: Renovar antes da expiração.  

### ⚠️ Riscos  
- Certificados expirados quebram conexões.  

</details>


## 🚀 Como Contribuir  
1. Faça um **fork** do repositório.  
2. Adicione melhorias (ex: novas transações, scripts).  
3. Envie um **Pull Request**.  

📜 **Licença:** MIT  

<div align="center">
  <sub>Criado para operações SAP Basis mais eficientes e descomplicadas ;)</sub>  
</div>
