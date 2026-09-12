# 📚 Miniguia de Estudos DevOps com NotebookLM

> **Uso de Inteligência Artificial como ferramenta de aprendizagem ativa para estudos de DevOps, Cloud, CI/CD, Kubernetes, Infraestrutura como Código, Observabilidade, DevSecOps e SRE.**

## 🎯 Contexto e Objetivos

Este projeto foi desenvolvido como parte de um estudo prático utilizando o **NotebookLM** como ferramenta de aprendizagem ativa.

O objetivo não foi utilizar a Inteligência Artificial apenas para obter respostas prontas, mas experimentar diferentes formas de interação, avaliar a qualidade das respostas, identificar limitações e transformar os resultados em uma trilha estruturada de aprendizagem.

O estudo foi direcionado principalmente para os conhecimentos necessários ao trabalho de um profissional **DevOps**, com foco em:

* CI/CD;
* Git e controle de versão;
* Containers;
* Docker e Podman;
* Kubernetes;
* Infraestrutura como Código;
* Terraform e Ansible;
* Cloud Computing;
* Microsoft Azure, AWS e Google Cloud;
* Observabilidade;
* Prometheus, Grafana, Loki e OpenTelemetry;
* DevSecOps;
* Segurança;
* Redes e Reverse Proxy;
* Mensageria;
* Bancos de dados e armazenamento;
* SRE;
* Troubleshooting e resposta a incidentes.

### Objetivos específicos

1. Organizar uma base de conhecimento utilizando documentação técnica confiável.
2. Compreender o ciclo de vida de uma aplicação moderna, desde o commit até o usuário final.
3. Identificar os principais conceitos necessários para atuação profissional em DevOps.
4. Utilizar IA para estudar conceitos e simular situações reais.
5. Desenvolver prompts reutilizáveis para estudo, revisão, entrevistas e troubleshooting.
6. Identificar quais características tornam um prompt mais eficiente.
7. Registrar as dificuldades encontradas durante as interações com a IA.
8. Criar um material que possa ser reutilizado posteriormente como guia de estudos.

---

# 📖 Fontes-guia utilizadas no estudo

Para estruturar o conhecimento, algumas documentações foram utilizadas como referências centrais.

### 1. Google — Site Reliability Engineering

https://sre.google/books/

Material de referência para SRE, confiabilidade, SLI, SLO, SLA, Error Budget, monitoramento e operação de sistemas em escala.

### 2. Kubernetes Documentation

https://kubernetes.io/docs/

Documentação oficial para containers orquestrados, Pods, Deployments, Services, Ingress, escalabilidade e gerenciamento de aplicações.

### 3. Docker Documentation

https://docs.docker.com/

Referência para containers, imagens, redes, volumes e conceitos fundamentais de containerização.

### 4. Terraform Documentation

https://developer.hashicorp.com/terraform/docs

Referência para Infraestrutura como Código, provisionamento, estado, recursos e automação de infraestrutura.

### 5. GitHub Actions Documentation

https://docs.github.com/en/actions

Referência para automação de CI/CD, workflows, jobs, steps, execução de testes e pipelines.

> **Nota importante sobre o NotebookLM:** a eficiência das respostas não depende apenas do prompt. Ela também varia conforme a **qualidade, abrangência, organização, atualidade e disponibilidade da documentação utilizada como fonte**. Uma pergunta bem estruturada pode produzir resultados limitados quando as fontes fornecidas não possuem informações suficientes sobre o assunto. Da mesma forma, fontes muito amplas ou pouco específicas podem exigir prompts mais restritivos para obter respostas realmente úteis.

---

# 🧠 Metodologia de estudo

O processo utilizado pode ser resumido em:

```text
Documentação
     ↓
Curadoria
     ↓
NotebookLM
     ↓
Prompt inicial
     ↓
Avaliação da resposta
     ↓
Identificação das limitações
     ↓
Refinamento do prompt
     ↓
Nova interação
     ↓
Registro da aprendizagem
```

