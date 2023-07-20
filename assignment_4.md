## Q1> Given an array [1,2,3,2,5,6,9,6,5,3,2,2,1,8,10,10,7]. Create a hash and store the frequency of the array element. 
```ruby
arr = [1, 2, 3, 2, 5, 6, 9, 6, 5, 3, 2, 2, 1, 8, 10, 10, 7]
hash = Hash.new(0)

arr.each do |i|
 hash[i] += 1
end

puts hash
```
Output:
```ruby
{1=>2, 2=>4, 3=>2, 5=>2, 6=>2, 9=>1, 8=>1, 10=>2, 7=>1}
```
## Q2> Write a program to print sum of numbers from 100 to 200
```ruby
sum=0
for i in 100..200
    sum+=i
end    
puts sum
```
Output:
```ruby
15150
```
## Q3> Write an exception for dividing by zero in Ruby.
```ruby
def divide(x, y)
  result = nil
  begin
    result = x / y
  rescue ZeroDivisionError => e
    puts "Error: #{e.message}"
  end
  result
end

puts divide(10, 2) 
puts divide(5, 0)   
```
Output:
```ruby
5
Error: divided by 0
```
## Q4 > Write a program to find and replace all occurrences of a character in a string. 
```ruby
def replace(str, target_char, replacement_char)
  result = str.gsub(target_char, replacement_char)
  result
end

str = "Hello"
target = "l"
replace = "X"
modified_str = replace(str, target, replace)
puts "Modified string: #{modified_str}"
```
Output:
```ruby
Modified string: HeXXo
```
