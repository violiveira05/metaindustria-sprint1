# SafeField AI — Segurança Proativa no Metaindústria

## Integrantes

| Nome | RM |
| Milena Queiroz  | 558825 |
| Nicolas Alvares | 557271 |
| Victor Augusto  | 558338 |
| Gabriel Yeshua  | 558273 |
| Pedro Henrique  | 558867 |

## Contexto do Challenge

O projeto está alinhado ao contexto do Metaindústria, iniciativa ligada à transformação digital da indústria brasileira, com foco em tecnologias 4.0, inteligência artificial, automação e validação de soluções aplicadas ao setor produtivo.

No ambiente industrial, a segurança do operador não pode depender apenas de fiscalização posterior ou punição após a infração. A proposta deste projeto é apoiar a transição para um modelo de segurança proativa, com monitoramento contínuo, identificação preventiva de riscos e geração de alertas em tempo real.

## Problema abordado

Em operações industriais, falhas no uso de Equipamentos de Proteção Individual, entrada em áreas restritas, postura inadequada e exposição a situações de risco podem gerar acidentes graves. Muitas empresas ainda tratam essas ocorrências de forma reativa, registrando infrações apenas depois que o risco já ocorreu.

O problema central é: **como apoiar operadores, supervisores e gestores industriais na identificação preventiva de riscos em campo, reduzindo a dependência de fiscalização manual e aumentando a cultura de prevenção?**

## Proposta de solução

O **SafeField AI** é uma aplicação operacional de segurança industrial que utiliza visão computacional, sensores e dashboard web para monitorar o uso correto de EPIs e situações de risco em tempo real.

A solução identifica se o operador está utilizando os EPIs obrigatórios, como capacete, luvas, colete e óculos de proteção, além de registrar eventos de risco, emitir alertas para o supervisor e gerar relatórios de conformidade para o gestor industrial.

## Escopo da Sprint 1

Nesta Sprint, o foco está na exploração do problema, levantamento de requisitos e modelagem da solução. Não há implementação completa do sistema, mas sim a documentação técnica necessária para orientar as próximas etapas.

## Atores principais

- **Operador de Chão de Fábrica:** profissional monitorado pela solução durante a execução das atividades.
- **Supervisor de Segurança:** responsável por acompanhar alertas, validar ocorrências e orientar operadores.
- **Gestor Industrial:** acompanha indicadores, relatórios e níveis de conformidade por setor.
- **Sistema de IA:** componente responsável por processar imagens/sensores e identificar riscos automaticamente.

## Funcionalidades previstas

- Cadastro de operadores, setores, câmeras e EPIs obrigatórios.
- Monitoramento do uso de EPIs por visão computacional.
- Registro automático de eventos de risco.
- Emissão de alertas em tempo real para o supervisor.
- Geração de relatório de conformidade por setor, operador e período.
- Dashboard com indicadores de segurança.

## Tecnologias selecionadas

| Tecnologia | Uso no projeto | Justificativa técnica |
|---|---|---|
| Python | Módulo de IA e visão computacional | Possui forte ecossistema para IA, OpenCV e modelos de detecção. |
| OpenCV | Processamento de imagem | Permite captura e análise de frames de câmeras industriais. |
| YOLO | Detecção de EPIs e pessoas | Modelo adequado para detecção de objetos em tempo real. |
| FastAPI | API backend | Framework leve, rápido e adequado para integração com serviços de IA. |
| PostgreSQL | Banco de dados | Confiável para armazenar operadores, eventos, alertas e relatórios. |
| React | Frontend dashboard | Facilita a criação de interfaces dinâmicas para monitoramento operacional. |
| WebSocket | Alertas em tempo real | Permite enviar notificações instantâneas ao dashboard do supervisor. |
| Docker | Empacotamento da solução | Facilita execução padronizada em ambiente local, nuvem ou borda industrial. |

## Justificativa técnica

A solução exige processamento em tempo real, confiabilidade e escalabilidade. Por isso, Python e YOLO são adequados para a camada de visão computacional, enquanto FastAPI permite expor os resultados da IA para o sistema web de forma eficiente. O PostgreSQL garante persistência estruturada dos registros de segurança. O React oferece uma interface clara para supervisores e gestores, e o WebSocket permite alertas imediatos, essenciais para uma abordagem preventiva.

## Estrutura do repositório

```text
safe-field-ai/
├── README.md
├── docs/
│   ├── requisitos.md
│   └── diagramas/
│       ├── casos-de-uso.puml
│       ├── atividades.puml
│       └── classes.puml
└── entrega.txt
```

## Documentação

- [Levantamento de Requisitos](docs/requisitos.md)
- [Diagrama de Casos de Uso](docs/diagramas/casos-de-uso.puml)
- [Diagrama de Atividades](docs/diagramas/atividades.puml)
- [Diagrama de Classes](docs/diagramas/classes.puml)

## Como visualizar os diagramas

Os diagramas foram escritos em PlantUML. Para visualizar, é possível usar:

- Extensão PlantUML no Visual Studio Code.
- Site PlantUML Online Server.
- Plugin PlantUML em IDEs compatíveis.
