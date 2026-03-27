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

    // Languages
    std::vector<std::string> greetings = {
        "Hello World",       // English
        "Hola Mundo",        // Spanish
        "Bonjour le Monde",  // French
        "Kamusta Mundo"      // Filipino
    };

    size_t textID = engine.drawText(greetings[currentIndex], 100.0f, 100.0f, 1.0f, Color(1, 1, 1, 1));

    // Loop
    while (!engine.shouldClose()) {
        float currentTime = (float)glfwGetTime();

        engine.update();

        // Checking
        if (currentTime - lastSwitchTime >= 10.0f) {
            // Cycle the index
            currentIndex = (currentIndex + 1) % greetings.size();
            
            // Update the text
            engine.updateText(textID, greetings[currentIndex]);
            
            lastSwitchTime = currentTime;
        }

        engine.render();
        engine.display();
    }

    return 0;
}
```
