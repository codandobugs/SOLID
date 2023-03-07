## O Princípio da Inversão de Dependência (Dependency Inversion Principle - DIP)

O Princípio da Inversão de Dependência (Dependency Inversion Principle - DIP) sugere que as dependências devem ser invertidas, de forma que as classes de alto nível não dependam das classes de baixo nível, mas de abstrações. 
Isso significa que as classes de alto nível devem depender de interfaces ou classes abstratas em vez de classes concretas. 
Isso torna o código mais flexível e fácil de modificar, pois permite que você substitua as implementações sem ter que alterar o código dependente, isso também ajuda a promover a reutilização de código e a modularidade do sistema. 
Um exemplo seria ter uma classe de gerenciamento de banco de dados que depende de uma interface para a conexão com o banco de dados em vez de uma classe de conexão específica. 

```
/**
 * <@codandobugs>
 * O Princípio da Inversão de Dependência (Dependency Inversion Principle - DIP)
 */
// Exemplo de interface para a conexão com o banco de dados
interface DatabaseConnectionInterface 
{
  public function connect();
}

// Exemplo de classe concreta para a conexão com o banco de dados
class MySQLDatabaseConnection implements DatabaseConnectionInterface 
{
  public function connect() {
    // código para se conectar ao banco de dados MySQL
  }
}

/**
 * Exemplo de classe de gerenciamento de banco de dados que 
 * depende da interface para a conexão com o banco de dados
 */
class DatabaseManager {
  private $dbConnection;

  public function __construct(DatabaseConnectionInterface $dbConnection) {
    $this->dbConnection = $dbConnection;
  }

  public function executeQuery($query) {
    $this->dbConnection->connect();
    // código para executar a consulta no banco de dados
  }
}
```
