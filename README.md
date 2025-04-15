# Bank Fraud 


## The Concept

The idea here is straightforward: imagine you have a log of bank transactions, and you want a quick way to flag potentially suspicious ones. For this simulation, "suspicious" simply means any transaction (deposit or withdrawal) whose amount goes over a certain predefined limit.

**Important:** This is a very basic simulation! Real-world fraud detection uses much more sophisticated techniques involving machine learning, complex rule engines, pattern analysis, and network analysis. This project *only* looks at individual transaction amounts against a simple threshold.

## Implementations

You'll find a few versions here! All versions focus on clear, readable code demonstrating the core task.

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





This project is intended to show understanding of basic data structures (lists/vectors), iteration, conditional logic, and function definition in both Python and C++, along with a basic awareness of performance considerations.

Thanks for taking a look!