A ideia foi tratar a IA como uma ferramenta de investigação e aprendizagem, e não simplesmente como um mecanismo de geração de respostas.

---

# 🔄 Ciclo de vida de uma aplicação com CI/CD

Um dos primeiros exercícios realizados foi investigar o ciclo de vida de uma aplicação desde o desenvolvimento até o usuário final.

Uma representação simplificada é:

```text
Desenvolvedor
     │
     ▼
Git / Commit
     │
     ▼
CI
 ├── Build
 ├── Testes
 ├── Análise de código
 └── Segurança
     │
     ▼
Build da Imagem
     │
     ▼
Container Registry
     │
     ▼
CD
 ├── Homologação
 ├── Validação
 └── Produção
     │
     ▼
Kubernetes / VM / Cloud
     │
     ▼
Reverse Proxy / Load Balancer
     │
     ▼
Aplicação
     │
     ▼
Usuário Final
     │
     ▼
Observabilidade
 ├── Métricas
 ├── Logs
 └── Traces
     │
     ▼
Feedback / Incidentes
     │
     └──────────► Novo ciclo
```

## Principais decisões envolvidas

Durante esse ciclo, algumas decisões importantes precisam ser tomadas:

* estratégia de branching;
* política de revisão de código;
* testes automatizados;
* análise de segurança;
* criação e versionamento de imagens;
* armazenamento das imagens;
* estratégia de deploy;
* gerenciamento de secrets;
* configuração dos ambientes;
* rollback;
* observabilidade;
* alertas;
* escalabilidade;
* disponibilidade;
* recuperação diante de falhas.

### Estratégias de deploy estudadas

**Rolling Update**

Atualização gradual das instâncias da aplicação.

**Blue/Green**

Dois ambientes são mantidos e o tráfego pode ser direcionado para a nova versão após sua validação.

**Canary**

A nova versão é disponibilizada inicialmente para uma parcela limitada dos usuários antes da expansão.

---

# 📚 Glossário

Este glossário reúne conceitos essenciais identificados durante os estudos.

## 1. Controle de versão e CI/CD

### Git

Sistema distribuído de controle de versão utilizado para rastrear alterações no código, trabalhar com branches e colaborar no desenvolvimento.

### CI — Continuous Integration

Prática de integrar alterações frequentemente ao repositório e executar automaticamente processos como build, testes e validações.

### CD — Continuous Delivery / Continuous Deployment

Automação da entrega ou implantação de aplicações em ambientes de homologação e produção.

### Rolling Update

Estratégia que substitui gradualmente as instâncias antigas pelas novas.

### Blue/Green Deployment

Estratégia que mantém dois ambientes e alterna o tráfego entre eles.

### Canary Deployment

Estratégia que libera uma nova versão inicialmente para uma pequena parcela do tráfego.

---

# 🐳 2. Containers e Orquestração

### Container

Unidade de software que empacota uma aplicação juntamente com suas dependências.

### Imagem OCI/Docker

Artefato utilizado como base para execução de containers.

### Pod

Menor unidade implantável do Kubernetes. Pode conter um ou mais containers que compartilham rede e armazenamento.

### Deployment

Objeto declarativo do Kubernetes utilizado para gerenciar Pods e atualizações de aplicações.

### Service

Abstração que fornece uma identidade de rede estável para um conjunto de Pods.

### Ingress

Recurso utilizado para gerenciar tráfego HTTP/HTTPS direcionado para serviços dentro do cluster.

### HPA — Horizontal Pod Autoscaler

Mecanismo que ajusta automaticamente a quantidade de Pods de acordo com métricas como CPU ou memória.

---

# 🏗️ 3. Infraestrutura como Código e Cloud

### IaC — Infrastructure as Code

Prática de definir e gerenciar infraestrutura através de código versionável e automatizado.

### Idempotência

Característica de uma operação que produz o mesmo estado final quando executada repetidamente.

### Terraform State

Estado utilizado pelo Terraform para relacionar a configuração declarada com os recursos existentes na infraestrutura.

