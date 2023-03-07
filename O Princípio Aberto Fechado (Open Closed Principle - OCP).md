## O Princípio Aberto/Fechado (Open/Closed Principle - OCP)

O Princípio Aberto/Fechado (Open/Closed Principle - OCP) sugere que as classes devem ser abertas para extensão, mas fechadas para modificação. Isso significa que o código deve ser projetado de forma que possa ser estendido sem precisar modificar o código existente. Um exemplo seria ter uma classe abstrata para definir uma interface comum e, em seguida, criar classes concretas que implementam essa interface.
``
/**
 * <@codandobugs>
 * O Princípio Aberto/Fechado (Open/Closed Principle - OCP)
 */

// Exemplo de classe abstrata para definir uma interface comum
abstract class PaymentMethod 
{
  abstract public function processPayment($amount);
}

// Exemplo de classes concretas que implementam a interface comum
class CreditCardPayment extends PaymentMethod 
{
  public function processPayment($amount) {
    // código para processar pagamento com cartão de crédito
  }
}

class PayPalPayment extends PaymentMethod 
{
  public function processPayment($amount) {
    // código para processar pagamento com PayPal
  }
}
``