
# Factory Constructor?
### A factory constructor in Flutter is a special type of constructor that doesn't always create a new instance of its class. Instead, it may return an existing instance or even an instance of a different class. This flexibility allows developers to control the object creation process more precisely.

For example, a factory constructor can be used to implement a singleton pattern, where only one instance of a class is allowed to exist.
```
class Singleton {
  static Singleton _instance;

  factory Singleton() {
    if (_instance == null) {
      _instance = Singleton._privateConstructor();
    }
    return _instance;
  }

  Singleton._privateConstructor();
}
```

# Model Class?
### A model class is a blueprint for an object that encapsulates data and behaviour related to that data. In the context of a user model, it defines the attributes and methods associated with a user entity in your application. Creating a dedicated user model class helps in maintaining clean, modular, and readable code.

# Benefits of Using Model Classes
### 1. Code Organization: Model classes help in organizing your code by encapsulating data-related logic in a structured manner.

### 2. Code Reusability: Once you’ve defined a user model, you can reuse it throughout your application, promoting code reusability and reducing redundancy.

### 3. Readability: Using model classes enhances the readability of your code, making it easier for other developers (or even future you) to understand the structure of your data.

### 4. Maintenance: If your data structure evolves, you can make changes in one place (the model class) rather than scattering modifications across your entire codebase.

## Example :-
```
void main() {
  // Creating a new user
  User newUser = User(name: 'John Doe', age: 25, email: 'john@example.com');

  // Accessing user properties
  print('User Name: ${newUser.name}');
  print('User Age: ${newUser.age}');
  print('User Email: ${newUser.email}');
}
```
