import java.util.*;
public class Calcu {
    public static void main(String[] args) {
        Scanner scan=new Scanner(System.in);
        System.out.println("""
                                         Calculator 1.1
                ------------------------------------------------------------------
                """);
        System.out.println("Please enter your first number:");
        double n1 = scan.nextDouble();
        System.out.println("""
                Please choose an operator by typing the number provided beside it:
                1. Addition
                2. Subtraction
                3. Multiplication
                4. Division
                If none, then type 0 to exit the program.
                """);
        int choice = scan.nextInt();
        System.out.println("Please enter your second number:");
        double n2 = scan.nextDouble();

        switch (choice){
            case 1:
                System.out.print(n1+" + "+n2+" = "+add(n1,n2));
                break;
            case 2:
                System.out.println(n1+" - "+n2+" = "+minus(n1,n2));
                break;
            case 3:
                System.out.println(n1+" x "+n2+" = "+multiply(n1,n2));
                break;
            case 4:
                if (n1 != 0 && n2!= 0) {
                    System.out.print(n1 + " / " + n2 + " = " + divide(n1,n2));
                }
                else {
                    System.out.println("Error not found");
                }
                break;
            case 0:
                System.out.print("Thanks for choosing Calculator 1.1!");
                break;
            default:
                System.out.println("Error not found");
        }

    }
    
    static double add(double n1, double n2) {
        return n1 + n2;
    }
    static double minus(double n1, double n2) {
        return n1 - n2;
    }
    static double multiply(double n1, double n2) {
        return n1 * n2;
    }
    static double divide(double n1, double n2) {
        return n1 / n2;
    }
}
