# Valerie De Leon-Chavarria's Portfolio

Welcome! This repository serves as a public showcase for my projects and coding style. 

> **Note on Privacy:** The full source code for these projects is hosted in private repositories due to proprietary data, to adhere to academic integrity guidelines, and to protect core solutions. However, I have provided architecture overviews, deep dives, and isolated, sanitized code samples below.
> 
> *If you are a hiring manager and would like temporary collaborator access to a specific private repository, please reach out to me via LinkedIn or email found below.*

---
## Global Technical Skills

*   **Languages:** HTML & CSS, JavaScript, Python, C++, C, SQL, MATLAB
*   **Frameworks & Libraries:** React, Next.js, Node.js, FastAPI
*   **Tools & DevOps:** VSCode, Sublime Text, Linux Ubuntu, Git, Docker, GitHub Actions (CI/CD)

---
## University of California, Merced Course Descriptions
This is a list of courses I have taken within UC Merced to help understand the importance of a project

### 1. CSE 031 - Computer Organization and Assembly Language
* **Professor:** Santosh Chandrasekhar
* **Term:** Spring 2025
* **Course Description:** Exposes students to the underlying structure of machines. Starting from C programming, pointers, data representation, MIPS instruction-set, Compilation process and down to Hardware implementation.

---
## Featured Projects

### 1. CSE 031 - Lab 1: Introduction to C
This project explores foundational system concepts, including pointer arithmetic, procedural logic, and memory-safe input handling in C.

#### Private Repository Structure
The original private workspace consists of the following components:
*   `averages.c` — The primary engine handling dynamic numeric analysis and statistical calculation.
*   `punishment.c` — A control-flow module demonstrating precise string formatting and looping constructs.
*   `pseudoAverages.txt` — The algorithmic pseudocode mapping out optimization workflows before writing C.
*   `tpsAnswers.txt` — Technical analysis and conceptual write-ups regarding compilation behavior and memory limits.

#### Architectural Breakdown
1. Dynamic Arithmetic & Processing (`averages.c `)
The logical core of this module processes multi-type data arrays while preventing boundary and rounding errors. 
    *   **Key Challenge:** Preventing integer overflow during accumulation operations.
    *   **Design Choice:** Implemented explicit floating-point promotion rules (`(double)`) before executing divisions to retain precision during memory aggregation.

2. Formatted String Looping (`punishment.c`)
This subsystem handles repetitive generation rules based on user input, ensuring robust validation routines.
    *   **Design Choice:** Utilized safe buffered reading strategies to handle dynamic inputs without risking standard stack overflow vulnerabilities common to `scanf`.

#### Clean Code Sample (Sanitized Concept)
Below is an abstract example demonstrating the style and structural patterns used in `averages.c` to securely compute datasets without data corruption:

```c
#include <stdio.h>

/**
 * Computes the data set average safely by enforcing floating-point promotion.
 */
double compute_safe_average(const int current_dataset[], int dataset_size) {
    if (dataset_size <= 0) {
        return 0.0;
    }
    
    long long total_accumulator = 0; // Using a wider type to catch potential overflow
    for (int index = 0; index < dataset_size; index++) {
        total_accumulator += current_dataset[index];
    }
    
    // Explicit type conversion ensures arithmetic precision
    return (double)total_accumulator / dataset_size;
}

int main() {
    int sample_data[] = {10, 20, 30, 40, 50};
    int data_length = sizeof(sample_data) / sizeof(sample_data[0]);
    
    double average_result = compute_safe_average(sample_data, data_length);
    printf("Computed Dataset Performance Average: %.2f\n", average_result);
    
    return 0;
}
```

#### Key Technical Takeaways
  *   **Compilation Flow:** Analyzed compiler behavior and optimization flags by tracing the output of `a.out` against raw code executions.
  *   **System Profiling:** Documented terminal environment variables and text formatting constraints within `tpsAnswers.txt`.
---

## Let's Connect!

*   **LinkedIn:** [Valerie De Leon-Chavarria]([https://linkedin.com](https://www.linkedin.com/in/valerie-de-leon-231444247/))
*   **Email:** valerie@valerie-deleon.com
*   **Personal Website:** [valerie-deleon.com]([https://yourportfolio.com](https://valerie-deleon.com/))
