# Configuração e Gerenciamento de Monitoramento de VMs no Azure

## 📁 Descrição do Laboratório

Este repositório documenta um laboratório prático com foco na **configuração e gerenciamento do monitoramento de recursos no Azure**, especialmente **Máquinas Virtuais (VMs)**. O objetivo é manter visibilidade, controle e ação proativa diante de eventos críticos, como a exclusão acidental ou não autorizada de uma VM.

---

## 📚 Objetivos de Aprendizagem

* Configurar recursos de **monitoramento e alerta** para VMs no Azure.
* Visualizar logs e eventos relevantes para auditoria e diagnóstico.
* Automatizar a resposta a eventos críticos.
* Criar documentação clara e reutilizável para estudos futuros.

---

## ⚙️ Etapas do Laboratório (Passo a Passo)

### Visão Geral:

A necessidade de monitorar servidores em nuvem é crítica para garantir alta disponibilidade, performance e segurança. Neste laboratório, será realizada a implantação de uma infraestrutura de teste com VM, seguida pela configuração de monitoramento e alertas no Azure.

### 1. **Deploy da infraestrutura inicial**

* Acesse o portal do Azure.
* Utilize um **modelo (template ARM)** ou crie manualmente uma máquina virtual.
* Nomeie e categorize os recursos (grupo de recursos, rede, etc.).

### 2. **Configurar Azure Monitor**

* Acesse a seção **Monitor** no portal.
* Ative o diagnóstico na VM, associando-a a um **Log Analytics Workspace**.
* Certifique-se de que métricas e logs estão sendo coletados corretamente.

### 3. **Criar Alertas**

* Vá para "Monitor > Alertas > Regras de Alerta".
* Configure uma regra baseada em **atividade** (ex.: exclusão de VM) ou **métrica** (uso de CPU, memória, etc.).
* Defina condições de severidade e frequência.

### 4. **Criar Grupos de Ação (Notificações)**

* Crie ou associe um **Grupo de Ação** com notificações via:

  * E-mail
  * SMS
  * Webhook
  * App móvel (Azure App)
* Relacione o grupo de ação à sua regra de alerta.

### 5. **Testar os Alertas**

* Simule a condição da regra (ex.: uso elevado de CPU ou exclusão planejada da VM).
* Verifique se a notificação foi disparada corretamente.
* Revise logs no **Activity Log** e **Log Analytics**.

### 6. **Consultas com Azure Monitor (Log Analytics / KQL)**

* Acesse "Monitor > Logs".
* Execute consultas com linguagem **KQL** (Kusto Query Language):

  * Verificar quem excluiu a VM.
  * Listar reinicializações de sistema.
  * Identificar falhas recorrentes.

### 7. **Criação de Dashboard Personalizado**

* Acesse "Dashboard" no portal.
* Adicione gráficos e indicadores de:

  * Uso de CPU/memória
  * Alertas ativos
  * Estado da VM

---

## 📑 Recursos Adicionais

* [Documentação oficial - Monitoramento de VMs no Azure](https://learn.microsoft.com/pt-br/azure/azure-monitor/vm/monitor-virtual-machine)
* [Azure Monitor Overview](https://learn.microsoft.com/pt-br/azure/azure-monitor/overview)
* [Log Analytics e KQL](https://learn.microsoft.com/pt-br/azure/azure-monitor/logs/log-analytics-overview)

---

## 💡 Dicas Práticas

* Use nomes padronizados para grupos de ação e regras de alerta.
* Combine alertas de métrica (CPU, RAM) com alertas de log (eventos).
* Programe auditorias regulares via dashboard e Log Analytics.
* Teste os alertas antes de colocar em produção!

---

## 🚀 Conclusão

Este laboratório mostra como implementar um monitoramento robusto para VMs no Azure, usando ferramentas nativas como **Azure Monitor**, **Log Analytics** e **Alertas Proativos**. Uma abordagem essencial para qualquer ambiente de produção moderno baseado em nuvem.

---

> Repositório criado como parte do desafio da plataforma educacional. Contribuições e melhorias são bem-vindas!
