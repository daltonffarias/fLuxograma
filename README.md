# fLuxograma
Novo
https://www.mermaidchart.com/app/projects/ad597f61-2814-4c93-84fc-a8129a3e16c4/diagrams/a887c5b4-68c2-4bb5-a2b2-9df9f1055921/version/v0.1/edit

flowchart TD
    A["Início: Solicitação no Workflow"] --> B{"Verificar Pendências?"}
    B -- Não --> C["Processar Solicitação"]
    B -- Sim --> D["Corrigir Pendências"]
    D --> B
    C --> E["Emitir Ordem de Venda no Oracle"]
    E --> F{"Cliente cadastrado?"}
    F -- Não --> G["Solicitar Cadastro"]
    G --> E
    F -- Sim --> H["Definir Tributação e Itens"]
    H --> I{"Nota de SP?"}
    I -- Sim --> J["Gerar via Avalara"]
    I -- Não --> K["Gerar diretamente no Oracle"]
    J --> L["Monitorar Status e Gerar PDF"]
    K --> L
    L --> M{"Nota Avulsa?"}
    M -- Sim --> N["Emitir NFS-e na Prefeitura"]
    M -- Não --> O["Finalizar"]
    N --> O
    O --> P["Vincular Nota à Ordem"]
    P --> Q["Enviar PDF e Concluir"]
