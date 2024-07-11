# Hugo Leonardo Terra de Oliveira

Alfenas, Minas Gerais, Brazil  
+55-35-98875-7779  
<hugo@tce.dev.br>  

## Projetos e Habilidades

### Posição, empresa, projetos relevantes e detalhamento técnico.

### 1. Arquiteto/Desenvolvedor no Grupo Grão de Ouro

Inicialmente, fui contratado para desenvolver um e-commerce. Após analisar todos os requisitos, propus criar um ponto de venda com uma área de back-office do zero, pois o e-commerce era muito complexo para a necessidade real.

Além disto, haviam regras específicas que precisavam ser desenvolvidas, como produção fábril, armazenamento de produtos e matérias-primas, bonificações, metas e logística (interna/externa).

Para aumentar o desafio, cada área tinha seu próprio sistema e precisava ser integrada à solução. ♨️♨️♨️

>## Nutrimax
>
><div align="center"><img src="https://github.com/hugomarshall/me/raw/main/Nutrimax-Architecture.drawio.png" alt="Nutrimax Architecture" width="300" /></div>
>
>**- Back-end:** C#;
>
>**- Front-end:** Modelo responsivo AdminLTE para dispositivos móveis, tablets e TVs, usando Razor, HTML5, CSS3, Javascript, Jquery, Polly e NPM.
>
>**- Banco de dados:** SQL Server com Entity Framework Core, Dapper, consultas SQL e stored procedures.
>
>**- Padrões de projeto:** MVC, Unit-Of-Work, Repository, Generics, DDD (Domain Driven Design).
>
>**- Identidade:** Especificações OpenID misturadas com Active Directory.
>
>**- APIs:** netCore, OAS3 (Especificação Open API).
>
>**- Logs:** Serilog.
>
>**- Relatórios:** Integrações Report Server MSSQL, Syncfusion, Page Reports.
>
>**- Testes:** Testes unitários com xUnit, testes de integração, carga e estresse.
>
>### **PDV (Ponto de venda):**
>
> Área para o setor comercial e representantes coletarem pedidos. Com base em suas permissões, é possível escolher catálogos de preços com filtros.
>
>### **Back-office:**
>
> Área para CEO, gerentes, diretores, chefes e equipes parametrizarem, controlarem e gerenciarem todo o sistema com políticas hierárquicas para produção, comercialização, embalagem e logística.
>
>**Processo em segundo plano:**
>
> Criei alguns robôs para executar serviços em segundo plano, como análise automática de pedidos. Se aprovado, o pedido é colocado na fila para integração com o ERP.
>
>
>**Integrações com terceiros:**
>
>- Utilização direta de consultas SQL (Para resolver isso, foi necessário efetuar um profiler no banco de dados para capturar e entender as consultas (feito em conjunto com gestor));
>- ViaCEP: API REST para buscar endereços no Brasil;
>- Sendgrid: Remetente de e-mails, SMS e campanhas;
>- Wiki.js: Documentação de uso do sistema;
>
>
Essa primeira solução levou 6 meses para ser lançada e mais 6 meses para finalizar todos os ajustes com novos recursos.

>## S2GO
>
>Após concluir o projeto Nutrimax, o grupo decidiu criar um novo projeto para centralizar a coleta de dados e compartilhá-los entre diferentes setores de todo o grupo. E assim surge o S2GO (Sistema Grupo Grão de Ouro)…
>
><div align="center"><img src="https://github.com/hugomarshall/me/raw/main/S2GO-Architecture.drawio.png" width="300" /></div>
>
>O objetivo do S2GO é fornecer um ambiente para colaboradores automatizarem processos diários de trabalho e centralizarem informações de dados para serem processadas e tratadas por cada empresa/setor, seguindo suas próprias regras.
>Não posso mostrar diagramas detalhados devido a acordos de confidencialidade, mas na imagem abaixo você pode ver uma visão macro da solução.
>
><div align="center"><img src="https://github.com/hugomarshall/me/blob/main/S2GO-Projetos.drawio.png" alt="API Gateway" width="300" /></div>
>
>A solução foi criada seguindo as melhores práticas de arquitetura limpa para microsserviços, CQRS, Option, Generics, Message Brokers e Repository.
>
>### **- Front-end:**
>
>Layout responsivo para dispositivos móveis, tablets e TVs usando Blazor com o framework Syncfusion, HTML5, CSS3 e Javascript.
>
>### **Portal do Cliente:**
>
>A primeira solução foi uma plataforma centralizada para os clientes se registrarem, com um layout de modelo personalizado para cada empresa.
>Aqui, a equipe comercial pode compartilhar links temporários personalizados para um formulário, permitindo que os clientes atualizem e validem seus perfis ou criem uma conta.
>Para viabilizar esse processo, a equipe comercial entra em contato com cada cliente para obter seu e-mail principal e número de celular para enviar o link (cadastro reverso).
>
>
>### **Back-office:**
>
>O back office foi separado por rotas de empresa, onde cada empresa tem sua própria configuração, layout e regras.
>
>O processo comum compartilhado entre todos eles é a integração com terceiros, cada empresa possui sua própria biblioteca de classes encapsulando todos os processos (baixo acoplamento). 
>
>
>### **API´s:**
>
>**- Gateway:**
>
>Utilizei o Ocelot para implementar um API Gateway básica. A imagem abaixo mostra como o gateway funciona.
>
><div align="center"><img src="https://github.com/hugomarshall/me/raw/main/S2GO-API%20-%20Gateway.drawio.png" alt="API Gateway" width="300" /></div>
>
>
>**- Identidade:**
>
>API compartilhada entre cada empresa para gerenciamento de usuários, permissões, regras e políticas.
>Padrão OpenID usando o Microsoft Identity Framework com autenticação de token Bearer e integração com o Active Directory.
>
>
><div align="center"><img src="https://github.com/hugomarshall/me/raw/main/S2GO-Login.drawio.png" alt="Login UML" width="300" /></div>
>
>
>**- API Clientes:**
>
>API compartilhada entre cada empresa para gerenciamento de clientes.
>
>**- Nutrimax:**
>
>Migração da API do Nutrimax (.NET Core 3) para funcionar com o mesmo núcleo (.NET Core 6) e padrões de configuração.
>
>**- "Companies":**
>
>Resumi todas as APIs das empresas devido a acordos de confidencialidade.
>
>### **Gerenciamento de Processos com Hangfire:**
>
>Todos os processos em segundo plano foram migrados para o Hangfire, pois ele pode ser escalado, monitorado e executado independentemente.
>
>### **Aplicativo Móvel:**
>
>Desenvolvi um aplicativo móvel para que os clientes possam assinar contratos digitais e verificar os produtos armazenados no depósito.
>Para o desenvolvimento, utilizei a plataforma Xamarin com o padrão MVVM, DryIoc para IoC e Refit para lidar com solicitações REST.
>
>
><div align="center"><img src="https://github.com/hugomarshall/eu/assets/4738928/657b09e9-2746-463e-b2af-95b7e664d0ff" alt="Login UML" width="300" /></div>
>
>### **Integrações de Terceiros:**
>
>- ERP Agrotis: Consulta direta ao SQL (Para isso, foi necessário criar um perfil no banco de dados para entender e capturar as consultas);
>- ViaCEP: API REST para buscar endereços no Brasil gratuitamente;
>- D4Sign: API REST para criar contratos digitais (uso de webhooks);
>- SintegraWS: API REST;
>- Wiki.js: Documentação do sistema;
>- Sendgrid: Remetente de e-mails e SMS;

