title: Cadastrar uma mudança
Description: Tem por objetivo registrar uma mudança. 
# Cadastrar uma mudança 

Esta funcionalidade tem por objetivo registrar uma mudança. Segundo a ITIL, é necessário formalizar a solicitação de mudança, para que seja registrado pela equipe responsável todos os procedimentos realizados para a alteração desejada (desde a sua requisição ao impacto de sua implementação) monitorando o mesmo por todo o seu ciclo de vida.

Antes de começar
------------------

 Para efetivar o cadastro de uma mudança é preciso previamente cadastrar um contrato, uma unidade e que ela esteja vinculada ao contrato, um colaborador, um questionário, o Comitê Consultivo de Mudanças, ter um grupo vinculado ao contrato associado os Solicitantes (colaboradores) já cadastrados a este grupo. Caso seja preciso criar um novo colaborador, é necessário incluí-lo ao Grupo de Solicitante no qual esteja relacionado ao contrato.
Ademais, é fundamental o cadastro prévio do portfólio de mudanças.

Procedimento 
--------------

1.	Acessar a funcionalidade através da navegação no menu principal Processos > Gerência de Mudança > Mudança;
2.	Clicar no botão “Opções” e em seguida em “Cadastro”;
3.	Preencher todos os campos disponíveis:

### Solicitante

Para identificar o solicitante da mudança, complete os campos:

|Campos|Descrição|
|---|---|
|Nome (\*)|Nome completo do solicitante|
|Contato (\*)|Identificar o contato do usuário|
|E-mail (\*)|E-mail do usuário|
|Telefone|Número de telefone do usuário|
|Ramal|O número do ramal do usuário|
|Unidade (\*)|Unidade do usuário|
|Localidade Física|A localização física do usuário|
|Outras Informações|Informação adicional sobre o usuário|

(*) Indicar campos obrigatórios

### Mudança

Para identificar a mudança, preencha os campos:

|Campos|Descrição|
|---|---|
|Título (\*)|Título para identificar a mudança|
|Descrição da alteração (\*)|Descrição da mudança|
|Efeito de não implementar a mudança|Efeito caso a mudança não for implementada|
|Contrato|Contrato vinculado a mudança|
|Importância|O nível de importância da mudança. Apresenta as seguintes opções: **Importante** envolve uma quantidade significativa de preparação e trabalho com situações complexas ou grandes;**Significante** mudança significativa, mudanças significativas envolvem preparação e trabalho, avaliação, autorização e planejamento de mudanças. Exemplos: Compra e instalação de um novo servidor, Re-segmentação de rede;**Pequena** pode ser avaliado e autorizado fora da autoridade do CCM (por exemplo, por um coordenador).|
|Impacto|Impacto que a mudança gera, temos as opções: **Baixa**, **Média** e **Alta**.|
|Urgência|Urgência para realizar a mudança, temos as opções: **Baixa**, **Média** e **Alta**|
|Grupo Executor|O grupo responsável pela execução da mudança|
|Notificações|Definir as notificações entre "Enviar email ao criar a Mudança", "Enviar email ao finalizar a Mudança", "Enviar email para o comitê consultivo de mudança", "Enviar email para as demais ações da Mudança"|

(*) Indicar campos obrigatórios

!!! Abstract "NOTA"
    
        Para [Criar portfólio de mudança](/pt-br/4biz-helium/processes/change/configuration/change-portfolio.html)
        
### Anáise ágil de risco

Na área de análise de riscos, serão feitas três questões:

* Existe o risco de interromper serviços importantes? - com as opções de "Sim" ou "Não"

* Existe um risco de perda financeira? - com as opções "Sim" ou "Não"

* Existe um risco de imagem? - com as opções "Sim" ou "Não"

Será então apresentada uma representação do risco de 0 a 100.

### Planejamento

Para planejar a mudança, use as funcionalidades:

|Guia|Descrição|
|-|-|
|Atividades|Criar um workspace ou vincular um já existente|
|Datas|Data para planejar a mudança: no campo "Data prevista de início", a data de início do planejamento deve ser indicada. No campo "Data prevista de término", a data final do planejamento deve ser indicada. Depois de indicar a data de início e a data de término, você pode verificar os conflitos clicando em "Ver conflitos". Aprovação: "Data de aceitação" deve ser dada uma data para ser aceito, "Votação" deve ser dada uma data para votação, "Data de conclusão" deve ser dada uma data para a conclusão|
|Ações|Adicionar ações para a mudança|
|Notificações do sistema|Definir uma notificação do sistema para informá-lo da mudança|
|Documentos|Vincular conhecimento à mudança|
|Anexos|Inserir anexos à mudança|
|Anotações|Adicionar notas relevantes à mudança|

