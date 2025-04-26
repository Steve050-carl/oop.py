# oop.py
// Assignment 1
# Parent Class
class Superhero:
    def __init__(self, name, power, level):
        self.name = name
        self.power = power
        self.__level = level  # Private attribute (encapsulation)

    def show_details(self):
        print(f"Name: {self.name}, Power: {self.power}, Level: {self.__level}")

    def attack(self):
        print(f"{self.name} attacks with {self.power}!")

    def get_level(self):  # Getter for the private attribute
        return self.__level

# Child Class inheriting from Superhero
class FlyingHero(Superhero):
    def __init__(self, name, power, level, flight_speed):
        super().__init__(name, power, level)
        self.flight_speed = flight_speed

    def fly(self):
        print(f"{self.name} flies at {self.flight_speed} km/h!")

# Creating objects
hero1 = Superhero("Captain Code", "Debug Blast", 5)
hero2 = FlyingHero("Sky Rider", "Wind Slash", 8, 300)

# Using methods
hero1.show_details()
hero1.attack()

hero2.show_details()
hero2.attack()
hero2.fly()
print("Level:", hero2.get_level())  # Accessing private attribute through getter


//Activity 2
class Car:
    def move(self):
        print("Driving 🚗")

class Plane:
    def move(self):
        print("Flying ✈️")

class Boat:
    def move(self):
        print("Sailing 🚤")

# Function to demonstrate polymorphism
def travel(vehicle):
    vehicle.move()

# Create objects
car = Car()
plane = Plane()
boat = Boat()

# Test polymorphism
travel(car)
travel(plane)
travel(boat)

