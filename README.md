# Java-Abstract-Lab-Section-12

## Step 1: Abstract Good

Currently, the Good class allows instances of a Good to be created. In actuality, this
class serves as a template for the subclasses (Solid and Liquid), so instances of a
Good should not be created. For instance, consider the volume method on Good.
What is the volume of such a nebulous object?

### 1.1 Make Good abstract. In the Package Explorer view, double-click on the
Good.java file in the com.acme.domain package to open the file in a Java
editor. Use the “abstract” key word to make this class abstract.

```java
public abstract class Good {
...
}
```

### 1.2 Make the volume( ) method abstract in Good. Remove the current
implementation of the volume( ) method in Good, and replace it with an
abstract definition (see below). Making this method abstract forces the
Solid and Liquid classes to implement and override volume( ).

```java
public abstract double volume();
```

### 1.3 Save Good.java and run the TestOrders.java file to ensure your application
still works the same way.

### 1.4 Try to create an instance of Good.

1.4.1 In the main method of TestOrders.java, try to create an instance of the now
abstract Good.
```java
Good g = new Good("Acme Earthquake Pills", 1304, 0.15,
UnitOfMeasureType.CUBIC_FEET, false, 1);
```
1.4.2 This will also require you import the Good class.
```java
import com.acme.domain.Good;
```
1.4.3 You should get a compiler error that prevents an instance of Good from
being created.

<img src="./src/main/resources/compilerErrorGood.PNG" width="800px">
