# 12.-Constructor-Overloading

Aim: To study and implement types of Overloading.

Tools Used: VS Code or Programiz online compiler.

# Theory

## Overloading in Cpp
Overloading in C++ is a feature that allows the same function name or operator to be used with different meanings based on the input parameters. It improves code readability and reusability. There are mainly three types: function overloading, constructor overloading, and operator overloading. In function and constructor overloading, multiple functions/constructors with the same name are defined but with different parameter lists. Operator overloading allows redefining operators like +, -, == for user-defined classes. Overall, overloading makes programs more intuitive and closer to natural usage.

**1. Function Overloading:**
Function overloading in C++ is a feature where two or more functions have the same name but differ in the number or type of parameters. The compiler decides which function to call based on the arguments passed. It helps in achieving compile-time polymorphism and improves code readability.

```

returnType functionName(parameter_list1);  
returnType functionName(parameter_list2);  

```


**2. Constructor Overloading:**
Constructor overloading in C++ is a feature where a class can have multiple constructors with the same name but different parameter lists. The compiler selects the appropriate constructor based on the arguments passed at the time of object creation. It allows objects to be initialized in different ways, improving flexibility and code reusability.

```

class ClassName {
public:
    ClassName();                  // Default constructor
    ClassName(int x);             // Parameterized constructor
    ClassName(int x, int y);      // Overloaded constructor
};

```



**3. Operator Overloading:**
Operator overloading in C++ is a feature that allows predefined operators like +, -, *, ==, etc., to be redefined and used with user-defined data types (classes/objects). It gives operators new meanings while keeping their original syntax, making code more intuitive. Operator overloading is a type of compile-time polymorphism.

```

returnType operator op (parameter_list) {
    // operator logic
}

```


# Program-1: Constructor Overloading (1st Code)
This program demonstrates constructor overloading in C++, where multiple constructors are defined with the same name but different parameter lists. The compiler decides which constructor to invoke based on the number and type of arguments passed during object creation. Here, one constructor adds two integers, another adds two floats, and the third adds three integers. This allows the same class to perform different initializations flexibly, showing compile-time polymorphism.

--> Algorithm:

1. Start the program.
2. Define a class Add with three constructors:
  --One that takes two integers and prints their sum.
  --One that takes two floats and prints their sum.
  --One that takes three integers and prints their sum.
3. In the main() function:
  --Create object a1 with two integer arguments → calls the integer constructor.
  --Create object a2 with two float arguments → calls the float constructor.
  --Create object a3 with three integer arguments → calls the 3-parameter constructor.
4. Display the results of each constructor call.
5. End the program.

# Program-2: Constructor Overloading (2nd Code)
This program demonstrates constructor overloading in C++ using a class Interest. Two constructors are defined: one to calculate simple interest using integer inputs, and another to calculate compound interest using double inputs. When an object is created, the compiler selects the constructor based on the type of arguments passed. This allows the same class to perform different types of interest calculations, showcasing compile-time polymorphism.

--> Algorithm:

1. Start the program.
2. Define a class Interest with two constructors:
  --Constructor 1: Takes three integers (p, r, n) and calculates Simple Interest using SI = (p*r*n)/100.
  --Constructor 2: Takes two doubles and an integer (p, r, n) and calculates Compound Interest using CI = p * (1 + r/100)^n - p.
3. In the main() function, create an object i1 with arguments (20000.123, 3.5, 2) → calls the compound interest constructor.
4. The constructor computes the interest and displays the result.
5. End the program.

# Program-3: Function Overloading 
This program demonstrates function overloading in C++, where the same function name Concatenate is defined with different parameter types. One version of the function takes two strings and concatenates them, while the other takes two characters and returns their combination as a string. The compiler determines which function to call based on the type of arguments passed. Function overloading allows performing similar operations on different data types using the same function name, improving code readability and reusability. This showcases compile-time polymorphism in C++.

--> Algorithm:

1. Start the program.
2. Define a class Concat with two functions named Concatenate:
  --Function 1: Takes two string arguments and returns their concatenation.
  --Function 2: Takes two char arguments, converts them to a string, and returns the result.
3. In the main() function, create an object c of class Concat.
4. Call c.Concatenate("Nishka", "Ranadive") → calls the string version of the function.
5. Call c.Concatenate('N', 'R') → calls the character version of the function.
6. Display the results of both function calls.
7. End the program.

# Program-4: Operator Overloading (1st Code)
This program demonstrates operator overloading in C++, where the * operator is redefined for the user-defined class Box. The overloaded * operator compares the volumes of two Box objects and returns true if the first box is larger. The class also includes a volume() function to calculate the volume of a box. By overloading the operator, objects of Box can be compared using a natural operator syntax instead of a separate function. This improves code readability and shows compile-time polymorphism, allowing operators to work with user-defined types.

--> Algorithm:

1. Start the program.
2. Define a class Box with three data members: length, width, and height.
3. Create a parameterized constructor to initialize the box dimensions.
4. Define a member function volume() to calculate the volume of a box.
5. Overload the * operator to compare the volumes of two Box objects and return true if the first box is larger.
6. In main(), create two Box objects b1 and b2 with given dimensions.
7. Display the volume of both boxes using the volume() function.
8. Use the overloaded * operator to compare b1 and b2 and display which box is bigger.
9. End the program.

# Program-5: Operator Overloading (2nd Code)
This program demonstrates operator overloading in C++, where the + operator is redefined for the user-defined class Number. The overloaded + operator adds the value of two Number objects and returns a new Number object with the sum. This allows the use of the natural + syntax to add objects instead of calling a separate function. The display() function is used to show the values of the objects. Operator overloading improves code readability and makes user-defined types behave like primitive types, showcasing compile-time polymorphism.

--> Algorithm:

1. Start the program.
2. Define a class Number with a data member value.
3. Create a parameterized constructor to initialize the value of the object.
4. Overload the + operator to add the value of two Number objects and return a new Number object with the result.
5. Define a display() function to print the value of a Number object.
6. In main(), create two Number objects n1 and n2 with given values.
7. Use the overloaded + operator to add n1 and n2 and store the result in n3.
8. Display the values of n1, n2, and n3 using the display() function.
9. End the program.

# Conclusion
All five programs demonstrate the concept of polymorphism in C++ using overloading. Programs 1 and 2 show constructor overloading, where multiple constructors with different parameters allow objects to be initialized in different ways, such as adding numbers or calculating interest. Program 3 illustrates function overloading, enabling the same function name to work with different data types like strings and characters. Programs 4 and 5 demonstrate operator overloading, allowing user-defined objects to use operators like * and + naturally, improving code readability. Overall, these examples show how overloading provides flexibility, code reusability, and intuitive syntax. They also showcase compile-time polymorphism, where the compiler decides which function, constructor, or operator to invoke based on the arguments. Overloading makes C++ programs more efficient, organized, and easier to maintain.
