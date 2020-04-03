# Arrays

* [Define an array](#define-an-array)
* [Accessing array elements](#define-an-array)

## Define an array

You can create new array by using the following syntax:

```dart
var array_name = <optional_array_type> [array_elements];
```

**Example:**

```dart
void main () {
    var names = <String> [
        "Mohamed",
        "Kamal",
        "Zaki"
    ];
    print(names);

    var numbers = [1, 2, 3];
    print(numbers);
}
```

## Accessing array elements

You can access an array element by the following syntax:

```dart
array_name[element_index];
array_name[element_index] = new_value;
```

**Example:**

```dart
void main () {
    var names = [
        "Mohamed",
        "Kamal",
        "Zaki"
    ];
    print(names[1]);
    names[0] = "Ahmed";
    print(names[0]);
}
```