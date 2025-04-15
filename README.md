# Bank Fraud Simulator - CS Fundamentals Demo

Hey there! Thanks for checking out this little project. I put this together primarily as an exercise to demonstrate fundamental programming concepts – specifically processing data stored in basic structures like lists (Python) or vectors (C++) – within the context of a simplified bank fraud detection scenario.

## The Concept

The idea here is straightforward: imagine you have a log of bank transactions, and you want a quick way to flag potentially suspicious ones. For this simulation, "suspicious" simply means any transaction (deposit or withdrawal) whose amount goes over a certain predefined limit.

**Important:** This is a very basic simulation! Real-world fraud detection uses much more sophisticated techniques involving machine learning, complex rule engines, pattern analysis, and network analysis. This project *only* looks at individual transaction amounts against a simple threshold.

## Implementations

You'll find two versions here:

1.  **Python (`fraud_detector.py`):** Uses standard Python lists and dictionaries to represent the transaction log. The core logic involves iterating through the list and checking each transaction's amount against the threshold.
2.  **C++ (`fraud_detector.cpp`):** Uses `std::vector` to hold the transactions, with each transaction represented by a `struct`. The logic mirrors the Python version – iterating through the vector and applying the threshold check.

Both versions focus on clear, readable code demonstrating the core task.

## How to Run

Make sure you have Python 3 and a C++ compiler (like g++) installed.

**Python:**

1.  Navigate to the project directory in your terminal.
2.  Run the script:
    ```bash
    python fraud_detector.py
    ```

**C++:**

1.  Navigate to the project directory in your terminal.
2.  Compile the code (using g++ for example):
    ```bash
    g++ fraud_detector.cpp -o fraud_detector -std=c++11
    ```
    *(You might need `c++14` or higher depending on your compiler version if you use newer features, but `c++11` should be fine for this code).*
3.  Run the compiled executable:
    ```bash
    ./fraud_detector
    ```

Both scripts will print the sample transactions being processed, the threshold used, any transactions flagged as potentially fraudulent, and a rough estimate of the processing time.

## Performance Observation (Python vs. C++)

One of the interesting aspects often discussed is the performance difference between languages like Python and C++. For this *specific, simple task* of iterating through a list/vector and performing a basic comparison:

*   **Observation:** In my tests with this code and sample data, the C++ version generally executes noticeably faster than the Python version. You can see the time difference printed at the end of each script's output (Python in seconds, C++ in milliseconds for potentially better granularity on fast machines).
*   **Why?** C++ is a compiled language that translates directly to machine code, often resulting in faster execution for CPU-intensive tasks like looping and basic arithmetic. Python, being interpreted (or JIT-compiled), has some overhead.
*   **The Catch:** This is a *very* simple loop. For more complex real-world data analysis involving large datasets, Python often closes the gap significantly (or even surpasses simple C++ code) by leveraging highly optimized libraries written in C/Fortran (like NumPy and Pandas). Furthermore, Python's development speed is often much faster.

**Conclusion:** For this narrow task, C++ demonstrates a raw speed advantage. However, the "better" language depends entirely on the overall project needs – development time, ecosystem libraries, maintainability, and the specific performance bottlenecks.

## Limitations

*   **Basic Detection:** Only uses a simple amount threshold. Doesn't consider velocity, location, account history, or other crucial factors.
*   **No Real Data:** Uses hardcoded sample data. Needs modification to load data from files/databases.
*   **Simplified Data:** Uses basic types (double in C++, float/int implied in Python) for money – production financial systems require more robust handling (like fixed-point arithmetic or dedicated Money classes) to avoid floating-point errors.

## Purpose

This project is intended to show understanding of basic data structures (lists/vectors), iteration, conditional logic, and function definition in both Python and C++, along with a basic awareness of performance considerations.

Thanks for taking a look!
