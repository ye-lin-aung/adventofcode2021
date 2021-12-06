- [[Day 1] Sonar Sweep](#orgae0d909)
  - [Increment counter](#org03b00ac)
  - [Part One](#orgc9d5ab5)
    - [Test data](#org9eda41e)
    - [Input data](#org507c950)
  - [Part Two](#org74decad)
    - [Test data](#orga61b497)
    - [Input data](#org6076558)


<a id="orgae0d909"></a>

# [Day 1] Sonar Sweep


<a id="org03b00ac"></a>

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


<a id="orgc9d5ab5"></a>

## Part One


<a id="org9eda41e"></a>

### Test data

```ruby
input = File.readlines("test.txt").map(&:to_i)
def increment_counter(array)
 count = 0
 array.each_cons(2) do |first, second|
   count += 1 if second > first
 end
 count
end
"Result: #{increment_counter(input)}"
```

    Result: 7


<a id="org507c950"></a>

### Input data

```ruby
input = File.readlines("input.txt").map(&:to_i)
def increment_counter(array)
 count = 0
 array.each_cons(2) do |first, second|
   count += 1 if second > first
 end
 count
end
"Result: #{increment_counter(input)}"
```

    Result: 1226


<a id="org74decad"></a>

## Part Two


<a id="orga61b497"></a>

### Test data

```ruby
sum_array = []
File.readlines("test.txt").map(&:to_i).each_cons(3) do |first_num, second_num, third_num|
   sum_array << first_num + second_num + third_num
end
 def increment_counter(array)
  count = 0
  array.each_cons(2) do |first, second|
    count += 1 if second > first
  end
  count
 end
"Result: #{increment_counter(sum_array)}"
```

    Result: 5


<a id="org6076558"></a>

### Input data

```ruby
sum_array = []
File.readlines("input.txt").map(&:to_i).each_cons(3) do |first_num, second_num, third_num|
   sum_array << first_num + second_num + third_num
end
 def increment_counter(array)
  count = 0
  array.each_cons(2) do |first, second|
    count += 1 if second > first
  end
  count
 end
"Result: #{increment_counter(sum_array)}"
```

    Result: 1252
