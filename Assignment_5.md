## 1. Write ruby regex to accept basic email addresses, that contain a letter (any case) as its 1st character, followed by any number of word characters, then an ‘@’ symbol, again followed by any number of word characters, then a ‘.’ and finally a maximum of 4 letter (minimum 1).
```ruby
def validate(email)
    pattern = /^[A-Za-z]\w*(@)(\w+\.)[a-zA-Z]{1,4}$/
    return email.match?(pattern)
end

puts validate("invalid@email")
puts validate("valid@email.com")
```
Output:
```ruby
false
true
```
## 2. Let’s consider a ruby class Vehicle with following definition: 
```ruby
class Vehicle 
  def initialize 
     puts “I am a vehicle” 
   end 
 
   def max_speed 
     puts “10” 
   end 
 end
```
### a. Define 2 classes Car and Rickshaw which inherit the class Vehicle. 
### b. Override method max_speed in both classes to output 100 and 25 for classes Car and Rickshaw respectively.
```ruby
class Vehicle
  def initialize
    puts "vehicle"
  end

  def max_speed
    puts "10"
  end
end

class Car < Vehicle
  def max_speed
    puts "100"
  end
end

class Rickshaw < Vehicle
  def max_speed
    puts "25"
  end
end

car = Car.new
car.max_speed

rickshaw = Rickshaw.new
rickshaw.max_speed
```
Output:
```ruby
vehicle
100
vehicle
25
```
## 3. Differentiate between Module and Mixins 
1. Module:

- A module in Ruby is a container for grouping related methods, constants, and class variables together.
- Modules cannot be instantiated or used to create objects on their own. Instead, they are used primarily for code organization and namespacing.
- Modules can be included in classes using the include keyword, allowing the class to access the methods defined in the module.
- They are also used to define namespaced constants and provide utility methods, acting like namespaces and mixins.
- Modules are helpful for achieving multiple inheritance-like behavior in Ruby classes, as a class can include multiple modules.
- Modules cannot have instances or be instantiated directly.
2. Mixin:

- A mixin is a concept closely related to modules, and it allows the sharing of methods among different classes.
- A mixin is achieved by including a module in one or more classes, thereby extending those classes with the methods defined in the module.
- By including a module in a class, the class gains the functionality of the module, effectively "mixing in" the methods.
- Mixins promote the concept of "composition over inheritance," enabling code reuse and providing flexibility in extending class functionality.
- A class can include multiple mixins, allowing it to inherit methods from multiple modules, offering more flexibility than single inheritance.
## 4. Differentiate between Private and Protected methods
1. Private Methods:
- Private methods in Ruby can only be called from within the same instance of the class in which they are defined. They cannot be called with an explicit receiver, even from within other instances of the same class.
- Private methods are often used for internal implementation details that are not meant to be accessed directly by external code.
- They are typically used to encapsulate helper methods and to ensure that certain operations are only accessible within the class itself.
- You define a private method by using the private keyword before the method definition.
2. Protected Methods:
- Protected methods in Ruby can be called from within the same instance of the class, just like private methods. However, they can also be called with an explicit receiver of another instance of the same class.
- Protected methods are often used when you want to provide access to certain methods for related objects of the same class.
- They are used to share behavior between instances of the same class while maintaining encapsulation.
- You define a protected method by using the protected keyword before the method definition.