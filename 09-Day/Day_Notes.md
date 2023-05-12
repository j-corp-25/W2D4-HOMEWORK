


# Recursion

When a method calls itself

##### Example:
```ruby
# recursive method definition:
def say_hello
  p "hello"
  say_hello
end

say_hello # prints "hello" forever
```


### Recursive Countdown

In our previous example we saw how our recursive method crashed because it entered an infinite recursive loop. Of course useful recursive methods should not crash, so let's go through the process of building a working one.

Let's build a recursive `countDown` that starts ticking down numbers:

```ruby
def count_down(num)
  p num;
  count_down(num - 1)
end

count_down(10)  # this prints decreasing numbers starting at 10 forever
```

We can Use a stopper to make it stop at a certain point

```ruby
def count_down(num)
  if num == 0
    p "Houston, we have lift-off!"
    return;
  end

  p num
  count_down(num - 1)
end

count_down(10)  # prints numbers from 10 to 1, and finally "Houston, we have lift-off!"
```

Base Case Anatomy

### Anatomy of a Recursive Method

In recursive methods, we need to implement a way to stop the recursive loop and prevent it from looping forever. We took care of the infinite loop issue in our `countDown` by using an if statement that prevents another recursive call. In general, we call such a statement the **base case**

A recursive method consists of two fundamental parts:

-   the **base case** where we halt the recursion by not making a further call
-   the **recursive step** where we continue the recursion by making another subsequent call

```ruby
def count_down(num)
    # base case
    if num == 0
        p "Houston, we have lift-off!"
        return;
    end
    p num
    # recursive step
    count_down(num - 1)
end
```

### Solving a Problem Recursively:

Because every recursive problem must have a base and recursive case, we can follow these steps to help us write a recursive method:

1.  Identify the base case in the problem and code it. The base case should explicitly handle the scenario(s) where the arguments are so trivially "small", that we immediately know the result without further calculation. Be sure it works by testing it.
2.  Solve the next level of the problem, using the result of the base case. Test it.
3.  Modify the code in step 2, generalizing it for every level of the problem.
# In recursion we go back and forth between levels


# Using Git

**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

create new repository 
git add -A
git commit -m "  "
git push