### VPC / VNet

Redes virtuais isoladas utilizadas para organizar e proteger recursos em ambientes de Cloud.

---

# 🛡️ 4. DevSecOps

### Shift-Left Security

Prática de introduzir segurança mais cedo no ciclo de desenvolvimento.

### SAST

Análise estática do código para identificar possíveis vulnerabilidades.

### SCA

Análise das dependências utilizadas pela aplicação para identificar vulnerabilidades conhecidas e questões relacionadas a componentes de terceiros.

### Secrets Management

Gerenciamento seguro de credenciais, tokens, certificados e chaves.

### RBAC

Controle de acesso baseado em funções.

---

# 📊 5. Observabilidade e SRE

### Observabilidade

Capacidade de compreender o estado interno de um sistema através de dados externos, principalmente:

* métricas;
* logs;
* traces.

### OpenTelemetry

Projeto e padrão para instrumentação, coleta, processamento e exportação de dados de telemetria.

### SLI — Service Level Indicator

Indicador quantitativo utilizado para medir determinado aspecto do serviço.

Exemplos:

* latência;
* disponibilidade;
* taxa de erro.

### SLO — Service Level Objective

Objetivo definido para determinado SLI.

### SLA — Service Level Agreement

Acordo formal entre fornecedor e cliente relacionado ao nível de serviço.

### Error Budget

Margem de falha aceitável derivada dos objetivos de confiabilidade definidos pelos SLOs.

---

# 🌐 6. Redes e Middleware

### Reverse Proxy

Servidor intermediário que recebe requisições e encaminha o tráfego para os serviços apropriados.

Pode realizar funções como:

* TLS;
* roteamento;
* balanceamento;
* cache;
* controle de acesso.

### Event Streaming

Modelo de comunicação baseado no processamento contínuo de eventos.

### Cache em memória

Camada de armazenamento rápida utilizada para reduzir latência e diminuir a carga sobre sistemas de armazenamento persistente.

Um exemplo é o Redis.

---

# 🧪 Engenharia de Prompts e "Cicatrizes"

Durante os estudos, foi possível observar que a qualidade das respostas depende diretamente da forma como o contexto é apresentado à IA.

A estratégia evoluiu de perguntas genéricas para prompts que especificavam:

* contexto;
* papel da IA;
* objetivo;
* nível profissional;
* restrições;
* formato esperado.

---
> NOTA: Sinceramente? O NotebookLM torna a interação com a IA extremamente simples. Por isso, neste trecho, foquei em explicar a linha de raciocínio que utilizo, sempre lapidando os prompts com o auxílio de outra IA para alcançar os objetivos desejados. Apesar disso, confesso que atualmente utilizo IA menos do que deveria, geralmente me limitando a trechos de código, funções e tarefas pontuais, em vez de sistemas mais extensos. Prefiro conduzir os projetos em etapas menores, mantendo o controle sobre cada parte do processo. E, claro, também utilizo a IA para transformar minhas anotações em uma documentação mais agradável, organizada e estruturada, como esta que você está lendo.
---


## Primeiro Prompt:

> Elabore o ciclo de vida de uma aplicação que segue o CI/CD do commit até o usário final. Quais aplicações em cada etapa, decisões e comandos mais usados.

## Prompt Glossário:

> Tendo em vista nossas fontes e objetivos, monte um glossário dos conceitos aprendidos nos nossos estudos.

### Prompts genéricos produzem respostas genéricas

Perguntas como:

> "Me explique Kubernetes."

não definem o nível de profundidade esperado.

---

### Assuntos muito amplos dificultam a priorização

"Me explique observabilidade" pode gerar uma resposta enorme.

Definir o contexto profissional ajuda a estabelecer prioridades.

---

### A IA tende a entregar a solução

Quando o objetivo é desenvolver troubleshooting, pedir diretamente:

> "Como resolver?"

pode eliminar justamente a etapa mais importante: o raciocínio investigativo.

---

