---
id: khxu5xqcxi2rcuanehl87vu
title: Design Pattern
desc: ''
updated: 1650511005176
created: 1648522082649
---

Design patterns are the well-known solutions to **recurring** problems.

```mermaid
flowchart LR
    id1(Systematic reuse of best design ideas) --> id2(lower cost and higher quality)
```

### Characteristics

- Language neutral
- Dynamic
- Incomplete by design to promote customization.

### Design pattern types

- Creation
  - Use
    - Create objects systematically
  - Benefits
    - Flexibility
- Structural
  - Use
    - Establish relationship between software components
    - Accomplish both functional and non-functional goals
  - Benefits
    - Based on the goals structures can be defined
- Behavioral
  - Use
    - How well the objects can interact with each other
    - Accomplish both function and non-function goals
  - Benefits
    - Defining protocols while these objects interacting each other to achieve the common goal

### OOP use case for design patterns

```mermaid
flowchart LR
    id1(Creational) --> id2(Polymorphism)
    id3(Structural) --> id4(Inheritance)
    id5(Behavioral) --> id6(Methods)
```

```mermaid
flowchart LR
    id8(Creational) --> id7(Interface)
    id9(Structural) --> id7(Interface)
    id10(Behavioral) --> id7(Interface)
```

### Inheritance

In object-oriented programming, inheritance is the mechanism of basing an object or class upon another object or class, retaining similar implementation. Also defined as deriving new classes from existing ones such as super class or base class and then forming them into a hierarchy of classes.

```mermaid
classDiagram
Pet <|-- Cat
Pet <|-- Dog
Pet: +String name
Pet: +int age
Pet: +speak()
class Cat{
  +speak()
}
class Dog{
  +speak()
}
```

In the above **Cat** and **Dog** can inherit the attributes of **Pet**, but it will override the attribute _speak()_ based on their requirement.

### Polymorphism

- Relies on inheritance
- Allows child classes to be instantiated and treated as the same type as their parent
- Enables a parent class to be manifested any of its child classes.

### How to describe design pattern context

- Participants
  - Class involved to form a design pattern
  - Roles of these classes
- Quality attributes
  - Nonfunctional requirement's such as
    - usability
    - modifiability
    - reliability
    - performance
  - Effect on the entire software, such as
    - architectural solutions
- Forces
  - Various factors or trade-offs to consider
    - manifested in quality attributes
    - unintended consequences
- Consequences
  - worse performance
  - Decision makers should consider consequences.

### Pattern Language

- Name
  - capture the gist
  - vocabulary
  - Meaningful and memorable
- Context
  - Scenario
  - Insights on when and where
- Problem
  - Design challenges the pattern trying to address
- Solution
  - Specifies the pattern
  - Structure → relationships (between the elements)
  - Behavior → interactions (between the elements)
- Related patterns
  - Lists other patterns used to describe
  - Used together to solve a problem
  - Similar but different

## Creation patterns

## Factory

**Factory encapsulate object creation** that is factory is an object that is specialized in creating other object.

### Factory problem situation

- Uncertain in type of objects
- Decision to be made in runtime regarding what classes to use.

### Factory Scenario

A pet shop originally selling dogs only, now they want to sell cats too, and they want to describe their attributes too.

### Factory method implementation

```python
class Dog:
  """A simple Dog class"""
  def __init__(self, name):
    slef._name = name

  def speak(self):
    return "Woof"
```

```python
class Cat:
  """A simple Cat class"""
  def __init__(self, name):
    slef._name = name

  def speak(self):
    return "Meow"
```

```python
# The below function not part of the Cat class
def get_pet(pet="dog"):
  """Factory method"""
  pets = dict(dog=Dog("Hope"), cat=Cat("Peace"))
  return pets[pet]
# now will try initiate and test above classes
d = get_pet("dog")
print(d.speak())
# Output: Woof
c = get_pet("cat")
print(c.speak())
# Output: Meow
```

## Abstract Factory

Abstract factory builds on factory pattern and it' useful when we are expecting the family of related objects at a given time but doesn't have to know which family it is until runtime.

### Abstract Factory problem situation

- The user expectations yields

### Abstract Factory scenario

A pet factory whose concrete factories include dog factory and cat factory. Both dog and cat factories produce dogs and cats, as well as related products, such as dog food and cat food.

### Abstract Factory Implementation

```mermaid
classDiagram
PetFactory <|-- CatFactory
PetFactory <|-- DogFactory
CatFactory <|-- Cat
CatFactory <|-- CatFood
DogFactory <|-- Dog
DogFactory <|-- DogFood

```

We implement our abstract factory without using inheritance because Python is a dynamically typed language, and therefore does not require abstract classes.

```python
class Dog:
  """One of the obhects to be returned"""
  def speak(slef):
    return "Woof!"

  def __str__(self):
    return "Dog"

class DogFactory:
  """Concrete factory"""
  def get_pet(self):
    """Returns a Dog object"""
    return Dog()
  def get_food(self):
    """Returns a Dog Food object"""
    return "Dog Food!"

class PetStore:
  """PetStore houses our Abstract Factory"""
  def __init__(self, pet_factory=None):
    """pet_factory is our Abstract Factory"""
    self._pet_factory = pet_factory # concrete factory

  def show_pet(self):
    """Utility method to display the details of the objects returned by the DogFactory"""
    pet = self._pet_factory.get_pet()
    pet_food = self._pet_factory.get_food()
    print("Our pet is '{}'!".format(pet))
    print("Our pet says hello by '{}'".format(pet.speak()))
    print("Its food is '{}'!".format(pet_food))

# Create a Concrete Factory
factory = DogFactory()

# Create a pet store housing our Abstract Factory
shop = PetStore(factory)

# Invoke the utility method to show the details of our pet
shop.show_pet()
```

