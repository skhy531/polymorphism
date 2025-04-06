# Base class
class Superhero:
    def __init__(self, name, power, city):
        self.name = name
        self.power = power
        self.city = city

    def introduce(self):
        print(f"I am {self.name}, protecting {self.city} with the power of {self.power}!")

    def use_power(self):
        print(f"{self.name} uses {self.power}!")

# Inherited class
class FlyingHero(Superhero):
    def __init__(self, name, power, city, wingspan):
        super().__init__(name, power, city)
        self.wingspan = wingspan

    def use_power(self):
        print(f"{self.name} soars through the skies with a wingspan of {self.wingspan} meters!")

# Another inherited class
class SpeedHero(Superhero):
    def __init__(self, name, power, city, speed):
        super().__init__(name, power, city)
        self.speed = speed

    def use_power(self):
        print(f"{self.name} runs at {self.speed} km/h to save {self.city}!")

# Creating objects
hero1 = FlyingHero("SkyQueen", "Flight", "Nairobi", 15)
hero2 = SpeedHero("Flashbeat", "Super Speed", "Mombasa", 300)

hero1.introduce()
hero1.use_power()

hero2.introduce()
hero2.use_power()
class Vehicle:
    def move(self):
        print("This vehicle moves...")

class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

class Boat(Vehicle):
    def move(self):
        print("Sailing 🚢")

# Create a list of different vehicles
vehicles = [Car(), Plane(), Boat()]

# Demonstrate polymorphism
for v in vehicles:
    v.move()
