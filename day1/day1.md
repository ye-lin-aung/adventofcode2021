- [[Day 1] Sonar Sweep](#org076d6bc)
  - [Increment counter](#org7a1fd5e)
  - [Part One](#orgd98890a)
    - [Test data](#orgff3eefc)
    - [Input data](#org5e6c15b)
  - [Part Two](#org3ccea15)
    - [Test data](#orgb216533)
    - [Input data](#org79f2232)


<a id="org076d6bc"></a>

# [Day 1] Sonar Sweep


<a id="org7a1fd5e"></a>

## Increment counter

```ruby
def increment_counter(array)
 array.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum
end
```


<a id="orgd98890a"></a>

## Part One


<a id="orgff3eefc"></a>

### Test data

```ruby
def increment_counter(array)
 array.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum
end
input = File.readlines("test.txt").map(&:to_i)      
"Result: #{increment_counter(input)}"
```

    Result: 7


<a id="org5e6c15b"></a>

### Input data

```ruby
def increment_counter(array)
 array.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum
end
input = File.readlines("input.txt").map(&:to_i)      
"Result: #{increment_counter(input)}"
```

    Result: 1226


<a id="org3ccea15"></a>

## Part Two


<a id="orgb216533"></a>

### Test data

```ruby
def increment_counter(array)
 array.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum
end
sum_array = []
File.readlines("test.txt").map(&:to_i).each_cons(3) do |first_num, second_num, third_num|
   sum_array << first_num + second_num + third_num
end
"Result: #{increment_counter(sum_array)}"
```

    Result: 5


<a id="org79f2232"></a>

### Input data

```ruby
def increment_counter(array)
 array.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum
end
sum_array = []
File.readlines("input.txt").map(&:to_i).each_cons(3) do |first_num, second_num, third_num|
   sum_array << first_num + second_num + third_num
end     
"Result: #{increment_counter(sum_array)}"
```

    Result: 1252
