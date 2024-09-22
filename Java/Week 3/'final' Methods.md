
- Prevents subclasses from overriding that method

- Often a parent class's setters are declared final

- Done to ensure that only the superclass can mutate its own fields, on its own terms
 
- Subclasses should never be able to "directly" change a superclass field except via super() calls in the constructor

- Subclass setters should likewise be made final