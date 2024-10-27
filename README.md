# https://github.com/Qba3/java-laby/blob/laby/lab1/README.md
# Zad1
Komenda i wynik:
```
java -version
```
```
java version "23.0.1" 2024-10-15
Java(TM) SE Runtime Environment (build 23.0.1+11-39)
Java HotSpot(TM) 64-Bit Server VM (build 23.0.1+11-39, mixed mode, sharing)

```
# Zad2
```
public class Shape {
    public void print() {
        System.out.println("Name of Class: " + this.getClass().getSimpleName());
    }
    public static void main(String[] args) {
        Shape shape = new Shape();
        shape.print();
    }
}
```

Kompilacja, uruchomienie:
```
javac src/Shape.java
java src/Shape.java
```
Wynik:
```
Name of Class: Shape
```
# Zad3
```
abstract class Shape {
    public void displayName() {
        System.out.println("Class name: " + this.getClass().getSimpleName());
    }
    public abstract double calculateArea();
    public abstract double calculatePerimeter();
}

class Rectangle extends Shape {
    private double length;
    private double height;

    public Rectangle(double length, double breadth) {
        this.length = length;
        this.height = breadth;
    }

    @Override
    public double calculateArea() {
        return length * height;
    }

    @Override
    public double calculatePerimeter() {
        return 2 * (length + height);
    }
}

class Triangle extends Shape {
    private double a;
    private double b;
    private double c;

    public Triangle(double sideA, double sideB, double sideC) {
        this.a = sideA;
        this.b = sideB;
        this.c = sideC;
    }

    @Override
    public double calculateArea() {
        double semiPerimeter = calculatePerimeter() / 2;
        return Math.sqrt(semiPerimeter * (semiPerimeter - a) * (semiPerimeter - b) * (semiPerimeter - c));
    }

    @Override
    public double calculatePerimeter() {
        return a + b + c;
    }
}

class ShapeDescriber {
    public static void describeShape(Shape shape) {
        System.out.println("Area: " + shape.calculateArea());
        System.out.println("Perimeter: " + shape.calculatePerimeter());
    }
}

public class Main {

    public static void main(String[] args) {
        Shape rectangle = new Rectangle(5, 7);
        Shape triangle = new Triangle(3, 2, 3);

        ShapeDescriber.describeShape(rectangle);
        ShapeDescriber.describeShape(triangle);
    }
}
```
