# Jazz

Jazz - JIT/AOT compiled programming language that uses gccjit for emitting machine code.

# Roadmap
You can see roadmap there: [Jazz Roadmap](https://github.com/users/playXE/projects/3)

# TODO
- ~~constexpr functions~~ DONE!
- Macros
- ~~Jazz2C++ Translator~~ DONE!
- ~~Struct initialization:~~ DONE!

# Building book
```
$ cd book
$ mdbook build
$ mdbook serve
```

Now you can open `http://localhost:3000/` in your browser.

# Example code

Factorial: 
```go
import "std/libc.jazz"
func factorial(x: i32) i32 {
    if x == 0 {
        return 1;
    } else {
        return factorial(x - 1) * x;
    }
}

pub func main() i32 {
    printf("%i\n",factorial(5));

    return 0;
} 
```

# Building

1. Install libgccjit with version >= 9: 
    Fedora Linux
    ```
    sudo dnf install libgccjit-devel
    ```
    Ubuntu Linux
    ```
    sudo apt install libgccjit-9-dev
    ```
2. Run `cargo build --release`
3. Run `cargo install --path .`

# Libraries and programs written in Jazz
- [AllegroJazz](https://github.com/playXE/AllegroJazz/) Jazz bindings to Allegro 5 library.
    - [Snake](https://github.com/playXE/Snake-Jazz/) Snake game written in Jazz using AllegroJazz library
