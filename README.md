# API Médica Voll

Esta é uma API baseada em Java para um sistema médico, desenvolvida usando Spring Boot e Maven. A aplicação utiliza PostgreSQL para armazenamento de dados e Swagger para documentação da API.

## Tecnologias Utilizadas

- Java: Linguagem de programação usada para desenvolver a aplicação.
- Spring Boot: Framework usado para facilitar o desenvolvimento de aplicações Spring.
- Spring Security: Framework usado para fornecer autenticação e autorização.
- Maven: Ferramenta de gerenciamento de projetos e compilação.
- PostgreSQL: Sistema de banco de dados relacional de código aberto.
- Swagger: Ferramenta usada para documentação da API.
- JWT (JSON Web Token): Padrão (RFC 7519) para criação de dados com assinatura que podem ser verificados e confiáveis.
- Hibernate: Framework para mapeamento objeto-relacional para Java.

## Estrutura do Projeto

O projeto é dividido em vários módulos:

- `med.voll.api.controller`: Contém os controladores para manipulação de requisições HTTP.
- `med.voll.api.domain`: Contém as classes de domínio e repositórios para acesso a dados.
- `med.voll.api.domain.medico`: Contém as classes relacionadas à entidade `Medico`.
- `med.voll.api.domain.paciente`: Contém as classes relacionadas à entidade `Paciente`.
- `med.voll.api.domain.consulta`: Contém as classes relacionadas à entidade `Consulta`.
- `med.voll.api.domain.endereco`: Contém as classes relacionadas à entidade `DadosEndereco`.
- `med.voll.api.infra.security`: Contém as classes relacionadas às configurações de segurança.

## Configuração

Para executar este projeto, você precisa ter Java e Maven instalados em sua máquina.

1. Clone o repositório.
2. Navegue até o diretório do projeto.
3. Execute `mvn clean install` para construir o projeto.
4. Execute `mvn spring-boot:run` para iniciar a aplicação.

## Configuração do Banco de Dados

A aplicação utiliza PostgreSQL, um poderoso sistema de banco de dados relacional de código aberto, para gerenciar e manipular o banco de dados. A configuração do banco de dados é feita através do arquivo `application-prod.properties` localizado em `src/main/resources`. Este arquivo contém as seguintes configurações:

- `spring.datasource.url`: URL do banco de dados. Esta é a URL de conexão com o banco de dados PostgreSQL que a aplicação irá utilizar.
- `spring.datasource.username`: Nome de usuário para a conexão com o banco de dados.
- `spring.datasource.password`: Senha para a conexão com o banco de dados.

Além disso, o arquivo também contém configurações do JPA:

- `spring.jpa.show-sql`: Se verdadeiro, o SQL gerado pelo Hibernate será exibido.
- `spring.jpa.properties.hibernate.format_sql`: Se verdadeiro, o SQL gerado pelo Hibernate será formatado para uma leitura mais fácil.

Para alterar qualquer uma dessas configurações, você deve alterar os valores correspondentes no arquivo `application-prod.properties`. Lembre-se de que essas configurações são sensíveis e devem ser tratadas com cuidado para evitar a exposição de dados sensíveis.

## Documentação da API

A documentação da API é gerada usando Swagger. Você pode visualizar a documentação navegando para `/swagger-ui.html` em sua aplicação quando ela estiver em execução. Isso exibirá uma interface interativa onde você pode visualizar e testar os endpoints da sua API.

## Testes

O projeto contém testes unitários para os repositórios. Esses testes podem ser encontrados no diretório `src/test/java`.

## Segurança

A aplicação utiliza JWT (JSON Web Token) para autenticação. As configurações de segurança estão localizadas no pacote `med.voll.api.infra.security`.

## Contribuindo

Pull requests são bem-vindos. Para alterações importantes, por favor, abra uma issue primeiro para discutir o que você gostaria de mudar.

