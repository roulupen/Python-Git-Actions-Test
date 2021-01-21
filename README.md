# Python-Git-Actions-Test

Session 2 assignment of EPAi2.0

## Code Description(session2.py)

### Classes

- #### Something

  - __init__ : No arugument constructor of the class and it sets the member variable "something_new" as None.
  - __repr__ : This method overrides the default method and generates string representation of the object.

- #### SomethingNew

  - __init__ : This is a two argument constructor of the class. The first argument is an int type and this values assigned to a member variable i, the second argument is of type "Something" and this value assigned to a member variable something.
  - __repr__ : This method overrides the default method and generates string representation of the object.

### Methods

- #### add_something(collection: List[Something], i: int)

  - This function takes list of Something types as first argument and an int type as second argument. Then creates a new Object of Something and SomethingNew and creates a circular reference between the two objects and finally adds the something object into the collection list

- #### reserved_function()

  - This is a dummy function without any acutal instructions to perform.

- #### clear_memory(collection: List[Something])

  - This function takes List of Something types as an argument then iterate over all the elements in that list and remove circular dependency between Something and SomethingNew object then clears the list.

- #### critical_function()

  - This function doesn't take any input argument. It crates list of Something object of size 1024 * 128 by calling the function add_something and then calls clear_memory function to clear the created list.

- #### compare_strings_old(n)

  - This function takes an argument n. It generates to very long string a and b then it compares the string a and b "n" times.
  Then it creates list of characters char_list from string a using the list method then it checks whether charcter 'd' present in that list for n times.

- #### compare_strings_new(n)

  - Initially, this method takes an argument n and uses the sleep method from time module to sleep for 6 secs. But, I have modified this method to optimally compare two strings creating string interns and instead of comparing two strings by == operator now I'm checking the string using is operator.
  Second, enhancement is instead of creating a list and checking if character 'd' present or not I'm creating a set and checking if character 'd' present in that set or not. Finding an element in set is much more faster than finding in a list.

## Unit Test Case Descriptions

- ### test_clear_memory

  - This method verifies if circular dependcies handled properly inside "clear_memory" function or not. Unless circular dependices are not handled this will not pass.

- ### test_memory_actually_increased

  - This method verifies if peak memory usage is increasing by the critical_function method call.

- ### test_performance

  - Compares the time taken by compare_strings_old and compare_strings_new method, and verifies if performance of compare_strings_new method is 10 times faster than compare_strings_old method.

- ### test_readme_exists

  - Verfies if "README.md" file exists or not.

- ### test_readme_contents

  - Verifies if the "README.md" file contains at least 500 words or not.

- ### test_readme_proper_description

  - Verifies if the "README.md" files contains proper description about the code and unit test cases by comparing if certains key words present in the file or not.

- ### test_readme_file_for_formatting

  - Verifies if the "README.md" file has at least 10 '#' characters, to verifies if proper heading are present in the file while describing different sections.

- ### test_class_repr

  - Verifes if the class Something and SomethingNew has overrided __repr__ method or not. If override method not present then this test case will not pass.

- ### test_indentations

  - Verfies if Session2.py file is poperly indented(4 spaces) or not.

- ### test_function_name_had_cap_letter

  - Verfies if any function inside session2 file has capital letter in function name. If it has any capital letter then it fails the test case.

