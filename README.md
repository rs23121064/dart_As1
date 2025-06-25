# dart_As1
assignment 01
//questions 
a)Create an abstract class Vehicle with:
A protected variable _speed.
An abstract method move().
A non-abstract method setSpeed(int speed) to set the speed.

b)Create a subclass Car that extends Vehicle:
Implement the move() method to print "The car is moving at $_speed km/h".

c)Use encapsulation to prevent direct access to _speed.

d)In the main function, create an object of Car, set the speed, and call the move() method.


//Answers

// (a) Abstract class
abstract class Vehicle {
  int _speed = 0;

  void setSpeed(int speed) {
    _speed = speed;
  }

  int get speed => _speed;
  void move(); // abstract method
}

// (b) Subclass Car
class Car extends Vehicle {
  @override
  void move() {
    print("The car is moving at ${speed} km/h");
  }
}
// (c) abstract class Vehicle {
  int _speed = 0; // Step 1: private variable

  void setSpeed(int speed) { // Step 2: setter
    _speed = speed;
  }

  int get speed => _speed; // Step 3: getter

  void move(); // abstract method
}
// (d) Main function
void main() {
  Car myCar = Car();
  myCar.setSpeed(80);
  myCar.move();
}

