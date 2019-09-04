## Exercise: Linear Search (25 Points)

The purpose of this assignment is for your to become familiar with C++ and the basic search algorithm for an unsorted array.

The first thing you will need to do is fork and clone this assignment
from GitHub. Follow the instructions 
[here](https://github.com/vcc-csv15-fall2018/Course-Information/wiki)
to get started. 

Be sure that you fork the project first and use the URL from
the forked project when you clone it in CLion.

### Problem Description

The problem for this assignment is fairly simple: implement a linear search function for an
array of objects of any time (a templated function). The function takes a value to find, an array, 
the size of the array and returns the index of the element found, if its in the array,
otherwise it returns -1.

The functions declaration should look like the following: 

```cpp
#include <cstdint>

namespace edu { namespace vcccd { namespace vc { namespace csv15 {

template <class T>
int64_t find(const T& value, T array[], size_t size) {
	// put your code here
}

}}}}
```

The declaration should be in a file named `linearsearch.h` and the implementation can be
in any file with the extension `.cc`.

### Writing the code for this Project

Writing the code for this project is very simple. Since the 
objective of this assignment is understanding the workflow, 
the code is given to you. Simply create the one file below 
`main.cc` in CLion
and then copy the content into the files. 

#### Header file

In CLion in the project explorer, right-click the `include` directory
and chose `New => C++ Header File`. 

![Adding source file](https://github.com/sbcc-cs140-fall2018/Course-Information/wiki/images/03_new_source_file.png)

Under **Name** fill in
linearsearch. CLion will add the extension, but by default 
adds the `.h` extension. You should now see the file `linearsearch.h` in
the project explorer in the `include` directory.

Properly set up the namespaces and declare the function described above in this file.

#### Implementation file

In CLion in the project explorer, right-click the `src` directory
and chose `New => C++ Source File`. 

![Adding source file](https://github.com/sbcc-cs140-fall2018/Course-Information/wiki/images/03_new_source_file.png)

Under **Name** fill in
linearsearch, or whatever name you want to give it. CLion will add the extension, but by default 
adds the `.cpp` extension. All projects in this class will
use the `.cc` extension. Select `.cc` in the **Type** drop-down
and press **OK**. You should now see the file `linearsearch.cc`, or whatever you called it, in
the project explorer in the `src` directory.

Properly set up the namespaces and implement the function described above in this file.

### Running the code for this project

Running this code should be straightforward. In the drop-down 
menu in the upper right-hand corner you should see a *Run
Configuration* called `Helloworld | Debug`. Make sure this 
configuration is selected and press the play button next to it.
In the **Run** view below the code you should see the output 
of running the program. It should look something like this:

```bash
/Users/username/githubusername/ex01-linearsearch/cmake-build-debug/bin/LinearSearch
Found value at index 3.

Process finished with exit code 0
```
Success! Now you can move on to testing your code. Remember that your output might be
different, but should look similar to this

### Testing the code for this project

Testing the code for this project is similar to running your code
as outlined above. In the drop-down menu in the upper right-hand
corner select the configuration `LinearSearch_Gtest` and press the 
play button next to it. In the **Run** view below the code you should
see the output of running these tests. It should look something
like this:

```bash
Running main() from gtest_main.cc
[==========] Running 3 tests from 1 test case.
[----------] Global test environment set-up.
[----------] 3 tests from LinearSearchTest
[ RUN      ] LinearSearchTest.FindInt10
[       OK ] LinearSearchTest.FindInt10 (0 ms)
[ RUN      ] LinearSearchTest.DontFindInt11
[       OK ] LinearSearchTest.DontFindInt11 (0 ms)
[ RUN      ] LinearSearchTest.PassNullString
[       OK ] LinearSearchTest.PassNullString (0 ms)

Your unit test score is 20 out of 20
The assignment is worth a total of 25 where the remainder of 5 points
comes from grading related to documentation, algorithms, and other
criteria.

[----------] 3 tests from LinearSearchTest (0 ms total)

[----------] Global test environment tear-down
[==========] 3 tests from 1 test case ran. (0 ms total)
[  PASSED  ] 3 tests.

Process finished with exit code 0
```

Remember, red good, green bad. If your tests pass you should see green
text and your code ran fine. You should also see your score for this
assignment minus code styling points which I will add later.

### Submitting the code for this project

At the bottom of CLion there should be a view tab labeled **Version Control**.
Select this tab at the bottom of the screen. You should see a tab called **Local Changes**.
Under **Unversion Files** you should have one file: `main.cc`.
Select these files and right-click on them. In the drop-down menu
select **Add to VCS**. Next, right-click on these files again, which should
now be under **Default** and select **Commit**. Add the appropriate
commit message and click **OK**. Finally, right click on the committed files,
select `Git -> Repository -> Push...`. Follow the onscreen directions
and press **OK**. This step will run the tests again, check that everything is OK
and then submit them to the cloud to have the tests run for grading.

If you do not understand these directions, or wish to do them on the command
line rather than in CLion, then read these [directions](https://github.com/vcc-csv15-fall2018/Course-Information/wiki/How-to-Turn-In-Every-Project).

