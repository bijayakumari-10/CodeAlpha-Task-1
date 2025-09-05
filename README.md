import java.util.Scanner;  // Import Scanner for user input

public class GradeTracker {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);  // Create Scanner object

        // Ask user for number of students
        System.out.print("How many students? ");
        int n = sc.nextInt();  // Read number of students

        int[] grades = new int[n];  // Create array to store grades
        int sum = 0;  // Variable to store total of grades
        int highest, lowest;  // To store highest and lowest grades

        // Input grades from user
        for (int i = 0; i < n; i++) {
            System.out.print("Enter grade " + (i + 1) + ": ");
            grades[i] = sc.nextInt();  // Store grade in array
            sum += grades[i];  // Add grade to sum
        }

        // Initialize highest and lowest with the first grade
        highest = lowest = grades[0];

        // Loop to find highest and lowest grades
        for (int i = 1; i < n; i++) {
            if (grades[i] > highest)
                highest = grades[i];  // Update highest
            if (grades[i] < lowest)
                lowest = grades[i];  // Update lowest
        }

        // Calculate average
        double average = (double) sum / n;

        // Display results
        System.out.println("\n--- Grade Summary ---");
        System.out.println("Average: " + average);
        System.out.println("Highest: " + highest);
        System.out.println("Lowest: " + lowest);
    }
}
