# Ruby Bug: Unexpected Instance Variable Modification

This repository demonstrates a common Ruby bug related to directly modifying instance variables using `instance_variable_set`. Directly manipulating instance variables outside of defined methods can lead to unexpected behavior and make debugging difficult.  This practice is generally discouraged.

**Problem:** Directly changing instance variables using `instance_variable_set` bypasses potential validation, encapsulation, and side effects handled within the class's methods.  This can lead to inconsistencies and errors that are hard to trace.

**Solution:**  Always use accessor methods (getters and setters) to interact with instance variables. This ensures controlled access and allows you to implement logic within these methods to handle validation, calculations, and side effects correctly.   Using `attr_accessor`, `attr_reader`, and `attr_writer` provides a clean and maintainable way to access and modify instance variables.