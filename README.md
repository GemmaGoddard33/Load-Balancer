# Load Balancer Simulation

This project is a **Load Balancer Simulation** implemented in C++ that demonstrates how a load balancer distributes incoming requests to multiple servers using threads. The simulation also optimizes the handling of request distribution by managing threads efficiently and dynamically accommodating random request arrivals. This project also simulates "spinning up" and "spinning down" servers to ensure resources are optimized. 

## Features

1. **Threaded Load Balancing**:
   - Incoming requests are processed by multiple threads representing servers.
   - Each server processes requests assigned by the load balancer.

2. **Randomized Request Generation**:
   - A dedicated thread dynamically generates random incoming requests and adds them to the load balancer queue.

3. **Optimization**:
   - Efficient thread management ensures balanced distribution of requests.
   - The load balancer dynamically adjusts to handle the varying request load.

## Components

### 1. **Driver**
   - The entry point of the program.
   - Initializes the load balancer and servers.
   - Manages simulation lifecycle.

### 2. **Request**
   - Represents a single request with properties like ID and processing time.
   - Encapsulates the data necessary for processing.

### 3. **LoadBalancer**
   - Central component that manages request distribution.
   - Optimizes allocation of requests to available threads.
   - Uses a synchronized queue to handle incoming and processed requests.

### 4. **WebServer**
   - Simulates a server that processes requests.
   - Runs in its own thread and continuously fetches requests from the load balancer.

---

## Executing the Code

1. Compile the code using the MakeFile

``` make ```

2. Execute the Code

``` ./balancer ```

You can view sample output in the output.txt file
