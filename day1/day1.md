
# Table of Contents

1.  [[Day 1] Sonar Sweep](#orgb237437)
    1.  [Increment counter](#org2fe7679)
    2.  [Part One](#org7f7955e)
        1.  [Test data](#org6949e99)
        2.  [Input data](#org74ad41d)
    3.  [Part Two](#org5d2dca1)
        1.  [Test data](#orgea06c8e)
        2.  [Input data](#orgac51052)


<a id="orgb237437"></a>

# [Day 1] Sonar Sweep


<a id="org2fe7679"></a>

## Increment counter

    def increment_counter(array)
     count = 0
     array.each_cons(2) do |first, second|
       count += 1 if second > first
     end
     count
    end


<a id="org7f7955e"></a>

## Part One


<a id="org6949e99"></a>

### Test data

    input = File.readlines("test.txt").map(&:to_i)
    def increment_counter(array)
     count = 0
     array.each_cons(2) do |first, second|
       count += 1 if second > first
     end
     count
    end
    "Result: #{increment_counter(input)}"

    Result: 7


<a id="org74ad41d"></a>

### Input data

    input = File.readlines("input.txt").map(&:to_i)
    def increment_counter(array)
     count = 0
     array.each_cons(2) do |first, second|
       count += 1 if second > first
     end
     count
    end
    "Result: #{increment_counter(input)}"

    Result: 1226


<a id="org5d2dca1"></a>

## Part Two


<a id="orgea06c8e"></a>

### Test data

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

    Result: 5


<a id="orgac51052"></a>

### Input data

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

    Result: 1252