---

### 2. Senior Web Developer at Cresça Brasil (Adquirido pela Uol Educação)

Como líder técnico neste projeto em específico, fiz parte da equipe de Pesquisa e Desenvolvimento e fui responsável por desenvolver vários sistemas importantes, incluindo:
- Portal de Gerenciamento de Projetos (Interno): Desenvolvi um portal interno para gerenciar projetos, proporcionando uma plataforma eficiente para colaboração e progresso da equipe.
- Chatbox com SignalR para Telemarketing: Criei um chatbox usando SignalR para ser usado no sistema de telemarketing, melhorando a comunicação e interação com os clientes.


>## Streaming de Vídeo Privado de Alta Disponibilidade com AWS
>
>Esse projeto foi um dos meus maiores desafios. Atuei como líder técnico e trabalhei em conjunto com um especialista em infraestrutura para criar uma solução que armazenasse cursos online e os disponibilizasse para os alunos.
>O foco principal era a segurança e a prevenção de downloads não autorizados.
>O sistema utilizava um player genérico que podia ser incorporado em qualquer página dos clientes, com sete camadas de segurança.
>O objetivo era dividir o fluxo de streaming em pequenos tamanhos de buffer e enviá-los ao cliente, tornando praticamente impossível o download completo dos arquivos.
>
>**- Back-end language:** C#;
>
>**- Front-end:** Layouts responsivos para dispositivos móveis e pcs utilizando Asp.net, Javascript e CSS;
>Na época não existiam frameworks responsivos e a página inteira foi desenvolvida com HTML e CSS puros para cada dispositivo.
>
>**- Banco de Dados:** SQL Server com entity framework e conexões diretas (BLL, DAL).
>
>**- Padrões:** MVC, Repository, Factory.
>
>
>**Integrações com terceiros:**
>
>- AWS: S3 Storage, Firewall, EC2 e Lambda;
>- JWplayer: Player privado para renderizar streams.
>

---

### 3. Desenvolvedor Full stack Sênior na Iterative

A Iterative é uma Fábrica de Software em São Paulo e foi uma das primeiras empresas a adotar o trabalho remoto. Eu fui um dos funcionários que participou dessa mudança.

Nela eu participei da equipe de food services que era um sistema focado na gestão de restaurantes. 

>## Linked Gourmet (Serviços no ramo alimentício)
>
>O projeto foi dividido em três equipes: duas de desenvolvimento (back-office e caixa) e uma de suporte. Eu fui o principal desenvolvedor sênior na equipe de desenvolvimento do back-office.
>O modelo da solução é SaaS (Software como Serviço) usando o padrão de microservices e message broker.
>
>## Back-Office
>
>Portal web para configurar, monitorar e manter restaurantes.
>
>**- Padrões:** MVVM, Generics, Repository, Factory;
>
>**- Back-end:** C#;
>
>**- Front-end:** Layout responsivo para dispositivos móveis, tablets e TVs usando HTML, Javascript, CSS e o framework Knockout;
>
>**- Banco de dados:** SQL Server com Entity Framework, consultas SQL e stored procedures.
>
>
>**- 3th Party Integrations:**
>
>- Azure: Armazenamento, Service Bus;
>
>## Sync
>
> Executável para sincronizar dados entre o back-office e o Caixa.
>
>## Caixa
>
> Local API Server to run disconected from internet and mobile interfaces for waiters and desktop to cashier.
>
>**- Patterns:** CQRS, DDD, Mediatr, Command e Observer.
>
>**- Back-end:** C#;
>
>**- Front-end:** Responsive layout for mobile, tablets and TV´s using Angular, Javascript and Bootstrap;
>
>**- Database:** SQLite com Entity Framework.
>
>
>**3th Party Integrations:**
>
>- Azure: Storage, Service Bus;
>- Payment Gateways: Stone, MundiPagg;
>- Cardápio online: iFood;
>
>
