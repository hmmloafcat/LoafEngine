# LoafEngine

### This program is not released yet. Please wait

---

## Credits and Dependencies

- [GLFW](https://glfw.org)
  - The main graphics API. Can handle input, graphics (obviously), displaying, etc.
- [stb](https://github.com/nothings/stb)
  - Single-header libraries like `stb_image.h` and `stb_vorbis.c`. Made by Sean Barrett. (https://nothings.org)
- [OpenAL](https://openal.org)
  - OpenAL for audio playing.
- [xiph foundation](https://xiph.org)
  - The people who made the OGG audio format. Compressed, but good sound.
 
### All these are free and open-source, no payment needed! Also, thank you contributors/distributors.

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

    size_t currentIndex = 0;
    float lastSwitchTime = 0.0f;

    size_t textID = engine.drawText(greetings[currentIndex], 30.0f, 30.0f, 1.0f, Color(1, 1, 1, 1));

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
