# Documento de Levantamento de Requisitos — SafeField AI

## 1. Visão geral

O SafeField AI é uma solução de segurança industrial proativa para o ambiente Metaindústria. O sistema monitora operadores em campo, identifica uso incorreto ou ausência de EPIs, registra eventos de risco e notifica supervisores em tempo real.

## 2. Personas

### Persona 1 — Operador de Chão de Fábrica

- Nome fictício: Carlos Mendes
- Idade: 34 anos
- Perfil: trabalha em linha de produção e executa atividades próximas a máquinas e áreas de risco.
- Necessidade: receber orientação rápida quando estiver exposto a risco ou sem EPI obrigatório.
- Dor: nem sempre percebe que está em situação irregular ou próxima de uma área perigosa.

### Persona 2 — Supervisora de Segurança

- Nome fictício: Mariana Costa
- Idade: 41 anos
- Perfil: acompanha conformidade de segurança, fiscaliza setores e responde a incidentes.
- Necessidade: receber alertas em tempo real para agir antes de um acidente.
- Dor: não consegue acompanhar todos os operadores manualmente o tempo todo.

### Persona 3 — Gestor Industrial

- Nome fictício: Roberto Lima
- Idade: 48 anos
- Perfil: responsável por indicadores operacionais e segurança da planta.
- Necessidade: visualizar relatórios de conformidade, setores críticos e evolução dos riscos.
- Dor: falta de dados consolidados para tomada de decisão preventiva.

## 3. Requisitos funcionais

| Código | Requisito funcional | Prioridade |
|---|---|---|
| RF01 | O sistema deve permitir cadastrar operadores com nome, matrícula, setor e função. | Alta |
| RF02 | O sistema deve permitir cadastrar setores industriais monitorados. | Alta |
| RF03 | O sistema deve permitir cadastrar EPIs obrigatórios por setor ou função. | Alta |
| RF04 | O sistema deve receber imagens ou frames de câmeras de monitoramento. | Alta |
| RF05 | O sistema deve identificar automaticamente a presença ou ausência de EPIs obrigatórios. | Alta |
| RF06 | O sistema deve registrar evento de risco quando detectar ausência de EPI obrigatório. | Alta |
| RF07 | O sistema deve gerar alerta em tempo real para o supervisor responsável. | Alta |
| RF08 | O supervisor deve poder visualizar alertas pendentes em um dashboard. | Alta |
| RF09 | O supervisor deve poder validar, comentar e encerrar um alerta. | Média |
| RF10 | O sistema deve armazenar histórico de eventos de risco. | Alta |
| RF11 | O gestor deve poder gerar relatório de conformidade por período, setor e operador. | Alta |
| RF12 | O sistema deve exibir indicadores de segurança, como total de alertas, reincidências e percentual de conformidade. | Média |
| RF13 | O sistema deve permitir classificar o nível de risco do evento como baixo, médio ou alto. | Média |
| RF14 | O sistema deve registrar data, horário, setor, operador e tipo de risco identificado. | Alta |
| RF15 | O sistema deve permitir configurar câmeras vinculadas a setores industriais. | Média |

## 4. Requisitos não funcionais

| Código | Requisito não funcional | Categoria | Prioridade |
|---|---|---|---|
| RNF01 | O sistema deve processar detecções com baixa latência para permitir resposta em tempo real. | Desempenho | Alta |
| RNF02 | O sistema deve manter disponibilidade adequada para operação durante turnos industriais. | Disponibilidade | Alta |
| RNF03 | O sistema deve registrar logs de eventos e falhas para auditoria. | Auditoria | Alta |
| RNF04 | A interface deve ser simples e objetiva para uso em ambiente operacional. | Usabilidade | Alta |
| RNF05 | O sistema deve permitir crescimento para novos setores, câmeras e tipos de EPI. | Escalabilidade | Média |
| RNF06 | O acesso ao dashboard deve exigir autenticação. | Segurança | Alta |
| RNF07 | Os dados dos operadores devem ser protegidos contra acesso não autorizado. | Segurança | Alta |
| RNF08 | O sistema deve permitir integração futura com sensores IoT e sistemas industriais. | Integração | Média |
| RNF09 | O sistema deve armazenar imagens somente quando necessário para evidência e auditoria. | Privacidade | Alta |
| RNF10 | O sistema deve ser executável em ambiente conteinerizado. | Portabilidade | Média |

## 5. Restrições do sistema

- O sistema depende de câmeras posicionadas corretamente no ambiente industrial.
- A qualidade da detecção pode ser afetada por iluminação, oclusão, baixa resolução ou ângulo inadequado.
- A solução deve apoiar a prevenção, mas não substitui procedimentos obrigatórios de segurança do trabalho.
- O reconhecimento deve priorizar EPIs e riscos operacionais, não identificação biométrica sensível.
- O ambiente industrial pode exigir processamento em borda para reduzir latência.
- O sistema deve respeitar políticas internas de privacidade, auditoria e segurança da informação.

## 6. Funcionalidade crítica escolhida para o Diagrama de Atividades

A funcionalidade crítica modelada é: **detecção de ausência de EPI e emissão de alerta de risco em tempo real**.

Esse fluxo foi escolhido porque representa o núcleo da proposta de segurança proativa: identificar o risco antes que o incidente ocorra e permitir ação imediata do supervisor.
