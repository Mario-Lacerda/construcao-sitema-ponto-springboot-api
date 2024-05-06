# Construir sistema de controle de ponto e acesso API REST com Spring Boot 



​             Neste projeto você terá o desafio de desenvolver uma API Rest para controle de ponto e acesso dos usuários de uma empresa. Utilizaremos Java 16, Spring Boot, Spring Data com auditoria, Banco H2, Gradle e Swagger.

## **Criação do projeto**

O primeiro passo é criar um novo projeto Spring Boot. Você pode usar o Spring Initializr para isso. No Spring Initializr, selecione as seguintes dependências:

- Spring Web
- Spring Data JPA
- H2 Database
- Spring Boot Gradle Plugin
- Springfox Swagger2

Após selecionar as dependências, clique em "Generate Project". O Spring Initializr vai gerar um novo projeto Spring Boot.

### **Configuração do banco de dados**

O próximo passo é configurar o banco de dados. Para isso, abra o arquivo `application.properties` e adicione as seguintes configurações:



```plaintext
spring.datasource.url=jdbc:h2:mem:ponto-e-acesso
spring.datasource.username=sa
spring.datasource.password=
```

### ** Criação das entidades**

O próximo passo é criar as entidades do nosso sistema. As entidades são os modelos de dados que representam os dados do nosso sistema. Neste projeto, criaremos as seguintes entidades:

- `Usuario`: representa um usuário do sistema.
- `HorarioDeTrabalho`: representa um horário de trabalho de um usuário.
- `RegistroDePonto`: representa um registro de ponto de um usuário.

### **Configuração do JPA**

O JPA é um padrão de persistência de dados que permite mapear objetos Java para tabelas de banco de dados. No Spring Boot, o JPA é configurado automaticamente. No entanto, precisamos configurar algumas propriedades do JPA para que ele funcione corretamente. Para isso, abra o arquivo `application.properties` e adicione as seguintes configurações:

```plaintext
spring.jpa.hibernate.ddl-auto=update
spring.jpa.generate-ddl=true
```

### **Configuração da auditoria**

A auditoria permite rastrear as alterações feitas nas entidades do nosso sistema. Para configurar a auditoria, abra o arquivo `application.properties` e adicione as seguintes configurações:

```plaintext
spring.data.jpa.auditing.auditor-aware-ref=auditorAware
```

### **Criação do repositório**

O repositório é uma classe que é responsável por acessar os dados do banco de dados. No Spring Boot, o repositório é configurado automaticamente. No entanto, precisamos criar uma interface para o nosso repositório. A interface deve estender a classe `JpaRepository`.

```
public interface UsuarioRepository extends JpaRepository<Usuario, Long> {
}
```



### **Criação dos serviços**

Os serviços são responsáveis por fazer a lógica de negócio do nosso sistema. No nosso sistema, criaremos dois serviços:

- `UsuarioService`: responsável pela lógica de negócio de usuários.
- `HorarioDeTrabalhoService`: responsável pela lógica de negócio de horários de trabalho.

### *Criação dos controladores**

Os controladores são responsáveis por lidar com as requisições HTTP do nosso sistema. No nosso sistema, criaremos dois controladores:

- `UsuarioController`: responsável pelas requisições HTTP de usuários.
- `HorarioDeTrabalhoController`: responsável pelas requisições HTTP de horários de trabalho.

### ** Configuração do Swagger**

O Swagger é uma ferramenta que permite documentar as APIs do nosso sistema. Para configurar o Swagger, abra o arquivo `application.properties` e adicione as seguintes configurações:

```
springfox.documentation.swagger.v2.enabled=true
```



## **Testes automatizados**

É importante escrever testes automatizados para garantir que o nosso sistema está funcionando corretamente. No nosso sistema, vamos escrever os seguintes testes automatizados:

- Teste unitário para o serviço de usuários.
- Teste unitário para o serviço de horários de trabalho.
- Teste de integração para o controlador de usuários.
- Teste de integração para o controlador de horários de trabalho.

### **Implantação do sistema**

O último passo é implantar o sistema em um servidor. Para isso, podemos usar uma ferramenta como o Docker ou o Kubernetes.

Com isso, você terá criado um sistema de controle de ponto e acesso com Java 16, Spring Boot, Spring Data com auditoria, Banco H2, Gradle e Swagger.



### **Por que usar Java 16, Spring Boot, Spring Data com auditoria, Banco H2, Gradle e Swagger?**

- **Java 16:** Java 16 é a versão mais recente do Java e traz vários recursos novos, como melhorias de desempenho, novas APIs e recursos de linguagem.
- **Spring Boot:** Spring Boot é um framework que simplifica o desenvolvimento de aplicações Java. Ele fornece uma configuração padrão para muitas tarefas comuns, como configuração de banco de dados, segurança e internacionalização.
- **Spring Data com auditoria:** Spring Data é um framework que simplifica o acesso a dados no Spring. Spring Data com auditoria permite rastrear as alterações feitas nas entidades do nosso sistema.
- **Banco H2:** H2 é um banco de dados em memória que é muito rápido e fácil de usar. Ele é ideal para desenvolvimento e teste.
- **Gradle:** Gradle é um sistema de construção que automatiza o processo de construção do nosso projeto. Ele pode ser usado para compilar o código, executar testes e implantar o aplicativo.
- **Swagger:** Swagger é uma ferramenta que permite documentar as APIs do nosso sistema. Ele gera uma documentação interativa que pode ser usada por desenvolvedores e usuários.

## **Conclusão do aprendizado**

Ao concluir este projeto, você terá aprendido como:

- Desenvolver uma API Rest com Spring Boot.
- Usar Spring Data para acessar dados em um banco de dados.
- Usar Spring Data com auditoria para rastrear alterações em entidades.
- Usar o banco de dados H2 para desenvolvimento e teste.
- Usar Gradle para construir e implantar seu projeto.
- Usar Swagger para documentar as APIs do seu sistema.

Este projeto é um ótimo ponto de partida para aprender como desenvolver aplicações Java corporativas.



**Documentacao gerada pelo swagger:** http://localhost:8081/swagger-ui.html
