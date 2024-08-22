# Aula 02 - Classes Atributos e métodos
 
- Entender como funciona classes e atributos.

Digitar "prop" para auto completar isso:

```csharp
public int MyProperty { get; set; }
```
Para criar atributos de uma classe.
# Funcionario
**Classe:** Funcionário.

**Atributos:** ID, Nome, Cpf, Data de admissão, Salário e tipo de funcionário.
```csharp
public class Funcionario
{
  //Atributos da classe
  public int Id{get; set;}
  public string Nome { get; set; } ="";
  public string Cpf { get; set; } = string.Empty;
  public DateTime DataAdmissao { get; set; }
  public decimal Salario { get; set; }
  public TipoFuncionarioEnum TipoFuncionario { get; set; }
}
```
**Métodos:** ReajustarSalario, ExibirPeriodoExperiencia, CalcularDescontoVT, ContarCaracteres e ValidarCpf.
```csharp
 public void ReajustarSalario()
        {
            Salario = Salario + (Salario * 10/100);
        }

        public string ExibirPeriodoExperiencia()
        {
            string periodoExperiencia =
              string.Format("Periodos de Experiencia: {0} até {1} ", DataAdmissao, DataAdmissao.AddMonths(3));
            return periodoExperiencia;
        }
        public decimal CalcularDescontoVT(decimal percentual)
        {
            decimal desconto = this.Salario * percentual/100;
            return desconto;
        }
        private int ContarCaracteres(string dado)
        {
            return dado.Length;
        }
        public bool ValidarCpf()
        {
            if(ContarCaracteres(Cpf) == 11)
                return true;
            else
                return false;
        }
```
