---
title: "Modelos de Arquiteturas de APIs para Open Banking"
date: 2020-11-05T10:07:21+06:00
# post image
image: "images/modelos_arquitetura_apis.png"
# post type (regular/featured)
type: "featured"
# meta description
description: "Neste post vamos abordar modelos de Arquiteturas de APIs para Open Banking"
# post draft
draft: false
#author
author: "Edgar Silva"
---




Recentemente encontrei 2 Diagramas de Arquiteturas interessantes que gostaria de compartilhar aqui através destes post.

## Arquiteturas de Soluções

Na figura abaixo, nós temos os seguintes componentes que podemos destacar:

-   **Canais de Consumidores**: Aplicações de Canais e de Provedores Terceiros (TPP).
-   **Funcionalidades Comuns**:
    -   **UX Design**  – Experiência de Usuários
    -   **DevOps**  – Modernização das Operações, Aplicações e Infraestrutura
    -   **Segurança**: Acesso, Tokens, Login Adaptativo, Detecção de Fraudes etc.
    -   _Dados e Inteligência Artificial_
    -   _Cache de Dados_
    -   _Governança_
    -   _Infraestrutura de Cloud_
-   **API Gateway  Externo**
    -   _**APIs de Open Banking e Serviços**_
        -   Produtos, Contas, Pagamentos, Clientes, ATMs, Agênias etc.
    -   **Developer Portal**
        -   Acesso as APIs, Documentações, Gerações de Tokens, SDKs etc
    -   **Sandbox**
        -   Acesso a ambientes de Testes das APIs e execuções gratuitas.
    -   **Autenticação**
        -   Serviços de Geração de Tokens e chaves de acesso, usando padrões como OAuth2, JWT etc. Integração com provedores de Autenticação, on-premises ou soluções Cloud como Azure AD, Auth0, AWS Cognito etc.
    -   **Consent Management** :
        -   Com a entrada em vigo da Lei Geral de Proteção de Dados – LGPD no Brasil, por mas que o Open Baking não faça tanta referência a mesma, na fase 2 do Open Banking do Brasil, onde haverão compartilhamento de informações, estas por sua vez deverão ter o  _consentimento_ e possibilidade de  _revogação_ por parte dos usuários, que são os donos das suas informações, consequentemente, suas identidades.
    -   **Gestão de Provedores Terceiros (TPP)**
        -   Gestão de Serviços dos terceiros, on-boarding e exposição das suas APIs.
    -   **Métricas/Relatórios/Auditoria**  : Apresentar dados de acessos das APIs, responder perguntas como “quem”, “o que”,”onde”, “quando” e “o porquê”, que possam realmente mostrar insigths do uso e consumos das APIs. Outras grandes disciplinas que podem ser atendidas nestes aspectos podem ser: Logs, Stream Analytics e Streaming/Messaging Processing (Kafka).
-   **API Gateway  Interno**
    -   Repositório de Serviços Internos, que podem estar protegidos e centralizados por um API Gateway Interno, que permita e esteja alinhado com todos os processos de DevOps, CI/CD, Cloud-Native etc.
-   **Core Bancários e Sistemas de Registros**
    -   Integrar e Expor via APIs os Cores Bancários e sistemas existentes no Banco é fundamental para a habilitação de Open Banking.
    -   Um cliente uma vez fez um comentário que concordo totalmente:  _“O Open Banking nós já temos, só falta abrir”
-   **Fora do Banco**
    -   Diretórios de Open Banking
    -   Registros de Identidades
    -   Parceiros de Negócios
    -   Órgãos regulatórios
    -   Redes de Pagamentos

Abaixo um diagrama que pode fazer você se encontrar na sua implementação atual:

![](https://skalena.files.wordpress.com/2020/12/a9ab4-image.png?w=1024&h=495)

Arquitetura para Open Banking

## Arquitetura de Componentes em Camadas

No Diagrama abaixo, eu gostaria de destacar as camadas de componentes e APIs, assim como o impacto ou necessidade do negócio envolvido:

-   **APIs de Experiência:** Onde existe uma alta demanda de opiniões e orientação das áreas de negócios.
-   **APIs de Processo**  : Exposição de Processos via APIs, além de incorporar e/ou executar regras e tratamentos de exceções e erros.
-   **APIs de Sistemas:**  Basicamente expor os dados de seus protocolos, de forma mais unificada e com a possibilidade reuso.
-   **Aplicações, Protocolos e Dados**: É importante ter um mecanismo, framework ou solução de integração com soluções SaaS, Mainframes(legados), trocas de dados com FTP, SFTP, uso de CDC(Change Data Capture) etc.

![](https://skalena.files.wordpress.com/2020/12/784d3-image-1.png)

## Taxonomia de APIs usados por grandes Bancos

O objetivo deste post é trazer para você uma espécie de espelho para idéias do que você pode e deve implementar em sua estratégia de OpenBanking.

Em termos de produtos e plataformas, vários deles podem ser usados para entregar sua solução de Open Banking, e lembrando, os mesmos conceitos podem ser usados para uma entrega de Open Health (Saúde), Open Insurance (Seguros), Open Government (Governo) etc.

Precisando de qualquer ajuda, estamos por aqui em :  [https://skalena.com/contato](https://skalena.com/contato)  .