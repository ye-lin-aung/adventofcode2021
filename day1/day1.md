- [[Day 1] Sonar Sweep](#orgeceae4d)
  - [Part One](#org31ad38f)
    - [Test data](#orgacb4055)
    - [Input data](#org74c87ea)
  - [Part Two](#org6c89597)
    - [Test data](#orgc42eb76)
    - [Input data](#orgbe706f5)


<a id="orgeceae4d"></a>

# [Day 1] Sonar Sweep


<a id="org31ad38f"></a>

## Part One


<a id="orgacb4055"></a>

### Test data

```ruby
"Result: #{File.readlines('test.txt').map(&:to_i).each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum}"
```

    Result: 7


<a id="org74c87ea"></a>

### Input data

```ruby
"Result: #{File.readlines('input.txt').map(&:to_i).each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum}"
```

    Result: 1226


<a id="org6c89597"></a>

## Part Two


<a id="orgc42eb76"></a>

### Test data

```ruby
"Result: #{File.readlines('test.txt').map(&:to_i).each_cons(3).map do |first_num, second_num, third_num|
   first_num + second_num + third_num
end.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum}"
```

    Result: 5


<a id="orgbe706f5"></a>

### Input data

```ruby
"Result: #{File.readlines('input.txt').map(&:to_i).each_cons(3).map do |first_num, second_num, third_num|
   first_num + second_num + third_num
end.each_cons(2).select{ |first, second| second > first }.map{ 1 }.sum}"
```

    Result: 1252
