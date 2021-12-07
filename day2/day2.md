- [[Day 2] Dive](#org8a4d5ac)
  - [Part One](#orge739151)
    - [Test data](#org1c47510)
    - [Input data](#orgf485cca)


<a id="org8a4d5ac"></a>

# [Day 2] Dive


<a id="orge739151"></a>

## Part One


<a id="org1c47510"></a>

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


<a id="orgf485cca"></a>

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
