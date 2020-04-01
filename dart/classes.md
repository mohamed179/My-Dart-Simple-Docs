# Classes

* [Define a class](#define-a-class)
* [Define a class](#class-properties)
* [Define a class](#class-methods)
* [Define a class](#class-constructor)
* [Define a class](#class-inheritance)

## Define a class

You can define a new class using the following syntax

```dart
class class_name {
    class_content...
}
```

**Example:**

```dart
class Person {
    int age = 25;
    String name = 'Mohamed';
}
```

## Class properties

Any Dart class has its own properties (variables)

**Example:**

```dart
class Person {
    int age = 25;
    String name = 'Mohamed';
}
```

## Class methods

Any Dart class has its own methods (functions)

**Example:**

```dart
class Bird {
    void fly() {
        print('flying...');
    }
}
```

## Class constructor

Class constructor is a special method inside the class called once and used to initialize object created from this class.

You can add a constructor to a class using this syntax

```dart
class class_name {
    class_name (constructor_parameters...) {
        constructor_body...
    }
}
```

**Example:**

```dart
class Person {
    String name;
    int age;
    
    Person (String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

### Constructor name parameters

There is another constructor syntax

```dart
class class_name {
    property_name,
    another_property_name,
    ...

    class_name ({this.property_name, this.another_property_name,...});
}
```

**Example:**

```dart
class Person {
    String name;
    int age;
    
    Person ({this.name, this.age});
}
```

## Class inheritance

A class can inherit another class taking its all functionality

You can use the functionality of inheritance using the following syntax:

```dart
class parent_class_name {
    parent_class_body...
}

class child_class_name extends parent_class_name {
    child_class_body...
}
```

**Example:**

```dart
class A {
    String str = 'Some text!';
    void printStr() {
        print(this.str);
    }
}

class B {
    int number = 10;
    void printNumber() {
        print(this.number);
    }
}

void main () {
    var a = A();
    var b = B();
    a.printStr();
    b.printStr();
    b.printNumber();
}
```