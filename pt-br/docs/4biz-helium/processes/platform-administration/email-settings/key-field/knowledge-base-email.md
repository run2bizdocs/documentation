title: Campos chave dos e-mails de base de conhecimento
Description: Fornecer a relação dos campos chave disponíveis para o cadastro de modelo de e-mail relacionado à base de conhecimento.
# Campos chave dos e-mails de base de conhecimento


Este documento tem o objetivo de fornecer a relação dos campos chave disponíveis
para o cadastro de modelo de e-mail relacionado à base de conhecimento.

## Relação dos Campos Chave

São relacionados abaixo os campos chave disponíveis para inserção no cadastro de
modelo de e-mail relacionado à base de conhecimento:

| CAMPO-CHAVE | DESCRIÇÃO |
|-------------|-----------|
| ${APROVADOR}	| Aprovador do Conhecimento. Informa o nome do aprovador do conhecimento. |
| ${AUTOR} | Autor do Conhecimento. Informa o nome do autor do conhecimento. |
| ${CONTEUDO} | Conteúdo do Conhecimento. Informa a descrição do conteúdo do conhecimento. |
| ${DATAEXPIRACAO} |	Data de Expiração. Informa a data de expiração do conhecimento. |
| ${DATAINICIO} |	Data de Criação do Conhecimento. Informa a data de criação do conhecimento. |
| ${DATAPUBLICACAO} |	Data de Publicação. Informa a data de publicação do conhecimento. |
| ${DESTINATARIO} |	Grupo ou usuário a que se destina o e-mail.  |
| ${FONTEREFERENCIA} |	Fonte/Referência do Conhecimento. Informa a descrição da fonte do conhecimento. |
| ${IDBASECONHECIMENTO} |	Identificação do conhecimento. Informa a identificação do conhecimento na base. |
| ${JUSTIFICATIVAOBSERVACAO} |	Justificativa/Observação. Informa a descrição da justificativa/observação do conhecimento. |
| ${NOMEORIGEM} |	Nome origem do conhecimento. Informa a origem do nome do conhecimento. |
| ${ORIGEM} |	Origem do Conhecimento. Informa a identificação da origem do conhecimento. |
| ${PRIVACIDADE} |	Privacidade do Conhecimento. Informa a identificação da privacidade do conhecimento. |
| ${SITUACAO} |	Situação do Conhecimento. Informa a identificação da situação do conhecimento. |
| ${TITULO} |	Título do Conhecimento. Informa a descrição do título do conhecimento. |
| ${URL} |	Caminho da base de conhecimento; |
| ${VERSAO} |	Versão do Conhecimento. Informa a versão do conhecimento. |

## Exemplos de utilização

- **Modelo de e-mail para criação/ alteração de base de conhecimento**

```
Senhor(a) ${DESTINATARIO},

Informamos que o conhecimento ${TITULO} foi registrado em ${DATACRIACAO} e se encontra,

Situação: ${SITUACAO}
Autor: ${AUTOR}

Caminho: ${URL}

Atenciosamente,
```

- **Modelo de e-mail para Data de Expiração de base de conhecimento**

```
Senhor(a) ${DESTINATARIO},

Informamos que o conhecimento ${TITULO} está próximo à expirar em ${DATAEXPIRACAO} e se encontra,

Situação: ${SITUACAO}
Autor: ${AUTOR}

Caminho: ${URL}:
Atenciosamente,
```

## Relacionado

[Configurar modelo de e-mail][1]

!!! tip "About"

    <b>Product/Version:</b> 4biz | Helium &nbsp;&nbsp;
    <b>Updated:</b>01/18/2019 - Anna Martins

[1]:/pt-br/4biz-helium/platform-administration/email-settings/email-templates-configure-email-template.html