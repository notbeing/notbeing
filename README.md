```cpp
#include <iostream>
#include <vector>
#include <string>

class Developer {
public:
    std::string name;
    std::vector<std::string> language_stack;
    bool loves_sleep;

    Developer(std::string name, std::vector<std::string> language_stack, bool loves_sleep) {
        this->name = name;
        this->language_stack = language_stack;
        this->loves_sleep = loves_sleep;
    }

    void presentYourself() {
        std::cout << "Hello, my name is " << this->name << "." << std::endl;
        std::cout << "I'm a developer and I work with these programming languages: " << std::endl;
        
        for(auto &lang : this->language_stack) {
            std::cout << "- " << lang << std::endl;
        }

        if (this->loves_sleep) {
            std::cout << "Also, I really love sleep!" << std::endl;
        } else {
            std::cout << "And, surprisingly, I don't like to sleep." << std::endl;
        }
    }
};

int main() {
    std::vector<std::string> language_stack = {"Python", "Golang"};
    Developer dev("notbeing", language_stack, true);
    dev.presentYourself();
    return 0;
}

```
