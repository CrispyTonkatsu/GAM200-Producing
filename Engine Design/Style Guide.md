### File Naming
Extensions: hpp, cpp
Naming:
- For classes, use camel case name for class.
- For functions, use snake_case.
### Documentation
We will be using doxygen, the comments should be in the header file for *all* public functions. Make sure to describe functions which do not make sense without context. Give the missing details and/or caveats.

>[!caution] Don't forget to add your copyright header
>Forgetting this might bring issues, make sure that there are some. Specially nvim users.
### Comments
You can add them as you see fit. So long they are not intrusive and don't break your documentation.
### Inside Code
- Methods: snake_case
- Field Names: snake_case
- Integers: i32, i64, etc.
- Floats: f32, f64, etc.
- When possible use either the STL or crab.

>[!Caution] Casting
>Do not use:
>C-style casts
>const casts
>static casts
>reinterpret casts
>*be wary of* dynamic casts