### O papel da IA influencia a interação

Foi mais eficiente definir se a IA deveria atuar como:

* professor;
* entrevistador;
* avaliador;
* simulador de incidentes;
* orientador de estudos.

---

### Restrições aumentam a utilidade

Em determinados exercícios, limitar a resposta às fontes disponíveis ajudou a manter o estudo alinhado à documentação selecionada.

---

### O histórico pode funcionar como contexto

Ao considerar respostas anteriores e lacunas identificadas, a IA pode ajudar a construir uma sequência de estudos mais personalizada.

---

# 🧩 Estrutura de prompt utilizada

A estrutura que apresentou melhores resultados foi:

```text
Contexto
   +
Papel da IA
   +
Objetivo
   +
Nível
   +
Restrições
   +
Formato da resposta
```

### Exemplo

> "Atue como um instrutor de DevOps Pleno. Quero estudar Kubernetes Services para uma preparação profissional. Explique primeiro os conceitos fundamentais que preciso dominar, destaque os pontos mais cobrados em entrevistas e, depois, proponha um laboratório prático. Não entregue apenas definições: utilize exemplos de situações reais."

Essa estrutura tornou as respostas mais previsíveis e alinhadas ao objetivo de aprendizagem.

---

# 📝 Prompts reutilizáveis

## Para estudar

```text
Me ensine [ASSUNTO].

Comece pelos conceitos que realmente preciso dominar para atuar como DevOps Pleno.

Explique os fundamentos, mostre exemplos práticos e depois proponha um laboratório para validar meu conhecimento.
```

## Para revisar

```text
Faça uma revisão dos conceitos de [ASSUNTO] que preciso dominar como DevOps Pleno.

Priorize os conceitos mais importantes e destaque erros comuns e pontos que costumam aparecer em situações práticas.
```

## Para entrevista

```text
Faça uma entrevista técnica de DevOps Pleno.

Faça apenas uma pergunta por vez, aguarde minha resposta, avalie meu raciocínio, identifique minhas lacunas e explique como eu poderia melhorar minha resposta antes de avançar.
```

## Para estudo contínuo

```text
Com base no que já estudei, nas minhas respostas anteriores e nas lacunas identificadas, determine qual deve ser meu próximo assunto de estudo.

Justifique a prioridade e sugira uma sequência prática para aprender o tema.
```

## Para troubleshooting

```text
Minha aplicação está apresentando [ERRO].

Não entregue imediatamente a solução.

Monte uma árvore de diagnóstico, apresente hipóteses, diga quais evidências devo verificar e conduza a investigação passo a passo.
```

## Para troubleshooting baseado em fontes

```text
Minha aplicação está retornando [ERRO].

Monte uma árvore de diagnóstico utilizando apenas as fontes disponíveis neste notebook.

Priorize hipóteses, evidências, comandos/verificações e próximos passos.
```

## Para incidentes

```text
Simule um incidente de produção relacionado a [TECNOLOGIA].

Atue como um sistema em produção e me forneça informações somente conforme eu solicitar verificações.

Não entregue a causa raiz imediatamente.

Avalie meu raciocínio ao longo da investigação.
```

## Para transformar documentação em estudo

```text
Utilize as fontes disponíveis neste notebook para criar um plano de estudo sobre [ASSUNTO].

Separe em:
1. fundamentos;
2. conceitos intermediários;
3. conhecimentos necessários para DevOps Pleno;
4. troubleshooting;
5. laboratório prático;
6. perguntas de entrevista.
```

---

# 🎓 Conclusão

A principal descoberta durante este projeto foi que **Engenharia de Prompts não significa simplesmente escrever perguntas mais elaboradas**.

O processo envolve:

```text
Objetivo
   ↓
Hipótese
   ↓
Prompt
   ↓
Resposta
   ↓
Avaliação
   ↓
Identificação da limitação
   ↓
Refinamento
   ↓
Novo teste
```

As chamadas "cicatrizes" foram justamente os momentos em que a primeira interação não produziu o resultado esperado.

