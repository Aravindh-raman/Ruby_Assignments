## Q1: Write a program to print first n odd numbers where n can be from 1 to 100.
```ruby
for i in 1..100    
    if(i%2 != 0)
        puts i
    end
end
```
## Q2 Given an array of integers where elements can be from 1-7. every element maps to the day of the week. write a program to print it like 
1-monday, 2-tuesday, 3-wednesday 

arr = [1, 5 , 7, 4, 2, 6, 1, 4, 2, 7]; 

Output: 1-monday, 5-friday, 7-sunday ...0
```ruby
def map(arr)
  d = {
    1 => "monday",
    2 => "tuesday",
    3 => "wednesday",
    4 => "thursday",
    5 => "friday",
    6 => "saturday",
    7 => "sunday"
  }

  result = arr.map { |num| "#{num}-#{d[num]}" }
  puts result.join(', ')
end
arr = [1, 5, 7, 4, 2, 6, 1, 4, 2, 7]
map(arr)
```
Output:
```ruby
1-monday, 5-friday, 7-sunday, 4-thursday, 2-tuesday, 6-saturday, 1-monday, 4-thursday, 2-tuesday, 7-sunday
```
## Q3 Given an array of integers, sort the array using bubble, insertion or selection sort algorithm [any one] 
 arr = [12, 15, 9, 4, 30, 3, 7];
```ruby
def bubble_sort(arr)
    for i in 0...arr.length 
        for j in 0...(arr.length-i-1)
        if(arr[j]>arr[j+1])
            temp=arr[j]
            arr[j]=arr[j+1]
            arr[j+1]=temp
        end
        end
    end
    arr
end
arr = [12, 15, 9, 4, 30, 3, 7]
sorted_arr = bubble_sort(arr)
puts sorted_arr.join(", ")
```
Output:
```ruby
3, 4, 7, 9, 12, 15, 30
```