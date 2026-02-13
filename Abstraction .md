# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
```
from abc import ABC, abstractmethod
import math

class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass

class Rectangle(Shape):
    def __init__(self, length=5, breadth=10):
        self.length = length
        self.breadth = breadth
    
    def calculate_area(self):
        area = self.length * self.breadth
        print("Area of Rectangle:", area)

class Circle(Shape):
    def __init__(self, radius=7):
        self.radius = radius
    
    def calculate_area(self):
        area = math.pi * self.radius ** 2
        print("Area of Circle:", area)

# Create objects
rect = Rectangle()
circ = Circle()

# Call methods
rect.calculate_area()
circ.calculate_area()

```
## Output
<img width="413" height="178" alt="image" src="https://github.com/user-attachments/assets/bfafe6ed-24a9-4371-9352-3c1cafd43c2a" />

## Result
The program demonstrates an abstract class Shape with the abstract method calculate_area(), which is implemented by Rectangle and Circle to calculate and display their respective areas.
