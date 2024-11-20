# Assignment 1
# Define the Book class
class Book:
    def __init__(self, title, author, genre, price):
        self.title = title      # Title of the book
        self.author = author    # Author of the book
        self.genre = genre      # Genre of the book
        self.price = price      # Price of the book

    # Method to display book details
    def display_info(self):
        return f"Title: {self.title}, Author: {self.author}, Genre: {self.genre}, Price: ${self.price}"

    # Method to apply a discount on the book price
    def apply_discount(self, discount_percent):
        self.price -= self.price * (discount_percent / 100)

# Creating an object of the Book class
book1 = Book("The Great Gatsby", "F. Scott Fitzgerald", "Fiction", 20)

# Display book info
print(book1.display_info())

# Apply a discount and display the new price
book1.apply_discount(10)  # Applying 10% discount
print("Discounted price:", book1.price)


**#Assignment 2**
# Base class Vehicle
class Vehicle:
    def move(self):
        pass  # This is just a placeholder method to be overridden

# Car subclass
class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

# Plane subclass
class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

# Test polymorphism
def test_movement(vehicle):
    vehicle.move()

# Creating objects
car = Car()
plane = Plane()

# Test the move method of both vehicles
test_movement(car)  # Output: Driving 🚗
test_movement(plane)  # Output: Flying ✈️

