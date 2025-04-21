# Python-week-5-classes-
Assignment 1: Design Your Own Class!
# Base class representing a generic character
class Character:
    def __init__(self, name, age, power):
        self.name = name
        self.age = age
        self.power = power

    def introduce(self):
        return f"I am {self.name}, aged {self.age}. My main power is {self.power}!"

    def use_power(self):
        return f"{self.name} is using their power: {self.power}!"

# Derived class representing a Superhero
class Superhero(Character):
    def __init__(self, name, age, power, alias, affiliation):
        super().__init__(name, age, power)
        self.alias = alias
        self.affiliation = affiliation

    def introduce(self):
        return f"Superhero {self.alias}, part of {self.affiliation}, is here to save the day!"

    def use_power(self):
        return f"{self.alias} demonstrates heroic mastery with {self.power}!"

# Derived class representing a Villain
class Villain(Character):
    def __init__(self, name, age, power, nemesis):
        super().__init__(name, age, power)
        self.nemesis = nemesis

    def introduce(self):
        return f"I am the dreaded {self.name}, and my nemesis is {self.nemesis}!"

    def use_power(self):
        return f"{self.name} unleashes their sinister power: {self.power}!"

# Example objects
superhero = Superhero("Clark Kent", 30, "Super Strength", "Superman", "Justice League")
villain = Villain("Lex Luthor", 45, "Genius Intellect", "Superman")

# Example outputs
print(superhero.introduce())
print(superhero.use_power())
print(villain.introduce())
print(villain.use_power())

Assignment two::
# Base class
class Vehicle:
    def move(self):
        raise NotImplementedError("This method should be overridden by subclasses")

# Derived class representing a Car
class Car(Vehicle):
    def move(self):
        return "Driving 🚗"

# Derived class representing a Plane
class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"

# Derived class representing a Boat
class Boat(Vehicle):
    def move(self):
        return "Sailing 🚤"
# Derived class representing a Bicycle 
class Bicycle (Vehicle):
    def move(self):
        return "Cycling"

# Example objects
vehicles = [Car()Plane(), Boat() Bicycle(.)_]

# Iterate through each vehicle and call their move() method
for vehicle in vehicles:
    print(vehicle.move())
    
