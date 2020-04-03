# Functions

* [Defining a function](#defining-a-function)
* [Void return type](#defining-a-function)
* [Calling a function](#calling-a-function)
* [Main function](#main-function)
* [Named parameters (Default parameters)](#named-parameters-default-parameters)
* [One statement body function](#one-statement-body-function)
* [Functions as arguments](#functions-as-arguments)
* [Anonymous functions](#anonymous-functions)

## Defining a function

You can define a function in the following syntax

```dart
return_type function_name (parameters...) {
    function_body...
}
```

**Example:**

```dart
int add (int x, int y) {
    return x + y;
}
```

## Void return type

If the function should return nothing, then the return type must be `void`

**Example**

```dart
void printString (String str) {
    print(str);
}
```

## Calling a function

You can call a function as following example

**Example**

```dart
int add (int x, int y) {
    return x + y;
}

void main () {
    var x = add(1, 3);
    print(x);
}
```

## Main function

Dart run main function as the root of any dart program

**Example**

```dart
void main () {
    // your program start here...
}
```

## Named parameters (Default parameters)

You can add function named parameters (default parameters) in dart by using the following syntax

```dart
return_type function_name (none_named_parameters..., {named_parameters...}) {
    function_body...
}
...
function_name(pareter_name: parameter_value, ...);
```

**Example:**

```dart
void printThose (int firstNum, {int secondNum = 0}) {
    print(firstNum);
    print(secondNum);
}

void main () {
    printThose(7, secondNum: 10);
    printThose(20);
}
```

## One statement body function

If your function body has only one statement, then you can use the following syntax to define your function

```dart
return_type function_name (parameters...) => statement;
```

**Example:**

```dart
int addOne (int x) => x + 1;

void printX (int x) => print(x);

void main () {
  int x = addOne(4);
  printX(x);
}
```

## Functions as arguments

You can send a function (not its return) to another function as an argument

The other function then will call your function (use it).

> You have to define your function as required from the other function that will use your function

To send a function as an argument to another function, use the following syntax:

```dart
another_function_name(some_parameters..., your_function_name, ohter_parameters...);
```

**Example:**

```dart
void fly () => print('flying...');

void run () => print('running...');

void perform (activity) => activity();

void main () {
    perform(run);
    perform(fly);
}
```

## Anonymous functions

Anonymous functions are functions that has no name.

You can assign an variable an anonymous function by using the following syntax:

```dart
var variable_name = (parameters...) {
    function_body...
}

var variable_name = (parameters...) => statement;
```

**Example:**

```dart
var fly = () => print('flying...');

var run = () => print('running...');

void main () {
    fly();
    run();
}
```

You can send an anonymous function as an argument to another function by using the following syntax:

```dart
another_function_name(
    some_parameters...,
    (anonymous_function_parameters...) {
        anonymous_function_body...
    },
    ohter_parameters...
);
```

But if the anonymous function has only one statement in its body, you can use the following syntax: 

```dart
another_function_name(
    some_parameters...,
    (anonymous_function_parameters...) => statement,
    ohter_parameters...
);
```

**Example:**

```dart
void main () {
    var perform = (name, activity) {
        activity(name);
    };
    perform(
        'A bird',
        (animal) {
            print(animal + ' is flying...'); 
        }
    );
    perform(
        'Mohamed',
        (personName) => print(personName + ' is running...')
    );
}
```