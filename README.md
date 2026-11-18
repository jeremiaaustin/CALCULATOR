# CALCULATOR
basic build calculator by JEREMIA AUSTIN SIHOMBING
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        double angka1, angka2, hasil;
        char operator;

        System.out.println("===== JAVA CALCULATOR =====");

        System.out.print("Masukkan angka pertama: ");
        angka1 = input.nextInt();

        System.out.print("Masukkan operator (+, -, *, /): ");
        operator = input.next().charAt(0);

        System.out.print("Masukkan angka kedua: ");
        angka2 = input.nextInt();

        switch (operator) {

            case '+':
                hasil = angka1 + angka2;
                break;

            case '-':
                hasil = angka1 - angka2;
                break;

            case '*':
                hasil = angka1 * angka2;
                break;

            case '/':
                if (angka2 != 0)
                    //!=0 artinya tidak boleh dibagi dengan nol 
                {
                    hasil = angka1 / angka2;
                } else {
                    System.out.println("Tidak bisa dibagi nol!");
                    input.close();
                    return;
                }
                break;

            default:
                System.out.println("Operator tidak valid!");
                input.close();
                return;
            }
        

        System.out.println("Hasil: " + hasil);

        input.close();
    }
}
