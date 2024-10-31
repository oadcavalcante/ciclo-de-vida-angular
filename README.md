# Ciclo de Vida dos Componentes no Angular

![lifecycle](https://github.com/oadcavalcante/ciclo-de-vida-angular/blob/main/src/assets/lifecycle.png)

Este projeto demonstra o ciclo de vida dos componentes no Angular, detalhando cada um dos principais eventos de ciclo de vida que são disparados em componentes Angular. Esses eventos permitem controlar o comportamento de um componente desde sua criação até sua destruição, facilitando o gerenciamento de estados, dados e otimizações de desempenho.

## Visão Geral do Ciclo de Vida

Cada componente Angular passa por uma série de fases durante sua existência. A seguir, estão os principais métodos de ciclo de vida que podem ser implementados em um componente:

1. **ngOnChanges**  
   Executado sempre que uma ou mais propriedades de entrada (input properties) de um componente mudam. Este método é útil para responder a alterações nas entradas do componente.

2. **ngOnInit**  
   Chamado uma única vez após o primeiro `ngOnChanges`. Ideal para inicializações que devem ocorrer após a criação do componente, como configurações de propriedades que dependem de outras variáveis de entrada.

3. **ngDoCheck**  
   Invocado a cada ciclo de verificação de mudanças (change detection). Esse método permite que o desenvolvedor implemente sua própria verificação de mudanças customizada, caso necessário.

4. **ngAfterContentInit**  
   Disparado uma vez após o Angular inserir o conteúdo externo (ng-content) no componente. Útil para acessar e manipular conteúdo inserido dinamicamente.

5. **ngAfterContentChecked**  
   Executado após cada verificação do conteúdo inserido no componente, permitindo o gerenciamento contínuo de conteúdo dinâmico.

6. **ngAfterViewInit**  
   Chamado após a inicialização das visualizações do componente e de suas visualizações filhas. Ideal para qualquer operação que dependa de elementos DOM do próprio componente.

7. **ngAfterViewChecked**  
   Executado após cada verificação das visualizações do componente e de suas visualizações filhas. Permite monitorar mudanças contínuas nas visualizações do componente.

8. **ngOnDestroy**  
   Chamado imediatamente antes da destruição do componente. Ideal para limpar assinaturas, observables e outros recursos que possam causar vazamentos de memória.

## Estrutura do Projeto

Este projeto contém exemplos de cada evento de ciclo de vida aplicados em um componente. No exemplo, cada método de ciclo de vida é implementado com mensagens no console para facilitar o entendimento da ordem e do contexto de cada um.

## Requisitos e Instalação

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/ciclo-vida-angular.git
   cd ciclo-vida-angular

2. **Instalar dependências:**
   ```bash
   npm install
   
3. **Iniciar o servidor de desenvolvimento:**
    ```bash
    ng serve
    ```
4. **Acesse o projeto em** _http://localhost:4200_

## Executando o Projeto

  1. Abra o console do navegador para visualizar as mensagens de log que mostram a execução dos métodos de ciclo de vida.
  2. Interaja com o componente de exemplo para observar a ordem dos eventos de ciclo de vida.
  3. Use o botão "Remover Componente" para ver o ngOnDestroy em ação.

## Tecnologias Utilizadas

* **Angular** - Framework front-end para desenvolvimento de componentes reutilizáveis e modulares.
* **TypeScript** - Linguagem que permite definir interfaces e garantir tipos nas implementações dos métodos de ciclo de vida.
