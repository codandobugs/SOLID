## O Princípio da Segregação de Interfaces (Interface Segregation Principle - ISP)

O Princípio da Segregação de Interfaces (Interface Segregation Principle - ISP) sugere que os clientes não devem ser forçados a depender de interfaces que não utilizam. Isso significa que você deve evitar interfaces grandes e genéricas, e em vez disso, criar interfaces mais específicas para cada caso de uso. Isso ajuda a reduzir o acoplamento entre classes e torna o código mais flexível e fácil de modificar. Sendo assim, as interfaces devem ser pequenas e coesas, com apenas os métodos necessários para um determinado cliente. Um exemplo seria ter uma interface para uma classe de relatório com apenas os métodos necessários para gerar relatórios.
``
/**
 * <@codandobugs>
 * O Princípio da Segregação de Interfaces (Interface Segregation Principle - ISP)
 */

// Exemplo de interface para uma classe de relatório
interface ReportGeneratorInterface 
{
  public function generateHeader();
  public function generateBody();
  public function generateFooter();
  public function saveToFile($fileName);
}

/**
 * Exemplo de classe que implementa a interface com apenas os métodos necessários 
 * para gerar relatórios em formato PDF
 */
class PDFReportGenerator implements ReportGeneratorInterface 
{
  public function generateHeader() {
  // código para gerar o cabeçalho do relatório em PDF
  }

  public function generateBody() {
  // código para gerar o corpo do relatório em PDF
  }

  public function generateFooter() {
  // código para gerar o rodapé do relatório em PDF
  }

  public function saveToFile($fileName) {
  // código para salvar o relatório em PDF no arquivo especificado
  }
}
``