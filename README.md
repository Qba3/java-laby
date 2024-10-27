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

```
