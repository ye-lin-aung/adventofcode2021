- [[Day 1] Sonar Sweep](#org127aa58)
  - [Increment counter](#org4a9597a)
  - [Part One](#org0dd2e3f)
    - [Test data](#org03145ed)
    - [Input data](#org838369a)
  - [Part Two](#org5e136d0)
    - [Test data](#org0173799)
    - [Input data](#org21310c1)


<a id="org127aa58"></a>

# [Day 1] Sonar Sweep


<a id="org4a9597a"></a>

## Increment counter


<a id="org0dd2e3f"></a>

## Part One


<a id="org03145ed"></a>

### Test data

```ruby
"Result: #{File.readlines('test.txt').map(&:to_i).each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum}"
```

    Result: 7


<a id="org838369a"></a>

### Input data

```ruby
"Result: #{File.readlines('input.txt').map(&:to_i).each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum}"
```

    Result: 1226


<a id="org5e136d0"></a>

## Part Two


<a id="org0173799"></a>

### Test data

```ruby
"Result: #{File.readlines('test.txt').map(&:to_i).each_cons(3).map do |first_num, second_num, third_num|
   first_num + second_num + third_num
end.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum}"
```

    Result: 5


<a id="org21310c1"></a>

### Input data

```ruby
"Result: #{File.readlines('input.txt').map(&:to_i).each_cons(3).map do |first_num, second_num, third_num|
   first_num + second_num + third_num
end.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum}"
```

    Result: 1252
