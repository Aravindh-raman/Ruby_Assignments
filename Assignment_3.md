## 1. Explain implicit blocks with an example.
In Ruby, an implicit block is a block of code that can be passed to a method without explicitly defining it using the do..end or curly braces {} syntax. Instead, the block is implicitly defined based on the method's context and is automatically executed within the method. This is a convenient feature in Ruby that allows for cleaner and more concise code.

To use an implicit block, a method must have the ability to accept a block of code as an argument. This is usually achieved by using the yield keyword within the method. The method can then call the block of code using yield at the appropriate time, executing the block's code within its own context.
```ruby
def print_message
  puts "This is the beginning of the method."

  # The block will be executed here
  yield if block_given?

  puts "This is the end of the method."
end

# Using print_message method with an implicit block
print_message do
  puts "This is the code within the implicit block."
end
```
Output:
```ruby
This is the beginning of the method.
This is the code within the implicit block.
This is the end of the method.
```
## 2. Write a code where a proc is passed as an argument to the method.
```ruby
def perform_operation(x, y, operation_proc)
  result = operation_proc.call(x, y)
  puts "The result of the operation is: #{result}"
end

addition_proc = Proc.new { |a, b| a + b }

perform_operation(5, 3, addition_proc)
```
Output:
```ruby
The result of the operation is: 8
```
## 3. Differentiate between blocks, procs, and lambdas.
1. Blocks:

- Blocks are anonymous chunks of code that are not objects in themselves.
- They are used in Ruby to pass code to methods for execution.
- Blocks are often created using do..end or curly braces {} syntax.
- Blocks have limited reusability since they can't be saved to variables or passed as standalone arguments to methods.
2. Procs:

- Procs are objects that can hold blocks of code as first-class entities in Ruby.
- They are created using Proc.new or the proc method.
- Procs provide more flexibility with argument handling, as they allow a mismatch between the number of arguments passed to them and the number of - parameters defined in the block. Extra arguments are ignored, and missing arguments are assigned nil.
- Procs can be saved to variables, stored in data structures, and passed as arguments to other methods.
3. Lambdas:

- Lambdas are similar to Procs; they are also objects that hold blocks of code.
- They are created using the lambda keyword or -> (stabby lambda) notation.
- Lambdas enforce strict argument handling, ensuring that the number of arguments passed matches the number of parameters defined in the lambda - block. If there is a mismatch, an ArgumentError is raised.
- Lambdas behave more like anonymous methods, as they have their own bindings and scoping rules.
## 4. WAP to check if a string is palindrome.
```ruby
def palindrome(s)
  for i in 0...(s.length/2)
        if s[i]!=s[s.length-1-i]
            puts "string is not a palindrome"
            return 
        end
    end
    puts "string is palindrome"
    return
end
puts palindrome("racecar")
puts palindrome("hello")
```
Output:
```ruby
string is palindrome

string is not a palindrome
```
## 5. WAP to print the sum of maximum and minimum element in an array 
```ruby
arr = [3, 7, 1, 9, 5]
sum = arr.min+arr.max
puts "Sum is #{sum}"
```
Output:
```ruby
Sum is 10
```