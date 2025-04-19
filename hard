import java.util.*;
import java.util.stream.Collectors;

class Product {
    String name;
    String category;
    double price;

    Product(String name, String category, double price) {
        this.name = name;
        this.category = category;
        this.price = price;
    }

    @Override
    public String toString() {
        return name + " | " + category + " | " + price;
    }
}

public class ProductStreamOperations {
    public static void main(String[] args) {
        List<Product> products = Arrays.asList(
            new Product("Laptop", "Electronics", 1200),
            new Product("Phone", "Electronics", 800),
            new Product("Jeans", "Clothing", 40),
            new Product("T-shirt", "Clothing", 20),
            new Product("Blender", "Home Appliances", 100),
            new Product("Microwave", "Home Appliances", 200)
        );

        // Group products by category
        Map<String, List<Product>> groupedByCategory = products.stream()
            .collect(Collectors.groupingBy(product -> product.category));

        System.out.println("Products grouped by category:");
        groupedByCategory.forEach((category, prodList) -> {
            System.out.println(category + ": " + prodList);
        });

        // Find the most expensive product in each category
        Map<String, Optional<Product>> mostExpensiveProductByCategory = products.stream()
            .collect(Collectors.groupingBy(
                product -> product.category,
                Collectors.maxBy(Comparator.comparingDouble(product -> product.price))
            ));

        System.out.println("\nMost expensive product in each category:");
        mostExpensiveProductByCategory.forEach((category, product) -> {
            System.out.println(category + ": " + product.orElse(null));
        });

        // Calculate the average price of all products
        double averagePrice = products.stream()
            .mapToDouble(product -> product.price)
            .average()
            .orElse(0.0);

        System.out.println("\nAverage price of all products: " + averagePrice);
    }
}
