- [[Day 1] Sonar Sweep](#org63d9607)
  - [Increment counter](#org9e1ab6a)
  - [Part One](#org5281b40)
    - [Test data](#orgf21e89c)
    - [Input data](#org45c0b29)
  - [Part Two](#orgb81f3d6)
    - [Test data](#org3b4159a)
    - [Input data](#org0905f30)


<a id="org63d9607"></a>

# [Day 1] Sonar Sweep


<a id="org9e1ab6a"></a>

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


<a id="org5281b40"></a>

## Part One


<a id="orgf21e89c"></a>

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


<a id="org45c0b29"></a>

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


<a id="orgb81f3d6"></a>

## Part Two


<a id="org3b4159a"></a>

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


<a id="org0905f30"></a>

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
