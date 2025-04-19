import java.util.*;

class Employee {
    String name;
    int age;
    double salary;

    Employee(String name, int age, double salary) {
        this.name = name;
        this.age = age;
        this.salary = salary;
    }

    @Override
    public String toString() {
        return name + " | " + age + " | " + salary;
    }
}

public class EmployeeSort {
    public static void main(String[] args) {
        List<Employee> employees = Arrays.asList(
            new Employee("Alice", 30, 50000),
            new Employee("Bob", 25, 45000),
            new Employee("Charlie", 28, 55000)
        );

        // Sort by name using lambda
        employees.sort((e1, e2) -> e1.name.compareTo(e2.name));

        System.out.println("Sorted by Name:");
        employees.forEach(System.out::println);

        // Sort by salary using lambda
        employees.sort((e1, e2) -> Double.compare(e1.salary, e2.salary));

        System.out.println("\nSorted by Salary:");
        employees.forEach(System.out::println);
    }
}
