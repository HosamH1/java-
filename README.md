# Java Access Modifiers Guide

Java supports four access modifiers: `public`, `protected`, `default` (no modifier), and `private`. These determine the visibility and accessibility of classes, methods, and variables.

## Access Modifiers

### 1. Public

- **Description**: Accessible from any other class in any package. Provides the widest accessibility.
- **Example**:

```java
public class PublicExample {
    public void display() {
        System.out.println("Public access modifier example.");
    }
}

2. Protected

    Description: Accessible within its own package and by subclasses (including those in different packages). More accessible than default but more restrictive than public.
    Example:
// In packageOne/ProtectedExample.java
package packageOne;

public class ProtectedExample {
    protected void display() {
        System.out.println("Protected access modifier example.");
    }
}

// In packageTwo/ExampleSubclass.java
package packageTwo;
import packageOne.ProtectedExample;

class ExampleSubclass extends ProtectedExample {
    public static void main(String[] args) {
        ExampleSubclass obj = new ExampleSubclass();
        obj.display(); // Accessible
    }
}

Default (No Modifier)

    Description: Accessible only within its own package. More restrictive than protected.
    Example:
// In packageOne/DefaultExample.java
package packageOne;

class DefaultExample {
    void display() {
        System.out.println("Default (package-private) access modifier example.");
    }
}

4. Private

    Description: Accessible only within the class it is declared. Most restrictive access.
    Example:
public class PrivateExample {
    private void display() {
        System.out.println("Private access modifier example.");
    }

    public static void main(String[] args) {
        PrivateExample obj = new PrivateExample();
        obj.display(); // Accessible only within the same class
    }
}

Summary

    Public: No restrictions on access.
    Protected: Package + subclasses.
    Default (No Modifier): Package only.
    Private: Class only.

Each access modifier serves a specific purpose in controlling the visibility and accessibility of components in Java, aiding in encapsulation and object-oriented design principles.
