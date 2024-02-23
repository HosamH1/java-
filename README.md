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
