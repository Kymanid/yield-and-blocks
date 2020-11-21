<!-- Let's look at the following example:

def yielding
  puts "the program is executing the code inside the method"
  yield
  puts "now we are back in the method"
end 
To call this method with a block, we use the following syntax:

yielding { puts "the method has yielded to the block!" } 
or:

yielding do
  puts "the method has yielded to the block!"
end  -->



<!-- yielding with parameters
The yield keyword can take parameters. In other words, if you use yield and give it an argument, it will pass that argument to the block and that data will become available to the code in the block.

For example:

def yielding_with_arguments(num)
  puts "the program is executing the code inside the method"
  yield(num)
  puts "now we are back in the method"
end 
We can call #yielding_with_arguments by providing both an argument and a block containing a placeholder, |i| in the following example, which will accept the argument passed to yield:

yielding_with_arguments(2) {|i| puts i * 2} 
We call our method with an argument:

yielding_with_arguments(2) 
and a block:

{ |i| puts i * 2 } 
The |i| (placeholder variable in between pipes) is our placeholder for the yielded value. The puts i * 2 is the code we actually want to enact with our yielded value.

So, the above method call will output:

the program is executing the code inside the method
4
now we are back in the method 

The syntax inside the block might look familiar — it is how we pass items from a collection into a block, one by one, when we use an iterator like #each.


 -->
