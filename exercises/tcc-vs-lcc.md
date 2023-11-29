# TCC *vs* LCC

Explain under which circumstances *Tight Class Cohesion* (TCC) and *Loose Class Cohesion* (LCC) metrics produce the same value for a given Java class. Build an example of such as class and include the code below or find one example in an open-source project from Github and include the link to the class below. Could LCC be lower than TCC for any given class? Explain.

## Answer

## Circumstances where TCC and LCC Metrics Produce the Same Value

Tight Class Cohesion (TCC) and Loose Class Cohesion (LCC) metrics can produce the same value for a given Java class when all methods within the class have dependencies solely among themselves. In other words, if there are no dependencies or interactions between methods from different classes, both TCC and LCC will yield identical values.

### Example

Consider the following Java class where all methods are self-contained and have no dependencies on methods from other classes:

```
public class SelfContainedClass {
    public void method1() {
        // Implementation of method 1
    }

    public void method2() {
        // Implementation of method 2
    }

    // Additional methods...
}
```

In this example, both TCC and LCC metrics will be equal since there are no method dependencies on external classes. No method relies on data from other classes or methods outside this class.

## Can LCC be Lower than TCC for a Given Class
No, in a valid scenario, LCC cannot be lower than TCC for a given class. TCC measures the tightness of relationships between methods within a class, while LCC measures the loose coupling between methods. LCC encompasses TCC and additional factors such as relationships with external classes.

Since TCC focuses only on internal method dependencies within a class, it's a subset of LCC. Therefore, LCC will always be greater than or equal to TCC for any valid class design. If LCC were lower than TCC, it would indicate a contradiction in the cohesion metrics, implying that the class's internal cohesion is stronger than its overall cohesion, which is not a typical scenario.
