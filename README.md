# Bem-vindo ao GAN Playground

Site de demonstração: https://reiinakano.github.io/gan-playground

![demo_screen](demo_screen.jpg)

## Perguntas Frequentes (FAQ)

### Sobre o que é este projeto?

O GAN Playground permite que você experimente Redes Neurais Adversariais Geradoras (GANs) diretamente no seu navegador. Atualmente, ele contém três conjuntos de dados integrados: MNIST, Fashion MNIST e CIFAR-10.

O GAN Playground oferece a você a capacidade de configurar os hiperparâmetros dos seus modelos e construir o discriminador e o gerador camada por camada. Você pode observar a rede aprendendo em tempo real à medida que o gerador produz imagens cada vez mais realistas ou, mais frequentemente, fica preso em falhas como o colapso de modo (*mode collapse*).

### O que são Redes Neurais Adversariais Geradoras (GANs)?

Da Wikipédia: "As redes neurais adversariais geradoras (GANs, do inglês *Generative Adversarial Networks*) são uma classe de algoritmos de inteligência artificial usados em aprendizado de máquina não supervisionado, implementadas por um sistema de duas redes neurais que competem entre si em uma estrutura de jogo de soma zero. Elas foram introduzidas por Ian Goodfellow et al. em 2014."

Em minhas próprias palavras, as GANs são compostas por duas redes neurais, cada uma tentando superar a outra. O **discriminador** tenta determinar se uma determinada imagem é real ou gerada sinteticamente pela outra rede neural. O **gerador** tenta produzir imagens indistinguíveis das reais na tentativa de enganar o discriminador. A expectativa é que o gerador aprenda o suficiente para criar imagens realistas capazes de *enganar humanos*. Se você quiser mais informações, existem muitos recursos excelentes na internet com boas introduções a GANs. Aqui está o [artigo original sobre GANs](https://arxiv.org/abs/1406.2661).

### Por que você criou isto?

Minha esperança é que este projeto proporcione a iniciantes um contato prático com o treinamento de GANs com o mínimo de configuração possível. A maneira mais fácil de fazer isso é pelo navegador e, com o deeplearn.JS, isso finalmente se tornou possível. Na verdade, quando comecei este projeto, eu não tinha experiência prévia com GANs, e meu público-alvo inicial era eu mesmo!

### Quanto tempo devo esperar / qual é o melhor conjunto de parâmetros para ver imagens realistas?

Para ser sincero, não tenho certeza. GANs são notoriamente difíceis de treinar e nem mesmo eu encontrei a combinação ideal de parâmetros e camadas nesta demonstração que produza imagens muito realistas de forma consistente. Ou é isso, ou ainda não esperei tempo suficiente para o treinamento... De qualquer forma, se você encontrar um bom conjunto de parâmetros e camadas, por favor [abra uma issue](https://github.com/reiinakano/gan-playground/issues) ou [envie um pull request](https://github.com/reiinakano/gan-playground/pulls), e eu o adicionarei a esta demonstração.

### Isto se parece com a demonstração Model Builder do deeplearn.JS.

Sim, isto é basicamente a [demonstração Model Builder do deeplearn.JS](http://deeplearnjs.org/demos/model-builder/) adaptada para o treinamento de GANs! Eu apenas removi as partes que não precisava e adicionei as partes necessárias.

## Desenvolvimento

Para executar localmente, clone o projeto e prepare o ambiente de desenvolvimento:

```bash
$ git clone https://github.com/reiinakano/gan-playground.git
$ cd gan-playground
$ npm install && bower install # Instala os módulos do node e componentes do bower
```

Para desenvolver a aplicação de forma interativa:

```bash
$ ./scripts/watch-demo src/gan-playground.ts
>> Waiting for initial compile...
>> 1023189 bytes written to src/bundle.js (0.71 seconds) at 2:20:06 AM
>> Starting up http-server, serving ./
>> Available on:
>>   http://127.0.0.1:8080
>> Hit CTRL-C to stop the server
```

