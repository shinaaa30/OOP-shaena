# Define the Dog class
class Dog:
    # Constructor to initialize the dog's name and age
    def __init__(self, name, age):
        self.name = name  # Instance variable for the dog's name
        self.age = age    # Instance variable for the dog's age

    # Method to make the dog bark
    def bark(self):
        return f"{self.name} says Woof!"

    # Method to get the dog's age in human years
    def get_human_age(self):
        return self.age * 7

# Define the ServiceDog class that inherits from Dog
class ServiceDog(Dog):
    # Constructor to initialize the service dog's name, age, and service type
    def __init__(self, name, age, service_type):
        super().__init__(name, age)  # Call the constructor of the parent class
        self.service_type = service_type  # Additional attribute for service type

    # Method to describe the service dog
    def describe_service(self):
        return f"{self.name} is a {self.service_type} service dog."

# Create an instance of the Dog class
my_dog = Dog("Buddy", 3)

# Create an instance of the ServiceDog class
my_service_dog = ServiceDog("Max", 4, "therapy")

# Call methods on the instances
print(my_dog.bark())  # Output: Buddy says Woof!
print(f"{my_dog.name} is {my_dog.get_human_age()} years old in human years.")  # Output: Buddy is 21 years old in human years.

print(my_service_dog.bark())  # Output: Max says Woof!
print(f"{my_service_dog.name} is {my_service_dog.get_human_age()} years old in human years.")  # Output: Max is 28 years old in human years.
print(my_service_dog.describe_service())  # Output: Max is a therapy service dog.
