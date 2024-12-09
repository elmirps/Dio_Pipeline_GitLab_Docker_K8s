# Pipeline de Deploy de uma Aplicação Utilizando GitLab, Docker e Kubernetes 🚀

## Descrição 📜
Este projeto visa criar um pipeline de integração e entrega contínua (CI/CD) para uma aplicação simples utilizando GitLab CI, Docker e Kubernetes. O objetivo é demonstrar como a automação de testes e deploy pode ser realizada em uma aplicação Node.js, com um pipeline configurado no GitLab, que irá realizar os testes automatizados utilizando Jest e gerar uma imagem Docker para a aplicação. Esta imagem será posteriormente implantada utilizando Kubernetes.

## Tecnologias Utilizadas 🛠️
- **GitLab CI** 🔄: Utilizado para automação do processo de integração e entrega contínua, executando testes e controlando o deploy.
- **Docker** 🐳: Usado para criar um container com a aplicação Node.js, garantindo que ela rode de forma consistente em qualquer ambiente.
- **Kubernetes** 🏗️: Implementado para orquestrar o deploy da aplicação e escalabilidade no ambiente de produção.
- **Node.js** 🌐: Framework para o desenvolvimento da aplicação.
- **Jest** 🔬: Framework de testes utilizado para garantir que a aplicação funcione corretamente.
- **Prometheus** 📊 - Monitoramento da aplicação no Kubernetes.
- **Git**: Controle de versão utilizado para gerenciar o código fonte.

## Melhoria Proposta 💡
A proposta de melhoria para este projeto inclui:
1. **Automatizar o deploy no Kubernetes**: Integrar um processo de deploy automatizado no GitLab CI que implante a aplicação em um cluster Kubernetes.
2. **Pipeline de Testes de Integração**: Adicionar mais testes de integração para garantir que a aplicação funcione de forma robusta em diferentes cenários de produção.
3. **Monitoramento e Logging**: Implementar monitoramento da aplicação no Kubernetes e configurar um sistema de logging para facilitar a manutenção e resolução de problemas em produção.

## Resultados Esperados 🎯
Os resultados esperados com a execução do pipeline são:
- A aplicação será testada automaticamente toda vez que novas alterações forem feitas no repositório GitLab.
- Se os testes forem bem-sucedidos, uma nova imagem Docker será gerada, garantindo que o código seja implantado de maneira consistente em qualquer ambiente.
- A aplicação será automaticamente implantada em um cluster Kubernetes, permitindo escalabilidade e orquestração automática.

## Processo 🔄
1. **Estrutura do Projeto**: O projeto contém uma aplicação Node.js simples com um servidor Express que serve um arquivo HTML estático. O código está organizado em um repositório Git, com arquivos essenciais como o Dockerfile, `.gitignore` e `.gitlab-ci.yml` para gerenciar a integração e o deploy.
2. **Configuração do GitLab CI**: O arquivo `.gitlab-ci.yml` foi configurado para executar um pipeline que realiza os testes utilizando Jest em um ambiente Docker. A configuração inclui a etapa de testes com o comando `npm test`, que verifica se a aplicação e seus componentes estão funcionando corretamente.
3. **Criação de Imagem Docker**: A aplicação é containerizada com Docker, utilizando um Dockerfile que define o ambiente necessário para rodar a aplicação, incluindo o Node.js e suas dependências.
4. **Execução do Pipeline**: Quando um commit é feito no repositório, o GitLab CI executa o pipeline, realizando a instalação das dependências, executando os testes e, caso tudo passe, o deploy é realizado em um ambiente Kubernetes.
5. **Deploy no Kubernetes**: Uma vez que o pipeline de testes esteja completo, a imagem Docker é implantada em um cluster Kubernetes, onde a aplicação pode ser acessada e escalada conforme necessário.

## Conclusão ✅
O projeto demonstra como integrar diferentes ferramentas para criar um pipeline de deploy completo para uma aplicação simples. Utilizando GitLab CI para automação de testes, Docker para garantir consistência no ambiente de execução e Kubernetes para orquestração de deploy, conseguimos criar um sistema escalável e robusto. Além disso, a automação dos testes e do deploy ajuda a reduzir erros e aumenta a confiança nas mudanças realizadas no código.

## Reflexão 🧠
Criar um pipeline de deploy utilizando GitLab, Docker e Kubernetes traz benefícios significativos para o ciclo de vida de desenvolvimento de software. A automação dos testes e deploy permite que os desenvolvedores se concentrem no desenvolvimento de novas funcionalidades, enquanto o pipeline garante que o código seja testado e implantado de maneira eficiente e sem erros.
Além disso, o uso de Docker para containerizar a aplicação e Kubernetes para orquestrar o deploy oferece um nível de escalabilidade e flexibilidade que seria difícil de alcançar sem essas ferramentas. Embora o projeto esteja em um estágio inicial, ele serve como uma base sólida para a construção de pipelines de CI/CD mais complexos e robustos. A implementação de melhorias, como o monitoramento e logging, pode proporcionar ainda mais confiança no ambiente de produção.

