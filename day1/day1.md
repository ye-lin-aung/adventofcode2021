- [[Day 1] Sonar Sweep](#orge7becb2)
  - [Increment counter](#org657af84)
  - [Part One](#org177c276)
    - [Test data](#orgc3cea79)
    - [Input data](#org7998b42)
  - [Part Two](#org0537c1e)
    - [Test data](#orgbae1ff6)
    - [Input data](#orgc63da5b)


<a id="orge7becb2"></a>

# [Day 1] Sonar Sweep


<a id="org657af84"></a>

## Increment counter

```ruby
def increment_counter(array)
 count = 0
 array.each_cons(2) do |first, second|
   count += 1 if second > first
 end
 count
end
```


<a id="org177c276"></a>

## Part One


<a id="orgc3cea79"></a>

### Test data

```ruby
def increment_counter(array)
 count = 0
 array.each_cons(2) do |first, second|
   count += 1 if second > first
 end
 count
end
input = File.readlines("test.txt").map(&:to_i)      
"Result: #{increment_counter(input)}"
```

    Result: 7


<a id="org7998b42"></a>

### Input data

```ruby
def increment_counter(array)
 count = 0
 array.each_cons(2) do |first, second|
   count += 1 if second > first
 end
 count
end
input = File.readlines("input.txt").map(&:to_i)      
"Result: #{increment_counter(input)}"
```

    Result: 1226


<a id="org0537c1e"></a>

## Part Two


<a id="orgbae1ff6"></a>

### Test data

```ruby
def increment_counter(array)
 count = 0
 array.each_cons(2) do |first, second|
   count += 1 if second > first
 end
 count
end
sum_array = []
File.readlines("test.txt").map(&:to_i).each_cons(3) do |first_num, second_num, third_num|
   sum_array << first_num + second_num + third_num
end
"Result: #{increment_counter(sum_array)}"
```

    Result: 5


<a id="orgc63da5b"></a>

### Input data

```ruby
def increment_counter(array)
 count = 0
 array.each_cons(2) do |first, second|
   count += 1 if second > first
 end
 count
end
sum_array = []
File.readlines("input.txt").map(&:to_i).each_cons(3) do |first_num, second_num, third_num|
   sum_array << first_num + second_num + third_num
end     
"Result: #{increment_counter(sum_array)}"
```

    Result: 1252