## Singleton

When we have a class that is supposed to have only one instance, we can use the singleton pattern to ensure that.

### Singleton problem situation

- Global variant in an object-oriented way
- Borg
  - The Borg class implements the Borg design pattern which provides a singleton like pattern for Python. A Borg object can be accessed by calling the getInstance() function. This function returns an instance of the Borg class which stores its state between successive calls to get the Borg object.

### Singleton scenario

- An information cache shared by multiple objects

By keeping this information in a single object like Singleton or sharing it constantly in Borg objects, There is no need to retrieve the information from its original sources each time. All modules in Python act as Singletons. In our scenario, Borg acts as an information cache for networking acronyms, and their spelled out versions.

### Singleton implementation

```python
class Borg:
  """Borg class making class attributes global"""
  _shared_state = {} # Attribute dictionary

  def __init__(self):
    self.__dict__ = self._shared_state # Make it an attribute dictionary
  def __str__(self):
    return str(self._shared_state)
class Singleton(Borg): # Inherits from the Borg class
  """This class now shares all its attributes among its various instances"""
  def __init__(self, **kwargs):
    Borg.__init__(self)
    self._shared_state.update(kwargs) # Update the attribute dictionary by inserting a new key-value pair
  def __str__(self):
    return str(self._shared_state)

x = Singleton(HTTP="Hyper Text Transfer Protocol")
print(x)

y = Singleton(SNMP="Simple Network Management Protocol")
print(y)
```

## Builder

Builder is a solution to an antipattern called telescoping constructor. An antipattern is the opposite of the best programming practice and what we want to avoid.

### Builder problem situation

The telescoping constructor antipattern occurs when a software developer attempts to build a complex object using an excessive number of constructors. The builder pattern is trying to solve this problem.

### Builder problem scenario

Think of a scenario in which you're trying to build a car. This test requires various car parts to be first constructed individually and then assembled. The builder pattern brings order to this chaotic process to remove unnecessary complexity as much as possible.

### Builder implementation

 It partitions the process of building a complex object into four different roles:

- The first role is a director in charge of actually building a product.
- The second role provides all the necessary interfaces required in building an object. We call this one an abstract builder because there'll be a concrete builder inheriting from it.
- The concrete builder class inherits from the abstract builder class and actually implements the details of the interfaces of the abstract builder class for the specific type of product.
- The product role represents an object being built.

```python
class Director:
  """Director"""
  def __init__(self, builder):
    self._builder = builder

  def construct_car(self):
    self._builder.create_new_car()
    self._builder.add_model()
    self._builder.add_tires()
    self._builder.add_engine()

  def get_car(self):
    return self._builder.car

class Builder():
  """Abstract Builder"""
  def __init__(self):
    self.car = None

  def create_new_car(self):
    self.car = Car()

class SkyLarkBuilder(Builder):
  """Concrete Builder --> provides parts and tools to work on the parts"""
  def add_model(self):
    self.car.model = "Skylark"

  def add_tires(self):
    self.car.tires = "Regular tires"

  def add_engine(self):
    self.car.engine = "Turbo engine"

class Car():
  """Product"""
  def __init__(self):
    self.model = None
    self.tires = None
    self.engine = None

  def __str__(self):
    return '{} | {} | {}'.format(self.model, self.tires, self.engine)

builder = SkyLarkBuilder()
director = Director(builder)
director.construct_car()
car = director.get_car()
print(car)
```

## Prototype

Prototype clones objects according to a prototypical instance. Here the keyword is cloning. Note that we're talking about making a copy instead of building.

### Prototype problem situation

Prototype is useful when instantiating many identical objects individually, which could be expensive in terms of computing power. Cloning could be a good alternative because it makes a carbon copy in the memory space instead of building individual objects, respectively, from scratch the usual way.

### Prototype problem scenario

Let's assume that we are building a car. We can mass produce cars more easily and quickly If the cars have the same color and options. Similarly, in our Python programming scenario, you can clone the objects by making a copy of a prototype object instead of building them through constructors, as long as they're supposed to be identical without variations.

### Prototype implementation

Our solution consists of creating a prototypical instance first and then cloning it whenever you need the replica. **The pattern related to the prototype pattern is the abstract factory**.

```python
import copy

class Prototype:
  """Prototype"""
  def __init__(self):
    self._objects = {}

  def register_object(self, name, obj):
    """Register an object"""
    self._objects[name] = obj

  def unregister_object(self, name):
    """Unregister an object"""
    del self._objects[name]

  def clone(self, name, **attr):
    """Clone a registered object and update its attributes"""
    obj = copy.deepcopy(self._objects.get(name))
    obj.__dict__.update(attr)
    return obj

class Car:
  """Product"""
  def __init__(self):
    self.name = "Skylark"
    self.color = "Red"
    self.options = "Ex"

  def __str__(self):
    return '{} | {} | {}'.format(self.name, self.color, self.options)

c = Car()
prototype = Prototype()
prototype.register_object('skylark', c)
c1 = prototype.clone('skylark')
```

## Structural Patterns

## Decorator

The decorator design pattern is a structural pattern that allows users to add new features to existing objects without changing their structures.

Pattern makes implementing the decorator pattern very straightforward due to its built-in language feature.

### Decorator problem situation

 Our challenge here is to add additional features to an existing object dynamically without using subclasses.

### Decorator problem scenario

We start with a function displaying a hello world message. You want to make the message look fancier by decorating it with additional tasks, such as blink.

### Decorator implementation

Functions are objects in Python, and we can add additional features to these functions using the built-in decorator in Python.

Patterns such as adapter, composite and strategy are related to the decorator pattern.
