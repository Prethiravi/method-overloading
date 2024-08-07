public class MethodOverloadingDemo {

    // Method with two integer parameters
    public int add(int a, int b) {
        return a + b;
    }

    // Method with three integer parameters
    public int add(int a, int b, int c) {
        return a + b + c;
    }

    // Method with two double parameters
    public double add(double a, double b) {
        return a + b;
    }

    // Method with one integer parameter
    public void show(int a) {
        System.out.println("Integer: " + a);
    }

    // Method with one double parameter
    public void show(double a) {
        System.out.println("Double: " + a);
    }

    // Method with one string parameter
    public void show(String a) {
        System.out.println("String: " + a);
    }

    // Method with no parameters
    public void sayHello() {
        System.out.println("Hello!");
    }

    // Method with one parameter
    public void sayHello(String name) {
        System.out.println("Hello, " + name + "!");
    }

    // Method with two parameters
    public void sayHello(String name, int age) {
        System.out.println("Hello, " + name + "! You are " + age + " years old.");
    }

    // Method with two parameters: int and String
    public void print(int a, String b) {
        System.out.println("Integer: " + a + ", String: " + b);
    }

    // Method with two parameters: String and int
    public void print(String a, int b) {
        System.out.println("String: " + a + ", Integer: " + b);
    }

    public static void main(String[] args) {
        MethodOverloadingDemo demo = new MethodOverloadingDemo();

        // Testing add methods
        System.out.println("Sum of 2 and 3: " + demo.add(2, 3));                // Uses add(int, int)
        System.out.println("Sum of 2, 3, and 4: " + demo.add(2, 3, 4));        // Uses add(int, int, int)
        System.out.println("Sum of 2.5 and 3.5: " + demo.add(2.5, 3.5));       // Uses add(double, double)

        // Testing show methods
        demo.show(5);           // Uses show(int)
        demo.show(5.5);         // Uses show(double)
        demo.show("Hello");     // Uses show(String)

        // Testing sayHello methods
        demo.sayHello();                     // Uses sayHello()
        demo.sayHello("Alice");              // Uses sayHello(String)
        demo.sayHello("Bob", 30);            // Uses sayHello(String, int)

        // Testing print methods
        demo.print(10, "Ten");      // Uses print(int, String)
        demo.print("Twenty", 20);   // Uses print(String, int)
    }
}
