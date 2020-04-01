# Functions

* [Defining a function](#defining-a-function)
* [Void return type](#defining-a-function)
* [Calling a function](#calling-a-function)
* [Main function](#main-function)

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