import java.util.Scanner;

public class Calculadora {

    //a e b São os numeros utilizados.
    public static double adicao (double a, double b){
        return a + b;
    }
    public static double subtracao (double a, double b){
        return a - b;
    }
    public static double multiplicacao (double a, double b){
        return a * b;
    }
    public static double divisao (double a, double b){
        return a / b;
    }


    public static void main(String[] args) {

        Scanner leia = new Scanner(System.in);

       int opcao;
       double num1;
       double num2;

       do {
           System.out.println("  ");
           System.out.println("ESCOLHA UMA OPERAÇÃO");
           System.out.println("1-Adição");
           System.out.println("2-Subtração");
           System.out.println("3-Multiplicação");
           System.out.println("4-Divisão");
           System.out.println("0-Sair");
           System.out.println("Digite sua escolha: ");
           opcao = leia.nextInt();
           if (opcao >= 1 && opcao <= 4){

           System.out.println("Escreva o primeiro numero");
           num1 = leia.nextDouble();
           System.out.println("digite o segundo numero");
           num2 = leia.nextDouble();

           double resultado = 0;

           switch (opcao) {
               case 1:
                   resultado = adicao(num1, num2);
                   System.out.println("resultado: " + resultado);
                   break;
               case 2:
                   resultado = subtracao(num1, num2);
                   System.out.println("resultado: " + resultado);
                   break;
               case 3:
                   resultado = multiplicacao(num1, num2);
                   System.out.println("resultado: " + resultado);
                   break;
               case 4:
                   resultado = divisao(num1, num2);
                   if (num2 != 0) {
                       System.out.println("resultado: " + resultado);
                   }

           }
       }else if (opcao != 0){
               System.out.println("opção invalida tente novamente");
           }

       }while (opcao != 0);
        System.out.println("fim do calculo");

        leia.close();

    }
}
