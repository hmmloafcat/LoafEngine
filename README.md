# LoafEngine

***DISCLAIMER:*** This project is still in the works, so it's not available.

---
A 2D indie game engine made with C++ and GLFW

## Programs needed
- [VS Code](https://code.visualstudio.com) (or any IDE you prefer)

## Dependencies
- [GLFW](https://www.glfw.org/)
    - The engine uses GLFW for window management and input handling.
- [g++](https://gcc.gnu.org/)
    - The engine is written in C++ and compiled with g++.

## Q&A

**Q: Is this engine free to use?**

A: Absolutely! Free = cool.

**Q: Is this still in development?**

A: Yes, it's still in development. The engine is not yet available, but it will be soon.

**Q: Will this engine be open source?**

A: Yes, it will be open source! Open source = cool.

## API docs

It uses a custom programming language, called LoafLanguage. It's a simple programming language similar to Python, but for the engine. It has a simple syntax and it's easy to learn.
It uses indentation for functions/loops, similar to Python.

Example code:
```loaf
func main()
    // Display shapes
    
    // square
    square = object.New(shape="square", id=1, posX="center", posY="center", size=80, color="purple")
    
    // circle
    circle = object.New(shape="circle", id=2, posX=100, posY=50, size=60, color="red")
    
    // triangle
    triangle = object.New(shape="triangle", id=3, posX=-150, posY=-100, size=100, color="green")
    
    square.display()
    circle.display()
    triangle.display()
```

## License
This project is licensed under the MIT License. Check [LICENSE](LICENSE) for more info.

## Inspirations
The custom programming language is inspired by [Python](https://python.org), a interpited programming language.
