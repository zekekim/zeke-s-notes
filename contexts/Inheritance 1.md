---
context: cs1c
date: 2022-10-03
---

# Inheritance 1

1. Implement the program as described. Explain your results.

```
Base
Base
Base
```

The print function that is used is the one found in the `Base` class. Since each object is passed in as a `Base` object in the `printClass` function, the object is a derived object, however it is treated as a `Base` object because it is defined at compile time,

3. Change the print() member function to be virtual. Run the program again and explain your results.

```
Base
Base
Base
```

Since the `print` function is now virtual, it is now being overriden by the other instances of print in their respective inherited classes. However, since the object is specified as a base object, it is treated as one inside the `printClass` function because it is copied as a `Base` object through the parameters.

2. Change printClass() function so that its argument is passed by reference. Run the program again and explain your results.

```
Base
Child
Grandchild
```

Since the object is now being passed by reference instead of being copied in the parameter of the function, it is now being treated as its instantiated class type and by using overriding instead of redefining, the child and grandchild class are using their print functions.

3. Add an integer member to the Base class. Provide a constructor which initializes this member from its argument. Why does the program not compile? What is the best way to solve this problem?

This program doesn't compile since the inherited classes have no way of initializing the member from the base class. To fix this one could create a default constructor for the base class or initialize the base class using its initializer through inheritance in the child and grandchild class.