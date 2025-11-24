# Leakcheck
api for leakcheck.io check leak your email site
# main
```cpp
#include "Leakcheck.h"
#include <iostream>

int main() {
   Leakcheck api;
    auto cep = api.check_leak("example@example.com").then([](json::value result) {
        std::cout << result<< std::endl;
    });
    cep.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```



