- [[Day 2] Dive](#orgd523017)
  - [Part one](#orga82346c)
    - [Test data](#org7827168)
    - [Input data](#org5dd1dea)
  - [Part two](#org6e77fd3)
    - [Test data](#org8b5dbea)
    - [Input data](#orge3a4fd7)


<a id="orgd523017"></a>

# [Day 2] Dive


<a id="orga82346c"></a>

## Part one


<a id="org7827168"></a>

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


<a id="org5dd1dea"></a>

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


<a id="org6e77fd3"></a>

## Part two


<a id="org8b5dbea"></a>

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
end.map { |x| $horizontal * $depth }.first
```

    900


<a id="orge3a4fd7"></a>

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
end.map { |x| $horizontal * $depth }.first
```

    2015547716
