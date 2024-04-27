 **
 * Calculator program in Java with basic arithmetic operations.
 */
public class Calculator {

    /**
     * Adds two numbers.
     *
     * @param num1 The first number to be added.
     * @param num2 The second number to be added.
     * @return The sum of num1 and num2.
     */
    public static double add(double num1, double num2) {
        return num1 + num2;
    }

    /**
     * Subtracts the second number from the first number.
     *
     * @param num1 The number from which num2 will be subtracted.
     * @param num2 The number to be subtracted from num1.
     * @return The result of num1 minus num2.
     */
    public static double subtract(double num1, double num2) {
        return num1 - num2;
    }

    /**
     * Multiplies two numbers.
     *
     * @param num1 The first number to be multiplied.
     * @param num2 The second number to be multiplied.
     * @return The product of num1 and num2.
     */
    public static double multiply(double num1, double num2) {
        return num1 * num2;
    }

    /**
     * Divides the first number by the second number.
     *
     * @param num1 The numerator.
     * @param num2 The denominator (should not be zero).
     * @return The result of num1 divided by num2.
     * @throws ArithmeticException if num2 is zero.
     */
    public static double divide(double num1, double num2) {
        if (num2 == 0) {
            throw new ArithmeticException("Cannot divide by zero.");
        }
        return num1 / num2;
    }

    public static void main(String[] args) {
        /** Example usage: */
        double operand1 = 10.0;
        double operand2 = 5.0;

        /** Addition */
        double sum = add(operand1, operand2);
        System.out.println("Sum: " + sum);

        /** Subtraction */
        double difference = subtract(operand1, operand2);
        System.out.println("Difference: " + difference);

        /* Multiplication */
        double product = multiply(operand1, operand2);
        System.out.println("Product: " + product);

        /** Division */
        try {
            double quotient = divide(operand1, operand2);
            System.out.println("Quotient: " + quotient);
        } catch (ArithmeticException e) {
            System.out.println(e.getMessage());
        }
    }
}