[Atividades da fase de planejamento da mudança](/pt-br/4biz-helium/processes/change/use/change-planning-activities.html)

5. Também é necessário indicar as informações preliminares de "planejamento", "plano de reversão" e "revisão e encerramento".

### Plano de reversão

Para planejar a reversão de mudanças, use os recursos:

|Guia|Descrição|
|-|-|
|Atividades | Criar um workspace ou vincular um já existente|
|Ações | Adicionar ações para a mudança|
|Notificações do sistema|Configure uma notificação do sistema para informá-lo sobre o plano de reversão de mudanças|
|Documentos|Vincular conhecimentos ao plano de reversão|
|Anexos|Inserir anexos para o plano de reversão|
|Anotações|Adicionar notas relevantes ao plano de reversão|

[Cadastrar plano de reversão da mudança](/pt-br/4biz-helium/processes/change/use/change-reversion-plan.html)

### Revisão e fechamento

Para revisar e encerrar a mudança, use os recursos:

|Guia|Descrição|
|-|-|
|Revisão|Informe ao Usuário final sobre análise de risco e impacto da mudança|
|Atividades|Criar um workspace ou vincular um já existente|
|Incidentes|Vincular um incidente para a revisão|
|Problemas|Vincular um problema para a revisão|
|Lições Aprendidas|Vincular conhecimento para o plano de reversão|
|Fechamento|Identificar o fechamento da mudança|
|Anexos|Inserir anexos|
|Anotações|Adicionar notas relevantes|

5. Click on "Options" and then on "Save”;

## Relacionamentos

### IC da mudança

Para vincular um item de configuração, selecione ICs relacionados > Pesquisar item de configuração e selecione o item de configuração.

[Relacionar itens à mudança](/pt-br/4biz-helium/processes/change/use/relate-information-to-change.html)

### Serviços da mudança    

Para vincular um Serviço para a Mudança, selecione Serviços Relacionados > Adicionar Serviço e selecione o serviço.

### Questionário

Não é obrigatório, mas algumas mudanças podem vir junto com um questionário. Pode ser usado para fazer uma pesquisa (avaliação), questionários podem ser respondidos e as respostas serão vinculadas à mudança. O questionário deve ser criado previamente.

### Papéis e responsabilidades

Para definir as funções e responsabilidades da mudança, preencha os campos:

|Campo|Descrição|
|-|-|
|Colaborador|Nome do usuário|
|Papel|Papel que o usuário irá desempenhar|
|Responsabilidades|Selecionar a responsabilidade que será vinculada ao usuário|

### Votação RDM

A equipe de mudança pode visualizar a pontuação de votação para aprovação da mudança.

[Aprovar mudança](/pt-br/4biz-helium/processes/change/use/change-approval.html)

### Liberação

Para vincular uma liberação a uma mudança, procure um existente em "Pesquisar por título" ou crie uma nova liberação usando a opção "Cadastrar".

### Problema

Para vincular um problema a uma mudança, procure um existente em "Procurar por título" ou crie uma nova versão usando a opção "Cadastrar".

### Base de conhecimento

Para vincular uma base de conhecimento a mudança, procure uma existente em "Procurar por título" ou crie uma nova versão usando a opção "Cadastrar".

### Ticket

Para vincular um ticket a mudança, procure um existente em "Procurar por título" ou crie uma nova versão usando a opção "Cadastrar".

## Histórico e Audição

Para ver todas as ações e auditorias realizadas na Mudança.

## Mudança programada

Produção e exibição autorizadas de agendas de mudanças. Por exemplo, agendas de construção, teste e implementação exibem todas as alterações agendadas na programação de atividades periódicas e podem ser usadas como métodos de comunicação.


Relacionado 
---------------

[Criar um portfólio de mudança](/pt-br/4biz-helium/processes/change/configuration/change-portfolio.html)

!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;
    <b>Updated:</b>01/31/2019 – Larissa Lourenço

