import java.util.*;
import java.util.stream.Collectors;

class Student {
    String name;
    double marks;

    Student(String name, double marks) {
        this.name = name;
        this.marks = marks;
    }
}

public class StudentFilterSort {
    public static void main(String[] args) {
        List<Student> students = Arrays.asList(
            new Student("Aman", 82.5),
            new Student("Riya", 74.0),
            new Student("Karan", 91.2),
            new Student("Sneha", 65.3),
            new Student("Tina", 78.9)
        );

        List<String> filteredAndSorted = students.stream()
            .filter(student -> student.marks > 75)
            .sorted((s1, s2) -> Double.compare(s2.marks, s1.marks)) // descending order
            .map(student -> student.name)
            .collect(Collectors.toList());

        System.out.println("Students scoring above 75%:");
        filteredAndSorted.forEach(System.out::println);
    }
}
