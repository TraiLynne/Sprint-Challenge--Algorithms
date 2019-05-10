Add your answers to the Algorithms exercises here.

## Exercise I

a) Constant time `O(c)`- the only value that changes is `a`. Assuming `n` is equal to or greater than 1, multiplying `n` by itself and adding it to `a` will always be a value greater than `n`, the loop will stop after the first go.

b) My guess is Linear `O(n)` or Logarithmic Time `O(log n)` - the number of operations this would take is in direct proportion to `n` because the loop will end when `i` gets to `n`. `n` will stay a constant value, therefore the loop will end. But since there are multiple for loops in there, the number of operations will grow slowly the larger the value of `n`. I will come back to this one ...

c) Linear Time `O(n)` - the number of operations is in direct proportion to n. If I am reading this right, this is basically a countdown from `n` to 0.

## Exercise II
It sounds like I would do a binary search with a `O(log n)` runtime complexity.

1. Set `low = 0`, `high = n`, `m = n/2`
2. throw the egg from floor `m`, unless `high == m`
      
      a) if safe ? 
         
         1a. set `low = m`
         
         2a. set `range = [low ... high]`
         
         3a. set `m = range[length of range/2]`
         
         4a. repeat step 2
      
      b) if yolk ?
         
         1b. set `high = m`
         
         2b. set `range = [low ... high]`
         
         3b. set `m = range[length of range/2]`
         
         4b. repeat step 2

But at the same time ...If i start at the bottom floor and just keep moving up until the egg breaks, I will only lose one egg. That is if, everything is works as it should. So I guess it depends on if I want to not drop as many eggs in general or if I don't want a lot of broken eggs. I think that is Linear Time. 

1. Start at `current = 1`
2. Throw egg
   1. if safe ?
      1. `safe = current`
      2. `current = current + 1`
   2. if yolk ?
      1. `safe = current - 1`
      2. `unsafe = current`
      3. Done