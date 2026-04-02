# Refatoração do Sistema de Olimpíadas

## Objetivo

Este projeto tem como objetivo aplicar, na prática, os princípios SOLID em um sistema legado, promovendo melhor organização, manutenção e legibilidade do código, sem alterar seu comportamento funcional original.

---

## Descrição da Refatoração

O sistema original concentrava múltiplas responsabilidades na classe App, o que dificultava a manutenção e a evolução do código.

A refatoração consistiu na separação dessas responsabilidades em classes específicas de serviço, tornando o sistema mais organizado e modular.

---

## Estrutura Após Refatoração

Foram criadas as seguintes classes de serviço:

- ParticipanteService  
- ProvaService  
- QuestaoService  
- TentativaService  

A classe App passou a ser responsável apenas pelo controle do fluxo da aplicação e interação com o usuário.

---

## Princípios SOLID Aplicados

### Single Responsibility Principle (SRP)

Cada classe passou a ter uma única responsabilidade:

- ParticipanteService: responsável pelo cadastro e listagem de participantes  
- ProvaService: responsável pela criação e listagem de provas  
- QuestaoService: responsável pelo cadastro de questões  
- TentativaService: responsável pela criação de tentativas e cálculo de nota  

A classe App ficou responsável apenas pela interação com o usuário.

---

### Open/Closed Principle (OCP)

O sistema foi estruturado de forma que novas funcionalidades possam ser adicionadas sem necessidade de modificar as classes existentes, apenas estendendo o comportamento nos services.

---

### Liskov Substitution Principle (LSP)

As classes mantêm comportamentos consistentes, permitindo que sejam utilizadas sem comprometer o funcionamento do sistema.

---

### Interface Segregation Principle (ISP)

Embora não tenham sido criadas interfaces específicas, a separação em classes de serviço já reduz o acoplamento e evita dependências desnecessárias.

---

### Dependency Inversion Principle (DIP)

A classe App deixou de depender diretamente da implementação das regras de negócio, passando a delegar essas responsabilidades para as classes de serviço.

---

## Principais Mudanças

- Remoção da lógica de negócio da classe App  
- Criação de classes de serviço para organização do código  
- Eliminação de duplicação de código  
- Delegação de responsabilidades para classes específicas  

---

## Restrições Atendidas

- A lógica original do sistema foi mantida  
- Nenhuma funcionalidade foi removida  
- Não foram utilizados frameworks externos  

---

## Estrutura do Projeto

br.com.ucsal.olimpiadas

App.java  
Participante.java  
Prova.java  
Questao.java  
Tentativa.java  
Resposta.java  

service/  
ParticipanteService.java  
ProvaService.java  
QuestaoService.java  
TentativaService.java  

---

## Conclusão

A refatoração tornou o sistema mais organizado, legível e de fácil manutenção, além de facilitar futuras alterações sem impacto no funcionamento original.