# LoafEngine

### This program is not released yet. Pls wait

---

A game engine made in C++ and graphics w/ GLFW.

## The C++ API

The API for the game engine has been switched to C++.

```cpp
#include "loafEngine.h"

int main() {
    // Initalize
    LoafEngine engine;
    engine.window.title("Hello World!");

    // Text
    engine.drawText("Hello, World!", 100.0f, 100.0f, 1.0f, Color(1, 1, 1, 1));

    // Loop
    while (!engine.shouldClose()) {
        engine.update();
        
        engine.render(); 
        
        engine.display();
    }

    return 0;
}
```
