## Princípio da Responsabilidade Única (Single Responsibility Principle - SRP)

O Princípio da Responsabilidade Única (Single Responsibility Principle - SRP), diz que uma classe deve ter apenas uma única responsabilidade. Isso significa que uma classe deve ter apenas uma razão para mudar e deve ser responsável por apenas uma parte do comportamento do sistema. 
O SRP sugere que cada classe deve ter uma única responsabilidade. Isso significa que uma classe não deve fazer muitas coisas ao mesmo tempo. 
Um exemplo seria ter uma classe para lidar com a autenticação do usuário e outra classe para lidar com a criação de novos usuários.
``
/**
 * <@codandobugs>
 * O Princípio da Responsabilidade Única (Single Responsibility Principle - SRP)
 */

// Exemplo de classe para autenticação de usuário
class UserAuthenticator 
{
  public function authenticate($username, $password) {
    // código para autenticar o usuário
  }
}

// Exemplo de classe para criação de usuário
class UserCreator 
{
  public function create($username, $password, $email) {
    // código para criar um novo usuário
  }
}

``