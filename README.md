import java.util.ArrayList;
import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class StudentRecordsManager {
    public static void main(String[] args) {
        ArrayList<Map<String, Object>> students = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.println("1. Add Student");
            System.out.println("2. Remove Student");
            System.out.println("3. Record Grades");
            System.out.println("4. Calculate GPA");
            System.out.println("5. Generate Report");
            System.out.println("6. Exit");

            System.out.print("Enter your choice: ");
            int choice = scanner.nextInt();
            scanner.nextLine(); // Consume the newline character

            if (choice == 1) {
                System.out.print("Enter student name: ");
                String name = scanner.nextLine();
                Map<String, Object> student = new HashMap<>();
                student.put("name", name);
                student.put("grades", new HashMap<String, Integer>());
                students.add(student);
                System.out.println("Student added successfully.");
            } else if (choice == 2) {
                System.out.print("Enter student name to remove: ");
                String name = scanner.nextLine();
                students.removeIf(s -> s.get("name").equals(name));
                System.out.println("Student removed successfully.");
            } else if (choice == 3) {
                // Implement recording grades
            } else if (choice == 4) {
                // Implement calculating GPA
            } else if (choice == 5) {
                // Implement generating report
            } else if (choice == 6) {
                System.out.println("Exiting the program. Goodbye!");
                System.exit(0);
            } else {
                System.out.println("Invalid choice. Please enter a valid option.");
            }
        }
    }
}
