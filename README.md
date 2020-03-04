# Effective Java, Third Edition
![EJ3e Book Cover](https://www.pearsonhighered.com/assets/bigcovers/0/1/3/4/0134685997.jpg)

## Chapter-2

### Consider static methods instead of constructors

A class can provide a public static factory method (not related with factory method of design patterns) which is simply a static method that returns an instance of the class. Can be provided instead of, or in addition to public constructors.  
A class can have only a single constructor with a given signature. (a method's signature: its name and the types of parameters. no return type.)

```java
public static Boolean valueOf(boolean b) {
  return b ? Boolean.TRUE : Boolean.FALSE;
}
```

Unlike constructors;
- They have names.
- They're not required to create a new object each time they're invoked.
- They can return an object of any subtype of their return type.
- The class of the returned object can vary from call to call as a function of the input parameters.

Some common names for static factory methods:

- from:
```java
  Date d = new Date().from(instant);
```

- of:
```java
Set<Rank> faceCards = EnumSet.of(JACK, QUEEN, KING);
```

- valueOf:
```java
BigInteger prime = BigInteger.valueOf(Integer.MAX_VALUE);
```
- instance/getInstance, create/newInstance, getType, newType, type etc.



