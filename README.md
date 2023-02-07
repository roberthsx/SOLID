# Aplicações com principio SOLID


## SOLID

- S Single Responsibility Principle(SRP)
- O Open-Closed Principle(OCP)
- L Liskov Substitution Principle(LSP)
- I Interface Segregation Principle(ISP)
- D Dependecy Inversion Principle(DIP)

### Single Responsibility Principle(SRP)
Cada classe deve ter apenas um motivo para mudar
Cada classe deve ter apenas uma responsabilidade a ser cumprida

	• Unica responsabilidade
	• Classes menores 
	• fáceis de manter
	• Mais fáceis de estender
	• fáceis de testar

## Open-Closed Principle(OCP)
Você deve ser capaz de estender um comportamento de uma classe sem a necessidade de altera-lo
, classes deverão ser abertas para extensão mas fechadas para alteração,Estender significa incluir novas funcionalidades sem precisar mexer no que esta pronto, mantendo a estabilidade do código.Alterar  é incluir novas funcionalidades mexendo no que esta pronto , o que geralmente causa impacto no código.

Como implementar o principio aberto/fechado?

	• Adicionar as novas funcionalidades criando novas classes derivadas que devem ser herdadas da classe base original.
	• Permitir que o cliente acesse a classe original com uma interface abstrata.
	• fáceis de manter
	• Criar classes derivadas e deixar a implementação da classe original inalterada

Consequências ao não seguir o principio aberto/fechado?

	• Precisa testar as novas funcionalidades e também as antigas
	• Incluir novas funcionalidades dificulta a manutenção do código
	• Violação do principio da responsabilidade unica

## Liskov Substitution Principle(LSP)

	• Uma classe base deve poder ser substituída pela sua classe derivada sem alteração no comportamento final
	• "Se q(x) é uma propriedade demonstrável dos objetos x de tipo T. então q(y) deve ser verdadeiro para os objetos y de tipo S onde S é um subtipo de T" Barbara Liskov - 1984
	• A instância de uma classe base deve permitir a sua substituição por instâncias de classes derivadas sem que se necessite realizar qualquer alteração no código
	• Uma classe derivada deve poder sobrescrever os métodos da classe base de forma que a funcionalidade do ponto de vista do cliente continue a mesma. (sem quebrar o código)
	• O principio LSP é aplicável quando existe um relacionamento de herança onde temos uma ou mais classes derivadas herdando de uma classe base
	• Neste contexto os métodos da classe base estão definindo um contrato e espera-se que cada classe derivada cumpra este contrato.
	• Se uma classe derivada não aderir ao contrato definido da classe base esta violando o principio LSP
Se uma classe derivada estender ou sobrescrever o comportamento da classe base implementando um novo comportamento isso esta violando o principio LSP

## Interface Segregation Principle(ISP)


	• Reduzir os efeitos colaterais e a frequência das alterações necessárias, dividindo o software em várias partes independentes.
	• Obter um baixo acoplamento
	• Ter interfaces focadas em sua responsabilidade (SRP)
	• Reduzir as dependências no código


## Dependecy Inversion Principle(DIP)

	• Módulos de alto nível não devem depender de módulos de baixo nível. Ambos devem depender de uma abstração
	• Abstrações não devem depender de detalhes. Detalhes devem depender de abstrações 
	• Módulos de alto nível = classes de alto nível que por sua vez são classes de negócios que encapsulam logica complexa
	• Módulos de baixo nível = classe de baixo nível que são classes que fazem acoes básicas, acesso ao disco, acesso ao protocolo de banco de dados
	• Programe para uma interface e não para uma implementação
	• O principio Inversão de dependência não deve ser confundido com o padrão de projeto injeção de dependência.
