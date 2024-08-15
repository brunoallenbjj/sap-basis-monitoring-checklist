# sapchecklist

Monitoramento de ambientes SAP - Checklist.

 

 

# Visão Geral 

 

Esta documentação descreve as transações e modelo utilizado para gerenciar e controlar o monitoramento dos ambientes SAP, que é feito pela consultoria NUMEN IT SOLUCOES EM TECNOLOGIA LTDA e enviado com a periodicidade SEMANAL via e-mail ao time de IT BUSINESS APPLICATION. 

 

 


# Objetivo 

Estabilidade do Sistema 

Performance

Segurança 

Gestão de Erros 

Planejamento e Controle 

Conformidade e Auditoria 

Otimização de Recursos  

# Transações utilizadas no monitoramento. 

 

ST22 - DUMP 

Visão geral: Exibe dumps de erro no sistema. 

Monitoramento: Verificar regularmente por dumps de erro para identificar problemas no sistema. Configurar alertas para notificar sobre novos dumps. 

 

SM37 - JOB 

Visão geral: Mostra os jobs em execução e histórico de execuções. 

Monitoramento: Verificar jobs ativos e histórico para garantir que estão sendo executados conforme o esperado. Monitorar tempos de execução e possíveis falhas. 

 

SM58 - RFC TRANSACIONAL 

Visão geral: Mostra as mensagens de erro de comunicação entre sistemas SAP. 

Monitoramento: Verificar erros de comunicação entre sistemas SAP. Monitorar a fila SM58 para mensagens pendentes. 

 

SM12 - BLOQUEIO E DESBLOQUEIO TABELAS 

Visão geral: Exibe bloqueios de tabelas no sistema. 

Monitoramento: Verificar bloqueios ativos e resolver bloqueios prolongados que possam afetar o desempenho. 

 

 

 

 

 

SM13 - ADMINISTRAR REGISTRO DE ATUALIZAÇÃO 

Visão geral: Monitora e administra registros de atualização. 

Monitoramento: Verificar se os registros de atualização estão sendo processados      corretamente e se não há atrasos nas atualizações. 

 

SMLG - DISTRIBUIÇÃO DE CARGA 

Visão geral: Gerencia a distribuição de carga entre servidores. 

Monitoramento: Monitorar o balanceamento de carga para evitar sobrecarga em servidores específicos. 

 

SMGW - GATEWAY MONITOR 

Visão geral: Monitora o estado do gateway. 

Monitoramento: Verificar a disponibilidade e saúde do gateway para garantir a conectividade. 

 

DB02 - Overview, Alerts, Backup, Self-Monitoring 

Visão geral: Monitora o banco de dados SAP. 

Monitoramento: Verificar métricas de desempenho, alertas, status do backup e saúde do banco de dados. Garantir que o monitoramento interno do banco de dados esteja ativo. 

 

SCC4 - ABERTURA DE AMBIENTE 

Visão geral: Controla a abertura do ambiente. 

Monitoramento: Verificar se as configurações de ambiente estão corretas e se não houve mudanças não autorizadas. 

 

SM20 - ANÁLISE DE LOG DE AUDITORIA DE SEGURANÇA 

Visão geral: Registra atividades de segurança no sistema. 

Monitoramento: Analisar logs para detectar atividades suspeitas ou não autorizadas. 

SUIM - Extração de usuários 45 dias sem logar, Usuários com SAP_ALL 

Visão geral: Analisa usuários inativos e usuários com privilégios elevados. 

Monitoramento: Verificar usuários inativos e identificar potenciais problemas de segurança relacionados a privilégios elevados. 

 

STRUST 

Visão geral: Configuração de trust relationships para comunicação segura. 

Monitoramento: Verificar se as configurações de trust estão corretas e se não houve alterações não autorizadas. 


