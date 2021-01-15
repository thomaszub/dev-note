# Visitor

The visitor pattern separates algorithms from the object structures they work on.
If supported, this can be done by double dispatch or reflection.

## Java

In Java this can be done with the following interfaces including return value and exception propagation:
```java
public interface Visitor<R, E extends Throwable> {

    R visit(ConcreteNode1 node) throws E;

    R visit(ConcreteNode2 node) throws E;

    ...

}

public interface Node {

    <R, E extends Throwable> R accept(Visitor<R, E> visitor) throws E;

}

//Example of concrete implementation

public class ConcreteNode1 implements Node {
    
    public <R, E extends Throwable> R accept(Visitor<R, E> visitor) throws E {
        return visitor.visit(this);
    }

    ...

}
```
The implementation for a concrete node looks always the same and allows passing Void for R if no returned value is needed.
