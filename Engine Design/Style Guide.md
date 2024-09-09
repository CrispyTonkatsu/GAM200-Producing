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

#### Namespaces
[[snake_case]], but should be kept relatively short and sparse. 

```cpp 
namespace math { }
namespace half_life { }
```

#### Classes & Types 
Classes & All type names should be [[PascalCase]], *unless* you think that type should be treated as a [[Primitives|Primitive]], *eg.* something like an `i32`, `char`, `f32`, etc. If you are thinking of naming it like a primitive and need to use multiple words, you most likely shouldn't treat it as a primitive.  


```cpp
class Node { };

struct vec2 { };

using FloatVector = std::vector<f32>;

using mat3 = f32[3][3];
```

### Variables 
#### Local Variables 
Local variables should be kept in [[snake_case]].

```cpp
i32 my_number = 0;
```
#### Constants 
[[constexpr]] variables should be written in [[SCREAMING_SNAKE_CASE]].
```cpp
constexpr float PI = 3.1469420;
```

#### Class Variables
Class fields and static class variables should be in [[snake_case]].

```cpp
class Node2D {
  mat3 position_matrix{};
};
```

### Functions
All functions should be [[snake_case]]. 
```cpp
void lerp(f32 a, f32 b, f32 t);

class Vector2 {
  usize size() const { return 2; }
};
```

>[!Caution] Casting
>Do not use:
>C-style casts
>const casts
>static casts
>reinterpret casts
>*be wary of* dynamic casts