- [[Day 2] Dive](#org1fb821e)
  - [Part one](#org02baa0e)
    - [Test data](#org587cbd6)
    - [Input data](#org0de56e2)
  - [Part two](#org9f969eb)
    - [Test data](#org8a4b68a)
    - [Input data](#orgd5c64d4)


<a id="org1fb821e"></a>

# [Day 2] Dive


<a id="org02baa0e"></a>

## Part one


<a id="org587cbd6"></a>

### Test data

```ruby
File.readlines("test.txt").group_by{ |x| (x.include?("up") || x.include?("down")) }.values.map{ |x| x.map{ |x|
                                                                            if x.include?("up")
                                                                              -(x[/\d+/].to_i)
                                                                            else
                                                                              x[/\d+/].to_i
                                                                            end
                                                                           }.sum }.inject(:*)
```

    150


<a id="org0de56e2"></a>

### Input data

```ruby
File.readlines("input.txt").group_by{ |x| (x.include?("up") || x.include?("down")) }.values.map{ |x| x.map{ |x|
                                                                          if x.include?("up")
                                                                            -(x[/\d+/].to_i)
                                                                          else
                                                                            x[/\d+/].to_i
                                                                          end
                                                                         }.sum }.inject(:*)
```

    2036120


<a id="org9f969eb"></a>

## Part two


<a id="org8a4b68a"></a>

### Test data

```ruby
File.readlines("test.txt").map do |x|
  if x.include? "forward"
    $horizontal = ($horizontal || 0) + x[/\d+/].to_i
    $depth ||= 0 
    $depth += ($aim || 0) * x[/\d+/].to_i
  elsif x.include? "down"
    $aim = ($aim || 0) + x[/\d+/].to_i
  else
    $aim = ($aim || 0) - x[/\d+/].to_i
  end
end.inject { |x| $horizontal * $depth }
```

    900


<a id="orgd5c64d4"></a>

### Input data

```ruby
File.readlines("input.txt").map do |x|
  if x.include? "forward"
    $horizontal = ($horizontal || 0) + x[/\d+/].to_i
    $depth ||= 0 
    $depth += ($aim || 0) * x[/\d+/].to_i
  elsif x.include? "down"
    $aim = ($aim || 0) + x[/\d+/].to_i
  else
    $aim = ($aim || 0) - x[/\d+/].to_i
  end
end.inject { |x| $horizontal * $depth }
```

    2015547716
