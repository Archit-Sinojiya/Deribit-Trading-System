# Deribit-Trading-System

This project is a high-performance order execution and management system to trade on Deribit Test.

## Features
The system provides the following order management functionalities:
- Placing buy/sell orders
- Modifying orders
- Cancelling orders
- Viewing current positions
- Getting the orderbook

The project has been implemented in C++, and users require an account on Deribit Test to use the functionalities. All methods require authentication with the correct `client_id` and `client_secret`.

## Project Structure
The project is organized into two main folders:
- **`include/`**: Contains all the header files for each component. Each function is broken into a separate component to ensure modularity.
- **`src/`**: Contains the `.cpp` files that implement each component. Additionally, there are individual testing files to ensure the proper functioning of each component, but these are not required to run the entire project.

## Installation & Usage
To run the project on your local machine:
1. Clone this repository.
2. Navigate to the project directory.
3. Compile and run the project using the following command:

   ```sh
   g++ -o main main.cpp src/cancel_order.cpp src/get_orderbook.cpp src/order.cpp src/sell_order.cpp src/account.cpp src/auth.cpp src/modify_order.cpp -I./include -lcurl
   ./main
   ```

### Building with CMake
Alternatively, you can build the project using `CMakeLists.txt`:

```sh
mkdir build
cd build
cmake ..
make
```

## Requirements
- C++ Compiler (`g++` recommended)
- `libcurl` for HTTP requests
- CMake (optional, for building the project)

## Authentication
Before using the project, ensure you have valid credentials (`client_id` and `client_secret`) from Deribit Test for authentication.

---

For any issues or contributions, feel free to open a pull request or create an issue.

