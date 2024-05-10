    import java.util.Scanner;

    public class SalarioReajuste {


    public static void main(String[] args) {
        // Cria um objeto Scanner para entrada de dados
        Scanner scanner = new Scanner(System.in);

        // Solicita ao usuário que insira o salário atual
        System.out.print("Digite o salário atual do colaborador: ");
        double salario1 = scanner.nextDouble();

        // Define as Taxas de reajuste e percentuais de aumento
        double Taxa1 = 280.0;
        double Taxa2 = 700.0;
        double Taxa3 = 1500.0;
        double porcentagemTaxa1 = 0.2;
        double porcentagemTaxa2 = 0.15;
        double porcentagemTaxa3 = 0.1;
        double porcentagemTaxa4 = 0.05;
        double inflacao = 0.03;
        // Calcula o reajuste de acordo com a Taxa salarial
        double salarioReajuste;
        double porcentagemAumento;
        double salarioAumento;
        double aumentoPosReajuste;

        if (salario1 <= Taxa1) {
            salarioReajuste = salario1 * (1 + porcentagemTaxa1);
            porcentagemAumento = porcentagemTaxa1 * 100;
            salarioAumento = salario1 * porcentagemTaxa1;
            aumentoPosReajuste = salarioAumento - (salarioAumento * inflacao);
        } else if (salario1 <= Taxa2) {
            salarioReajuste = salario1 * (1 + porcentagemTaxa2);
            porcentagemAumento = porcentagemTaxa2 * 100;
            salarioAumento = salario1 * porcentagemTaxa2;
            aumentoPosReajuste = salarioAumento - (salarioAumento * inflacao);
        } else if (salario1 <= Taxa3) {
            salarioReajuste = salario1 * (1 + porcentagemTaxa3);
            porcentagemAumento = porcentagemTaxa3 * 100;
            salarioAumento = salario1 * porcentagemTaxa3;
            aumentoPosReajuste = salarioAumento - (salarioAumento * inflacao);
        } else {
            salarioReajuste = salario1 * (1 + porcentagemTaxa4);
            porcentagemAumento = porcentagemTaxa4 * 100;
            salarioAumento = salario1 * porcentagemTaxa4;
            aumentoPosReajuste = salarioAumento - (salarioAumento * inflacao);
        }

        // Exibe os resultados
        System.out.println("Salário antes do reajuste: R$ " + salario1);
        System.out.println("Percentual de aumento aplicado: " + (porcentagemAumento + 3) + "%");
        System.out.println("Valor do aumento: R$ " + salarioAumento);
        System.out.println("Salário após o aumento: R$ " + salarioReajuste);
        System.out.println("Valor do aumento após reajuste, descontando a inflação: R$ " + aumentoPosReajuste);

        // Fecha o scanner
        scanner.close();
    }
}

