## 1. Create a Circle class and initialize it with radius. Make two methods getArea and getCircumference inside this class.
```ruby
class Circle
   def initialize(r)
     @r = r
   end
 
   def getArea()
     return Math::PI * @r * @r
   end
 
   def getCircumference()
     return 2 * Math::PI * @r
   end
 end
 
 c = Circle.new(5)
 puts c.getArea()
 puts c.getCircumference()
 ```

## 2. Take float number in a variable and convert into a string with up to 2 places in decimal with a dollar sign prefixed.Example: f=9.312482 to s=”$9.31”
```ruby
num = 9.312482
s = format("$%.2f", num)
puts s
```
## 3. Create a Temperature class. Make two methods : 
1. convertFahrenheit - It will take celsius and will print it into Fahrenheit. 
2. convertCelsius - It will take Fahrenheit and will convert it into Celsius. 

Write a code in ruby for the above questions.
```ruby
class Temperature
    def initialize()
    end
  def convertFahrenheit(x)
    return ((9.0/5.0)*x+32.0)
  end
  def convertCelsius(x)
    return (x-32.0)*(5.0/9.0)
  end
end

t=Temperature.new
puts t.convertCelsius(85)
puts t.convertFahrenheit(29.4444)
```