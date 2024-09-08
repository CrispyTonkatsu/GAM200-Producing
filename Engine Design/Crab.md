The main differences for crab are Box, Rc and Option.
## Box\<T>
This is a variation of unique pointers. The main difference is the mutability of the memory it points to:
```C++
const auto uni = std::make_unique<int>(5);
const auto box = crab::make_box<int>(5);

*uni = 10; // Will modify variable
box = 10; // Will NOT modify variable
```
## Rc
This is the way the program will count references. There are 2 versions of Rc:
- Rc, which is const
- RcMut, which is mutable
## Option
This is an extension of std::optional. The main difference is that it requires checking to access the value.
```C++
std::optional<int> standard = 5;
Option<int> crab = 5;

int temp = *standard; // will compile
temp = *crab; // will NOT compile
```
## Result
This is the way a function can return a value or a failure to return a value.