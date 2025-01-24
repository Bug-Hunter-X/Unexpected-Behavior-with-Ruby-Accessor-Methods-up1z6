# Ruby Accessor Method Bug
This repository demonstrates a common yet subtle bug in Ruby related to the use of accessor methods without explicitly defining a setter method.  Attempting to assign a value directly to a getter method (e.g., `my_object.value = 30`) will not change the object's internal state unless a corresponding `value=` setter method is defined.

## The Bug
The `bug.rb` file shows how assigning a value directly to a getter method fails to modify the instance variable. Instead, it simply returns the current value of the instance variable without any change.

## The Solution
The `bugSolution.rb` file shows how to correct this by explicitly adding a setter method (`value=`). This allows direct modification of the instance variable using the accessor method.  Using the setter method provides a more explicit and maintainable way to manage the object's internal state.