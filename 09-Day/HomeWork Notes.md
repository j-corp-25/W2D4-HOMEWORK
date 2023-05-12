Think of recursion as a method calling a helper method but its actually calling itself.

once n = 10 in the recursion process it stops

*Your input + base case have to work together*

![[Pasted image 20230511003715.png]]

```ruby
def factorial(n)
	return 1 if n == 1
	n * factorial(n - 1)
end

p factorial(250)
```