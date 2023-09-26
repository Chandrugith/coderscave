# coderscave
import java.util.Scanner;

public class BMICalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("BMI Calculator");
        System.out.print("Enter your weight in kilograms: ");
        double weight = scanner.nextDouble();

        System.out.print("Enter your height in meters: ");
        double height = scanner.nextDouble();

        double bmi = calculateBMI(weight, height);
        String category = interpretBMI(bmi);

        System.out.println("Your BMI is: " + bmi);
        System.out.println("BMI Category: " + category);

        scanner.close();
    }

    public static double calculateBMI(double weight, double height) {
        return weight / (height * height);
    }

    public static String interpretBMI(double bmi) {
        if (bmi < 16) {
            return "Severely underweight";
        } else if (bmi >= 16 && bmi < 16.9) {
            return "Underweight";
        } else if (bmi >= 17 && bmi < 18.4) {
            return "Mildly underweight";
        } else if (bmi >= 18.5 && bmi < 24.9) {
            return "Normal";
        } else if (bmi >= 25 && bmi < 29.9) {
            return "Overweight";
        } else if (bmi >= 30 && bmi < 34.9) {
            return "Obese (Class I)";
        } else if (bmi >= 35 && bmi < 39.9) {
            return "Obese (Class II)";
        } else {
            return "Severely obese (Class III)";
        }
    }
}
