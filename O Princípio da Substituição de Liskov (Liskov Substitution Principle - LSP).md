## O Princípio da Substituição de Liskov (Liskov Substitution Principle - LSP)

O Princípio da Substituição de Liskov (Liskov Substitution Principle - LSP) sugere que as subclasses devem poder ser substituídas por suas classes pai sem afetar a integridade do sistema. Isso significa que as subclasses não devem ter comportamentos inesperados ou violar as regras da classe pai. Um exemplo seria ter uma classe pai para representar uma forma geométrica e, em seguida, ter subclasses para representar formas específicas.
``
/**
 * <@codandobugs>
 * O Princípio da Substituição de Liskov (Liskov Substitution Principle - LSP)
 */

// Exemplo de classe pai para representar uma forma geométrica
class Shape {
  public function getArea() {
    // código para calcular a área da forma geométrica
  }
}

// Exemplo de subclasses para representar formas específicas
class Square extends Shape {
  public function getArea() {
    // código para calcular a área do quadrado
  }
}

class Circle extends Shape {
  public function getArea() {
    // código para calcular a área do círculo
  }
}
``