Registrar essas situações permitiu transformar erros de interação em conhecimento sobre como utilizar melhor a Inteligência Artificial.

No contexto de DevOps, esse processo apresenta uma relação interessante com troubleshooting.

Em ambos os casos é necessário:

* observar um comportamento;
* identificar uma anomalia;
* formular uma hipótese;
* coletar evidências;
* realizar uma alteração ou teste;
* observar o resultado;
* ajustar a hipótese;
* repetir o processo.

Dessa forma, a IA deixou de ser utilizada apenas como uma ferramenta para responder perguntas e passou a funcionar como um **ambiente de aprendizagem ativa**, capaz de simular professores, entrevistadores, avaliadores e incidentes de produção.

---

# 📚 Catálogo completo das fontes utilizadas

As fontes abaixo foram utilizadas como documentação complementar e podem ser consultadas para aprofundamento.

## 🐳 Containers e Orquestração

* Docker — https://docs.docker.com/
* Podman — https://podman.io/docs
* Podman Compose — https://github.com/containers/podman-compose
* Kubernetes — https://kubernetes.io/docs/

## 🏗️ Infraestrutura como Código

* Terraform — https://developer.hashicorp.com/terraform/docs
* Ansible — https://docs.ansible.com/

## 🔄 CI/CD

* GitHub Actions — https://docs.github.com/en/actions
* Jenkins — https://www.jenkins.io/doc/
* GitLab CI/CD — https://docs.gitlab.com/ci/
* Azure DevOps — https://learn.microsoft.com/en-us/azure/devops/

## 🌿 Controle de Versão

* Git — https://git-scm.com/doc

## ☁️ Cloud

* Microsoft Azure — https://learn.microsoft.com/en-us/azure/
* AWS — https://docs.aws.amazon.com/
* Google Cloud — https://cloud.google.com/docs
* Azure CLI — https://learn.microsoft.com/en-us/cli/azure/

## 🔐 Identidade e Acesso

* Microsoft Entra ID — https://learn.microsoft.com/en-us/entra/

## 📊 Observabilidade e Monitoramento

* Prometheus — https://prometheus.io/docs/
* Grafana — https://grafana.com/docs/
* OpenTelemetry — https://opentelemetry.io/docs/
* Loki — https://grafana.com/docs/loki/latest/
* Datadog — https://docs.datadoghq.com/

## 🛡️ Segurança / DevSecOps

* HashiCorp Vault — https://developer.hashicorp.com/vault/docs
* Trivy — https://trivy.dev/latest/
* Snyk — https://docs.snyk.io/

## 🌐 Web / Proxy / Load Balancing

* Nginx — https://nginx.org/en/docs/
* HAProxy — https://www.haproxy.org/documentation/
* Caddy — https://caddyserver.com/docs/

## 📨 Mensageria e Streaming

* RabbitMQ — https://www.rabbitmq.com/docs
* Apache Kafka — https://kafka.apache.org/documentation/

## 🗄️ Bancos de Dados e Armazenamento

* Redis — https://redis.io/docs/
* PostgreSQL — https://www.postgresql.org/docs/
* MinIO — https://min.io/docs/minio/linux/index.html

## 📕 SRE

* Google Site Reliability Engineering — https://sre.google/books/

---

# ⚠️ Observação sobre as respostas da IA

Este projeto utiliza Inteligência Artificial como ferramenta de aprendizagem, mas as respostas geradas **não devem ser consideradas automaticamente corretas ou completas**.

A eficiência do NotebookLM pode variar conforme:

* qualidade das fontes;
* quantidade de documentação disponível;
* atualidade da documentação;
* abrangência dos documentos;
* organização das fontes;
* clareza do prompt;
* contexto fornecido;
* complexidade do assunto.

Por isso, as respostas devem ser confrontadas com a documentação oficial sempre que possível.

**A IA foi utilizada como ferramenta de apoio ao aprendizado, e não como substituta da documentação técnica ou do pensamento crítico.**
