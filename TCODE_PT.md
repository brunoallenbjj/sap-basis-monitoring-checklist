**Monitoramento de Ambiente SAP - Checklist**  

**Visão Geral**  
Este documento descreve as transações e o modelo utilizados para gerenciar e controlar o monitoramento de ambientes SAP, incluindo ambientes DEV, QAS ou PRD.  

**Objetivo**  
- Estabilidade do Sistema  
- Desempenho  
- Segurança  
- Gerenciamento de Erros  
- Planejamento e Controle  
- Conformidade e Auditoria  
- Otimização de Recursos  

**Transações Utilizadas no Monitoramento**  

**ST22 - DUMP**  

**Visão Geral:** Exibe dumps de erro no sistema.  

**Monitoramento:** Verificar regularmente dumps de erro para identificar problemas no sistema. Configurar alertas para notificar sobre novos dumps.  

**SM37 - JOB**  

**Visão Geral:** Mostra jobs em execução e histórico de execução.  

**Monitoramento:** Verificar jobs ativos e histórico para garantir que estão sendo executados conforme esperado. Monitorar tempos de execução e possíveis falhas.  

**SM58 - RFC TRANSACIONAL**  

**Visão Geral:** Exibe mensagens de erro de comunicação entre sistemas SAP.  

**Monitoramento:** Verificar erros de comunicação entre sistemas SAP. Monitorar a fila SM58 para mensagens pendentes.  

**SM12 - BLOQUEIOS E DESBLOQUEIOS DE TABELA**  

**Visão Geral:** Exibe bloqueios de tabela no sistema.  

**Monitoramento:** Verificar bloqueios ativos e resolver bloqueios prolongados que possam afetar o desempenho.  

**SM13 - ADMINISTRAÇÃO DE REGISTROS DE ATUALIZAÇÃO**  

**Visão Geral:** Monitora e administra registros de atualização.  

**Monitoramento:** Garantir que os registros de atualização estão sendo processados corretamente e que não há atrasos nas atualizações.  

**SMLG - DISTRIBUIÇÃO DE CARGA**  

**Visão Geral:** Gerencia a distribuição de carga entre servidores.  

**Monitoramento:** Monitorar o balanceamento de carga para evitar sobrecarga em servidores específicos.  

**SMGW - MONITOR DE GATEWAY**  

**Visão Geral:** Monitora o estado do gateway.  

**Monitoramento:** Verificar a disponibilidade e saúde do gateway para garantir conectividade.  

**DB02 - Visão Geral, Alertas, Backup, Automonitoramento**  

**Visão Geral:** Monitora o banco de dados SAP.  

**Monitoramento:** Verificar métricas de desempenho, alertas, status de backup e saúde do banco de dados. Garantir que o monitoramento interno do banco de dados está ativo.  

**SCC4 - ABERTURA DE AMBIENTE**  

**Visão Geral:** Controla a abertura do ambiente.  

**Monitoramento:** Verificar se as configurações do ambiente estão corretas e se houve alterações não autorizadas.  

**SM20 - ANÁLISE DE LOG DE AUDITORIA DE SEGURANÇA**  

**Visão Geral:** Registra atividades de segurança no sistema.  

**Monitoramento:** Analisar logs para detectar atividades suspeitas ou não autorizadas.  

**SUIM - Extração de usuários inativos há 45 dias, Usuários com SAP_ALL**  

**Visão Geral:** Analisa usuários inativos e usuários com privilégios elevados.  

**Monitoramento:** Verificar usuários inativos e identificar possíveis problemas de segurança relacionados a privilégios elevados.  

**STRUST**  

**Visão Geral:** Configura relações de confiança para comunicação segura.  

**Monitoramento:** Garantir que as configurações de confiança estão corretas e que não houve alterações não autorizadas.
